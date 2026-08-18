# Current Instruction | Launch Parallel Views 02-06

The project is now operating in experimental parallel multi-view mode.

Read and obey:

- `projects/pulla-reddy/PROJECT_RULES.md`
- `projects/pulla-reddy/MULTIVIEW_EXECUTION.md`
- `projects/pulla-reddy/MULTIVIEW_COORDINATOR_INSTRUCTION.md`
- all per-view state files under `projects/pulla-reddy/state/`

## V01 status

V01 is NOT approved beyond Layer 00.

The reworked Layer 01 v4 is waiting for strict independent visual/design review under:

`projects/pulla-reddy/review/V01/`

Do not start V01 Layer 02. Do not use any earlier unpublished downstream V01 files as approved parents. Leave the V01 lane frozen while the other views launch.

## Required coordinator action now

Initialize and start V02 through V06 as independent production lanes immediately.

Use safe parallel agents/tasks where supported. If true parallel agents are unavailable, initialize all five lanes during this run and then execute them round-robin without waiting for V01.

For each view:

1. Use the source mapping in `MULTIVIEW_EXECUTION.md`.
2. Create or confirm the correct local folder under `D:/Codex/G Pulla Reddy Sweets/01_Views/`.
3. Keep all view assets directly inside that one folder. Do not create layer or revision subfolders.
4. Extract the authoritative source image from the root project PDF.
5. Lock camera, crop, perspective, architecture, ceiling grid, materials, furniture and products.
6. Create Layer 00 first.
7. Publish a dedicated review package under `projects/pulla-reddy/review/V0X/` with `STATUS.md`, `manifest.json`, `SELF_QA.md`, a review-sized candidate preview and source-versus-Layer-00 comparison.
8. Update only that view's state file under `projects/pulla-reddy/state/`.
9. Stop that lane at `waiting_for_chatgpt_review` after its Layer 00 package is published. Do not mix files or states between views.

## Shared V02 / V06 planter requirement

Before generating either Layer 00, establish one shared planter design and record it in:

`projects/pulla-reddy/SHARED_PLANTER_SPEC.md`

The spec must lock:

- planter geometry and material language;
- planting height, density and rhythm;
- relationship to the curved built-in seater;
- how it remains physically consistent across V02 and V06;
- later concealed 3000K planter-lighting intent for soft foliage shadows.

Use the same planter design in V02 and V06 from Layer 00 onward. The planter is present but unlit in Layer 00.

## Quality rules

- 3000K only for later electric-lighting layers.
- Recessed, concealed or integrated lighting only.
- No visible pendants, tracks or surface fixtures.
- No global exposure cheating.
- No architecture or camera drift.
- No speculative redesign beyond the explicitly required shared planter.
- Correct objective defects autonomously before publishing.

## Coordinator report

After all five lanes are initialized and their Layer 00 packages are either published or actively running, create or update:

`projects/pulla-reddy/COORDINATOR_STATUS.md`

Report each view's local folder, source page, current task/layer, review path, state, blockers and shared dependencies.

Do not assemble the final presentation yet.
