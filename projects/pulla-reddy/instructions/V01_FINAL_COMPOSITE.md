# V01 Main Retail | Release Final Composite

## Approved prerequisites

V01 is independently approved through:

- Layer 06 cumulative render: `a059b10401f0e9b8c3d235630a3e2c43e5e70a3925022a05f65d71744d06bc30`
- Layer 06 decision: `jarvis-v01-l06-a059b104-approve-001`
- Concept sketch: `0b0e4bacdf2961335fe1d82cae6d86f9fc0ce3511ad6fa5e16fcf82c8feaeb78`
- Concept-sketch decision: `jarvis-v01-l07-0b0e4bac-approve-001`

The concept sketch is a communication artifact only. It is not a render parent.

## Required action

Create the Final V01 Composite as task/layer ID `08`.

The final render must be exactly the last independently approved cumulative render. Do not regenerate, relight, rebalance, denoise, sharpen, recolour, crop, rescale or otherwise reinterpret the scene.

Preferred method: copy the exact approved Layer 06 PNG byte-for-byte into the final-master filename so the final composite SHA-256 remains:

`a059b10401f0e9b8c3d235630a3e2c43e5e70a3925022a05f65d71744d06bc30`

If an export operation would change the hash, do not perform it unless technically unavoidable. Never trade provenance integrity for cosmetic re-exporting.

## Absolute locks

Preserve exactly:

- camera, focal character, crop and perspective;
- architecture and ceiling grid;
- counters, shelves, central merchandise, rear seating furniture and products;
- materials, colours and glass/reflection character;
- Layer 01 counter downlighting;
- Layer 02 shelf wall-wash;
- Layer 03 concealed shelf-integrated light;
- Layer 04 central merchandise/circulation support;
- Layer 05 rear seating comfort;
- Layer 06 concealed under-seater support;
- 3000K apparent electric-light character;
- existing exposure and gamma.

No seventh lighting family. No additional fixture effects. No global lift. No presentation treatment baked into the render.

## Review publication

Publish the exact Final V01 Composite through the GitHub Actions binary review-artifact path using task/layer ID `08`.

The review package must include:

- exact final candidate SHA-256;
- explicit comparison against approved Layer 06 SHA-256;
- confirmation whether the file is byte-for-byte identical;
- approved Layer 06 decision ID;
- approved concept-sketch decision ID;
- artifact ID and workflow run ID;
- generated provenance and remote candidate verification;
- final continuity note confirming no unlisted lighting or exposure change.

After remote retrievability and provenance are verified, set V01 to `READY_FOR_JARVIS_REVIEW` and STOP.

Do not begin the cross-layer continuity audit until the exact Final V01 Composite receives candidate-bound independent JARVIS approval.
