# Current Instruction | Parallel Production After V01 Continuity Failure

## Immediate objective

Keep every valid production lane moving independently. Do not wait for user intervention where the locked project rules already determine the answer.

Read and obey:

- `projects/pulla-reddy/PROJECT_RULES.md`
- `projects/pulla-reddy/MULTIVIEW_EXECUTION.md`
- `projects/pulla-reddy/MULTIVIEW_COORDINATOR_INSTRUCTION.md`
- `projects/pulla-reddy/control/schemas/jarvis-decision.schema.json`
- all per-view state files under `projects/pulla-reddy/state/`
- all current JARVIS decisions under `projects/pulla-reddy/control/decisions/`

## Priority 1 | V01 Layer 02 coordinate-continuity repair

The V01 Cross-Layer Continuity Audit candidate:

`6a9f3e21c631dd20a8a866391fa7cecb7d5ca4be6563fea9b347149c721b6f4e`

is rejected as a completion gate under:

`jarvis-v01-l09-6a9f3e21-reject-001`

because it proves a blocking coordinate-continuity defect beginning at historical Layer 02. JARVIS independently retrieved the exact Layer 01 and Layer 02 artifacts, verified their SHA-256 values and reproduced the one-pixel vertical registration mismatch.

The last valid immutable render parent is exact approved Layer 01:

`bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217`

Execute:

`projects/pulla-reddy/instructions/V01_LAYER02_COORDINATE_REPAIR.md`

Build a NEW Layer 02 from the exact approved Layer 01 parent. Add only the released recessed 3000K wall-wash family. Preserve the useful wall-wash design character of the historical Layer 02 as a visual reference, but do not use that defective raster as a pixel parent and do not simply shift it to hide the defect.

The repaired candidate must be exactly `1624 x 968`, must have best registration `dx=0, dy=0` against Layer 01, must preserve protected regions without broad negative deltas, must not use global exposure/gamma changes, and must retain the counter-led hierarchy with a quiet ceiling.

Publish through the GitHub Actions binary review-artifact path, verify provenance and remote retrievability, set V01 to `READY_FOR_JARVIS_REVIEW`, and stop.

Do not begin repaired Layer 03 until repaired Layer 02 receives exact candidate-bound independent JARVIS approval.

Historical Layers 02-06 and Final remain immutable evidence but are invalid as production parents until the chain is rebuilt sequentially and re-approved. The concept sketch remains communication-only. V01 contact-sheet/review-board production remains locked until the repaired chain reaches Final and a fresh continuity audit passes.

## Priority 2 | V03 Layer 01 counter downlighting

V03 Layer 00 night base candidate is independently approved.

Approved immutable parent:

`a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a`

Decision:

`jarvis-v03-l00-a6056c69-approve-001`

Execute:

`projects/pulla-reddy/instructions/V03_LAYER01_COUNTER_DOWNLIGHTING.md`

Create Layer 01 from the exact approved Layer 00 parent. Add only controlled deep-recessed 3000K downlighting over the visible sweet display counter(s). Make the sweets the first visual destination without globally lifting exposure, disturbing glass readability, brightening wall shelves, or changing circulation and seating.

Publish through the GitHub Actions binary review-artifact path and stop V03 at `READY_FOR_JARVIS_REVIEW` after remote retrievability and provenance are verified.

Do not begin the V03 wall-wash layer until Layer 01 receives exact candidate-bound independent JARVIS approval.

## Priority 3 | V02/V06 shared planter parent-chain repair

The shared planter is mandatory and must exist physically from Layer 00 onward in both V02 and V06.

If `projects/pulla-reddy/SHARED_PLANTER_SPEC.md` does not exist, create it first from the authoritative project rules and source geometry. Lock one shared design covering geometry, material language, planting height, density, rhythm, relationship to the curved built-in seater, cross-view consistency, and later concealed 3000K planter-lighting intent.

Then build/rebuild V02 and V06 Layer 00 from their authoritative sources with the exact shared planter present and all electric lighting off. Publish each through the GitHub Actions binary review-artifact path and stop each lane at `READY_FOR_JARVIS_REVIEW`. Do not rebuild later layers until the exact Layer 00 candidate for that view is independently approved.

The previously rejected V06 Layer 03 candidate remains invalid as a parent. Its restrained under-seat character may only be reused after the parent chain is repaired.

## Priority 4 | V04/V05

Continue each lane independently from its current valid Layer 00 initialization state. If a lane is `codex_action_required`, execute the current valid instruction rather than waiting for the user. Publish the resulting candidate through the GitHub Actions binary review-artifact path and stop at `READY_FOR_JARVIS_REVIEW`.

Never self-approve. Deterministic QA is Gate 1, not design approval.

## Global locks

- 3000K only for electric-lighting layers.
- Recessed, concealed or integrated lighting only.
- No visible pendants, tracks or surface fixtures.
- No global exposure/gamma cheating.
- No camera, crop, architecture, material or furniture drift.
- One new intended circuit per cumulative layer.
- Previous approved layers remain frozen.
- Every review candidate must be remotely retrievable as a GitHub Actions artifact and bound to its exact SHA-256.
- Presentation generation remains locked until every required view has a valid independent JARVIS approval chain.

## Parallel execution

V01, V02, V03, V04, V05 and V06 are independent lanes. Use parallel workers where supported. A blocked or rejected lane must not prevent useful work in other lanes.

## Coordinator output

Update `projects/pulla-reddy/COORDINATOR_STATUS.md` after actions are released or performed. For each view record current layer, exact candidate SHA when applicable, artifact ID, workflow run ID, state, blocker and next machine action.

The desired resting state is NOT `codex_action_required` when an objective machine action can be performed. Execute it. The desired resting state after publishing a candidate is `READY_FOR_JARVIS_REVIEW`.

Do not assemble the presentation yet.
