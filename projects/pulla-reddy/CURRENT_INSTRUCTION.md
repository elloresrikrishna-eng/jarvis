# Current Instruction | Parallel Production After V01 Layer 04 Approval

## Immediate objective

Keep every valid production lane moving independently. Do not wait for user intervention where the locked project rules already determine the answer.

Read and obey:

- `projects/pulla-reddy/PROJECT_RULES.md`
- `projects/pulla-reddy/MULTIVIEW_EXECUTION.md`
- `projects/pulla-reddy/MULTIVIEW_COORDINATOR_INSTRUCTION.md`
- `projects/pulla-reddy/control/schemas/jarvis-decision.schema.json`
- all per-view state files under `projects/pulla-reddy/state/`
- all current JARVIS decisions under `projects/pulla-reddy/control/decisions/`

## Priority 1 | V01 Layer 05 rear seating comfort

V01 Layer 04 central-merchandise / circulation candidate is independently approved.

Approved immutable parent:

`58553357484f01018a2d8a3929c3c662d67b3fbc21143847bb255d1c7d2ed837`

Decision:

`jarvis-v01-l04-58553357-approve-001`

Execute:

`projects/pulla-reddy/instructions/V01_LAYER05_REAR_SEATING_COMFORT.md`

Create Layer 05 from the exact approved Layer 04 parent. Add only restrained recessed 3000K comfort lighting for the visible rear seating / hospitality zone. Keep the rear area clearly softer and calmer than the sweet counters, wall shelves and central merchandise. Preserve all approved counter, wall-wash, shelf-integrated and central-merchandise lighting exactly apart from unavoidable local interaction.

Publish through the GitHub Actions binary review-artifact path and stop V01 at `READY_FOR_JARVIS_REVIEW` after remote retrievability and provenance are verified.

Do not begin Layer 06 until Layer 05 receives exact candidate-bound independent JARVIS approval.

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

Then:

1. Build/rebuild V02 Layer 00 from its authoritative source with the shared planter present and ALL electric lighting off.
2. Build/rebuild V06 Layer 00 from its authoritative source with the same shared planter present and ALL electric lighting off.
3. Preserve camera, crop, perspective, architecture, ceiling grid, furniture, products, materials and colours except for the explicitly mandated planter intervention.
4. Publish each Layer 00 through the GitHub Actions binary review-artifact path.
5. Set each lane to `READY_FOR_JARVIS_REVIEW` and stop that lane for independent review.
6. Do not rebuild later layers until the exact Layer 00 candidate for that view is independently approved.

The previously rejected V06 Layer 03 candidate remains invalid as a parent. Its restrained under-seat character may only be reused after the parent chain is repaired.

## Priority 4 | V04/V05

Continue each lane independently from its current valid Layer 00 initialization state. If a lane is `codex_action_required`, execute the current valid instruction rather than waiting for the user. Publish the resulting candidate through the same GitHub Actions binary review-artifact path and stop at `READY_FOR_JARVIS_REVIEW`.

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
