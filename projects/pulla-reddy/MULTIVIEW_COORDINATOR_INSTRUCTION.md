# Current Coordinator Instruction | Launch Parallel Views

The production strategy is now parallel multi-view execution.

Read and obey:
- `PROJECT_RULES.md`
- `MULTIVIEW_EXECUTION.md`
- existing per-view task/queue files

## Required coordinator action

Set up independent production lanes for V02 through V06 while leaving the existing V01 lane intact.

For each new view:
1. Create/assign the correct local view folder using the existing project workflow.
2. Extract the authoritative source image from the mapped PDF page.
3. Build Layer 00 first, preserving camera, architecture and materials.
4. For V02 and V06, add the same permanent curved-seater planter intervention from Layer 00 onward. Establish one shared planter design and reuse it consistently across both views.
5. Create a per-view execution queue based on `MULTIVIEW_EXECUTION.md`.
6. Create a dedicated Jarvis review path under `projects/pulla-reddy/review/V0X/`.
7. Publish per-view state/status without overwriting another lane.
8. Progress each lane independently through its queue, stopping at review gates as required by the control protocol.

## Parallelism

Run V02-V06 concurrently where the Codex environment supports safe parallel agents/tasks.

Do not serialize all views behind V01 unless a shared design dependency requires it.

The only deliberate dependency is the V02/V06 planter lock. Whichever view establishes the first reviewer-approved planter geometry becomes authoritative for the other.

## Do not do

- Do not merge view folders.
- Do not reuse one image output as another view's source.
- Do not create layer/revision subfolders.
- Do not change V01's already approved base or prior layers.
- Do not assemble the final presentation yet.

## Completion of launch step

When all five additional lanes are initialized and at least Layer 00 production has begun or been queued safely, publish a coordinator status file describing:
- each active view
- current layer/task
- local folder
- review path
- blockers/shared dependencies

Then allow the lanes to continue independently.
