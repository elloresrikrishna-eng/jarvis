# Current Instruction | Recovery + Artifact Migration

This instruction supersedes the previous passive parallel-launch instruction where they conflict.

## Immediate objective

Unblock the JARVIS return loop. Do useful production work now. Do not wait for user intervention where the project rules already determine the answer.

Read and obey:

- `projects/pulla-reddy/PROJECT_RULES.md`
- `projects/pulla-reddy/MULTIVIEW_EXECUTION.md`
- `projects/pulla-reddy/MULTIVIEW_COORDINATOR_INSTRUCTION.md`
- `projects/pulla-reddy/control/schemas/jarvis-decision.schema.json`
- all per-view state files under `projects/pulla-reddy/state/`
- all current JARVIS decisions under `projects/pulla-reddy/control/decisions/`

## Priority 1 | V01 artifact migration

V01 Layer 01 v4 remains unapproved. Do not advance to Layer 02.

Republish the exact existing V01 Layer 01 v4 candidate through the current GitHub Actions binary review-artifact path used by `jarvis-return-path-v1`.

Requirements:

1. Do not regenerate or visually modify V01 Layer 01 v4 merely to migrate it.
2. Calculate and preserve its exact candidate SHA-256.
3. Publish the exact candidate PNG plus required manifest/provenance as a GitHub Actions review artifact.
4. Record the workflow run ID and artifact ID in the V01 review/control state.
5. Set V01 to `READY_FOR_JARVIS_REVIEW` only when the artifact is remotely retrievable and provenance is valid.
6. Stop V01 there for independent JARVIS review.

## Priority 2 | V02/V06 shared planter parent-chain repair

The shared planter is mandatory and must exist physically from Layer 00 onward in both V02 and V06.

If `projects/pulla-reddy/SHARED_PLANTER_SPEC.md` does not exist, create it first from the authoritative project rules and source geometry. Lock one shared design covering geometry, material language, planting height, density, rhythm, relationship to the curved built-in seater, cross-view consistency, and later concealed 3000K planter-lighting intent.

Then:

1. Build/rebuild V02 Layer 00 from its authoritative source with the shared planter present and ALL electric lighting off.
2. Build/rebuild V06 Layer 00 from its authoritative source with the same shared planter present and ALL electric lighting off.
3. Preserve camera, crop, perspective, architecture, ceiling grid, furniture, products, materials and colours except for the explicitly mandated planter intervention.
4. Publish each Layer 00 through the GitHub Actions binary review-artifact path.
5. Set each lane to `READY_FOR_JARVIS_REVIEW` and stop that lane for independent review.
6. Do not rebuild later layers until the exact Layer 00 candidate for that view is independently approved.

The previously rejected V06 Layer 03 candidate must NOT be treated as an approved parent. Its successful under-seat character may only be reused after the parent chain is repaired.

## Priority 3 | V03/V04/V05

Continue each lane independently from its current valid state. If a lane is `codex_action_required`, execute the current valid instruction rather than waiting for the user. Publish the resulting candidate through the same GitHub Actions binary review-artifact path and stop at `READY_FOR_JARVIS_REVIEW`.

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

V01, V02, V03, V04, V05 and V06 are independent lanes. Use parallel workers where supported. A blocked/rejected lane must not prevent useful work in other lanes.

## Coordinator output

Update `projects/pulla-reddy/COORDINATOR_STATUS.md` after actions are released/performed. For each view record current layer, exact candidate SHA when applicable, artifact ID, workflow run ID, state, blocker and next machine action.

The desired resting state is NOT `codex_action_required` when an objective machine action can be performed. Execute it. The desired resting state after publishing a candidate is `READY_FOR_JARVIS_REVIEW`.

Do not assemble the presentation yet.
