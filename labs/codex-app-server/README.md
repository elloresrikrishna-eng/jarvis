# JARVIS Codex App Server Lab

Status: isolated experiment only

This lab evaluates whether `codex app-server` can replace a narrow part of JARVIS transport/orchestration without weakening JARVIS governance, provenance, approval, or exactly-once guarantees.

It does not change Light the Space runtime code. It does not change JARVIS `main`. It is not authorized to merge automatically.

## Why this lives in JARVIS

Light the Space V2 deliberately keeps simulation, judges, mentor planning, and correctness independent from any required external AI runtime. Codex therefore belongs outside the application as an optional execution/orchestration adapter.

The candidate boundary is:

`JARVIS Governor -> Codex App Server Adapter -> Codex Thread/Turn -> bounded workspace`

The governor remains authoritative for whether work may start, what repository/ref is targeted, which writes are permitted, whether a retry is allowed, and whether the result may advance a project gate.

## Protocol assumptions

The lab targets the current `codex app-server` protocol:

- bidirectional JSON-RPC-style messages over stdio JSONL
- one `initialize` request followed by `initialized`
- `thread/start` or `thread/resume`
- `turn/start` for work
- streamed turn/item notifications
- `turn/completed` as the terminal turn signal
- server-initiated approval requests for commands, file changes, permissions, and other interactive operations

Reference: https://github.com/openai/codex/blob/main/codex-rs/app-server/README.md

The lab treats any non-JSON stdout as protocol corruption and fails.

## Safety posture

The first canaries are intentionally more restrictive than production JARVIS would need:

- target repository must already be a Git repository
- starting HEAD and complete `git status --porcelain` are captured
- the default canary uses read-only sandboxing and no network
- approval requests fail closed
- every sent/received protocol message is written to an external JSONL trace
- successful plan IDs are written to an external journal
- a completed plan ID cannot execute twice through the harness
- the target repository must have the same HEAD and worktree state after the canary
- `JARVIS_APP_SERVER_SHOULD_NOT_EXIST.txt` is a hard tripwire

Trace and journal files default to the operating-system temp directory so the target repository does not become dirty merely because it was tested.

## Canary modes

### 1. Read-only transport canary

Purpose: prove initialization, thread creation, turn execution, event streaming, repository visibility, and no target-repository mutation.

```powershell
node labs/codex-app-server/smoke.mjs `
  --mode readonly `
  --plan-id lts-appserver-readonly-001 `
  --cwd "D:\Codex\Light the Space"
```

Pass requires:

- turn starts and completes
- agent returns `JARVIS_APP_SERVER_CANARY_OK`
- no approval request is raised
- no file-change item is observed
- HEAD and full worktree status are byte-identical before and after

### 2. Approval-denial canary

Purpose: prove the adapter can receive a write/permission approval request, deny it, and preserve the repository.

```powershell
node labs/codex-app-server/smoke.mjs `
  --mode approval-deny `
  --plan-id lts-appserver-approval-001 `
  --cwd "D:\Codex\Light the Space"
```

Pass requires an approval request to be observed and denied, followed by a terminal turn with no actual target-repository mutation. A proposed `fileChange` item is allowed in this mode because the repository invariant is authoritative.

### 3. Interrupt canary

Purpose: exercise `turn/interrupt` and verify interruption cannot leave a write behind.

```powershell
node labs/codex-app-server/smoke.mjs `
  --mode interrupt `
  --plan-id lts-appserver-interrupt-001 `
  --cwd "D:\Codex\Light the Space"
```

The current interrupt test is a transport/lifecycle canary, not yet a crash-recovery proof. It passes only when the interrupt is issued and repository invariants remain unchanged.

## Exactly-once boundary

The lab does not assume Codex itself provides JARVIS business-level exactly-once semantics.

JARVIS owns that guarantee.

The smoke harness accepts a caller-provided `--plan-id` and records successful IDs in a journal. Reusing a completed ID exits before starting a new app-server process. A production adapter would replace this JSON journal with the existing durable JARVIS state/audit layer.

This distinction is intentional:

- app-server owns Codex conversation and turn lifecycle
- JARVIS owns project action identity, authorization, retry policy, and side-effect accounting

## Acceptance matrix

| Gate | Required before any wider integration |
| --- | --- |
| Transport | initialize/start/turn/complete works repeatedly through stdio |
| Protocol cleanliness | stdout contains protocol JSON only |
| Read-only invariant | read canary leaves HEAD and worktree unchanged |
| Approval | a requested write can be denied without mutation |
| Interrupt | interrupted turn leaves no mutation |
| Auditability | complete send/receive trace is retained |
| Exactly-once | duplicate completed plan ID is rejected before execution |
| Failure handling | malformed protocol, timeout, child-process failure, and unknown server request fail closed |
| Existing JARVIS governor | remains the authority above the adapter |
| Light the Space boundary | zero app-server dependency in application runtime |

## Not yet authorized

Do not yet:

- replace the current browser/JARVIS transport
- give app-server unrestricted workspace write access
- enable network in this lab
- auto-accept command, file, permission, or MCP approvals
- persist Codex thread IDs as the sole source of project state
- let Codex decide retry authorization
- couple Light the Space frontend/backend correctness to Codex availability
- merge this branch to `main`

## Next gate after local evidence

Run the three canaries against the real local Light the Space worktree and retain their result/trace files. If all three pass, the next experiment may introduce a disposable temporary workspace write test with explicit JARVIS authorization and hash-based postconditions.

Only after that evidence should we decide whether app-server is worth adapting into the existing JARVIS executor layer.
