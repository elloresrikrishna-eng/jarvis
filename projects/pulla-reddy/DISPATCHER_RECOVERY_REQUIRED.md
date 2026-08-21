# Pulla Reddy | Dispatcher Recovery Required

## Diagnosis

The control plane has valid released work for all six view lanes, but the local Codex/Jarvis dispatcher is not consuming it.

Recovery evidence:

- Redispatch commit: `8a0a5ae036a0f56f88e57898ceef8a8495992284`
- Redispatch committed at: `2026-08-21T13:15:12Z`
- Recovery re-check at: `2026-08-21T16:13:23Z`
- New production/review commits after redispatch: `0`
- All released lanes remain machine-actionable and none has published a fresh `READY_FOR_JARVIS_REVIEW` candidate.

This is an operational dispatcher/heartbeat failure, not a lighting-design decision and not a reason to alter any approved parent, correction brief, or view queue.

## Required recovery behaviour

When the local dispatcher next starts or wakes:

1. Read `PROJECT_RULES.md`, `CURRENT_INSTRUCTION.md`, `STATE.json`, `COORDINATOR_STATUS.md`, and all per-view state files.
2. Do not invent new tasks. Consume only the exact currently released tasks.
3. Publish a dispatcher heartbeat before starting production so the control plane can distinguish a live worker from a stalled one.
4. Recommended heartbeat path: `projects/pulla-reddy/control/dispatcher-heartbeat.json`.
5. The heartbeat should record UTC timestamp, dispatcher version, current root-state blob/commit reference if available, current instruction reference, active local project root, and worker status.
6. Execute the six already-released lanes independently where safe.
7. For every produced candidate, use the GitHub Actions binary review-artifact path, verify exact SHA-256 provenance and remote retrievability, set only that lane to `READY_FOR_JARVIS_REVIEW`, and stop at its review gate.
8. Never advance a lane beyond its released task without exact candidate-bound JARVIS approval.

## Currently released machine work

- V01: repaired lighting concept sketch.
- V02: Layer 02 concealed shelf-integrated lighting.
- V03: Layer 01 sweet-counter downlighting.
- V04: valid Layer 00 initialization.
- V05: Layer 01 recessed wall-wash.
- V06: repaired Layer 01 seating/table comfort lighting.

Presentation generation remains locked.

No user design decision is required.
