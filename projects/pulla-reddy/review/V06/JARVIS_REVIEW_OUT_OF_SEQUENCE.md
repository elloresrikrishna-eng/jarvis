# V06 Curved Seating Hero | Jarvis Control Review

## Decision

**REJECT SUBMISSION / DO NOT ADVANCE**

This is a control-protocol rejection, not a visual-quality verdict on the pixels in `jarvis-review-test/V06/layer_03.png`.

## What failed

A Layer 03 under-seater candidate was submitted for review while the authoritative V06 per-view state still requires initialisation and Layer 00 production, with `approved_through_layer: -1`.

The mandatory shared V02/V06 planter specification also does not yet exist in the control plane. V06 therefore has no reviewer-approved Layer 00 parent and no approved Layer 01 or Layer 02 chain from which Layer 03 could legally inherit.

## Where it fails

- Control state: `projects/pulla-reddy/state/V06.json`
- Shared dependency: `projects/pulla-reddy/SHARED_PLANTER_SPEC.md` is not yet present
- Out-of-sequence package: `jarvis-review-test/V06/layer_03.png`

## Why this matters

The project rule is cumulative: `Layer N = approved Layer N-1 + exactly one new lighting circuit`.

Without an approved parent chain, Jarvis cannot verify previous-layer freeze, camera/architecture continuity, planter persistence, lighting hierarchy, or whether Layer 03 contains only the under-seater circuit. Approving this image in isolation would defeat the entire independent-review system.

## What must remain frozen

Nothing beyond the authoritative source is approved for V06 yet. Do not promote or reuse the submitted Layer 03 file as an approved parent.

## Required correction

1. Return V06 to the released initialisation task.
2. Establish the shared V02/V06 planter design and publish `projects/pulla-reddy/SHARED_PLANTER_SPEC.md` before either curved-seating lane advances.
3. Create V06 Layer 00 from the authoritative source with the shared planter present and all electric lighting off.
4. Publish the standard Layer 00 review package under `projects/pulla-reddy/review/V06/` containing `STATUS.md`, `manifest.json`, `SELF_QA.md`, a review-sized Layer 00 preview, and a source-versus-Layer-00 comparison.
5. Set V06 state to `waiting_for_chatgpt_review` and stop.
6. Only after Layer 00 is independently approved may V06 proceed through Layer 01, Layer 02, and then a new Layer 03 candidate.

## Acceptance criteria

- `SHARED_PLANTER_SPEC.md` exists and is consistent with V02.
- V06 Layer 00 is submitted through the standard review path.
- Camera, crop, perspective, architecture, ceiling grid, materials, furniture and products remain locked.
- Planter exists from Layer 00 onward but is unlit at Layer 00.
- No electric-lighting circuit is present in Layer 00.
- No downstream layer is treated as approved without its immediate parent being independently approved first.
