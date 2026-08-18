# Pulla Reddy Autonomous Production Protocol

## Active architecture | JARVIS return path v1

The active production review path is:

`WORKER -> DETERMINISTIC QA -> GITHUB ACTIONS IMAGE ARTIFACT -> EXTERNAL JARVIS REVIEW -> STRUCTURED GITHUB DECISION -> WORKER`

Canonical decisions are stored relative to this project control root at:

- `control/decisions/<project>/<view>/<layer>/latest.json`
- `control/decisions/<project>/<view>/<layer>/history/<decision-id>.json`

Every decision is schema validated and bound to the exact candidate SHA-256. Immutable history, a create-only claim, and an immutable consumption record prevent replay. Views run independently; one view's rejection cannot block another view. Within one view, only one active candidate per layer is allowed.

The direct OpenAI API visual reviewer and the internal Codex reviewer are `LEGACY / INACTIVE`. Neither may grant production approval. `OPENAI_API_KEY` and `OPENAI_REVIEW_MODEL` are not required by the active loop.

Only an exact external JARVIS `APPROVE` decision can complete a required layer. Presentation generation stays locked at `WAITING_FOR_ALL_VIEWS` until every required view is complete.

The sections below describe the earlier scheduled-run protocol and are retained as historical operating context. Where they conflict with this active architecture, JARVIS return path v1 controls.

This protocol exists to remove Srikrishna from the repetitive prompt-carrying loop between ChatGPT and Codex.

## Roles

- Srikrishna: design owner. Only needed for genuine design decisions or final approvals.
- ChatGPT: design director, reviewer and controller through the `jarvis` repository.
- Codex: local production agent working in `D:/Codex/G Pulla Reddy Sweets`.

## Control plane

The `jarvis` repository is the communication layer. The local `D:/Codex/G Pulla Reddy Sweets` folder remains the production workspace.

Codex must not require Srikrishna to copy routine prompts between ChatGPT and Codex once the automation is active.

## Codex scheduled-run behaviour

On each scheduled run in the current View 01 thread:

1. Preserve the full context of the existing View 01 conversation.
2. Read local `README.md` and `AGENTS.md`.
3. Read:
   - `projects/pulla-reddy/PROJECT_RULES.md`
   - `projects/pulla-reddy/V01_TASK.md`
   - `projects/pulla-reddy/STATE.json`
   - `projects/pulla-reddy/CURRENT_INSTRUCTION.md`
4. If `STATE.json` says `codex_action_required`, execute `CURRENT_INSTRUCTION.md`.
5. If the state says `waiting_for_chatgpt_review`, do not advance a lighting layer. Only ensure the required review package is present in Jarvis.
6. If the state says `blocked_user_decision`, stop production and preserve all work.
7. Never advance beyond the explicitly released lighting layer.
8. Never ask Srikrishna routine production questions that are answerable from local assets, project rules or Jarvis.

## Required review package after every generated layer

After producing any layer, Codex must publish a lightweight review package to:

`projects/pulla-reddy/review/V01/`

At minimum publish:

- `STATUS.md`
- `manifest.json`
- a reasonably compressed visual preview of the newly generated layer, named consistently, suitable for ChatGPT review through GitHub
- if practical, a side-by-side or contact-sheet preview comparing the prior approved layer with the new candidate

The manifest must include:

- view name
- source filename
- candidate filename
- candidate layer number
- image dimensions
- exact new lighting circuit introduced
- whether camera/crop alignment changed
- whether architecture/materials/products changed
- whether any previous lighting layer changed unexpectedly
- any warnings or uncertainty

Do not publish enormous production-resolution assets to Jarvis when a review-sized preview is sufficient. High-resolution masters remain in the local project folder.

## State transitions

Codex may set only these production-facing states in `STATE.json`:

- `waiting_for_chatgpt_review`
- `blocked_user_decision`
- `view_complete`

ChatGPT controls release of the next layer by setting:

- `codex_action_required`

## QA rules before publishing a candidate

Codex must self-check:

- exact camera and crop continuity
- architecture continuity
- ceiling-grid continuity
- furniture/product continuity
- previous-layer freeze
- 3000K-only lighting
- no visible non-recessed luminaires
- no global exposure cheat
- new circuit is the only intended lighting addition

If a candidate clearly fails these checks, Codex should correct it itself before publishing the review package rather than sending a knowingly bad candidate.

## Escalation

Only set `blocked_user_decision` when the problem is genuinely subjective or requires Srikrishna's design choice. Technical production errors, alignment drift, rendering defects and rule violations are not user decisions and should be corrected autonomously.

## View 01 completion

Once ChatGPT approves the final View 01 render, Codex should mark `view_complete`. Do not autonomously start View 02 until the control plane explicitly creates/releases View 02 work.
