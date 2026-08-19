# V01 Main Retail | Layer 02 Coordinate-Continuity Repair

## Control decision

The V01 Cross-Layer Continuity Audit candidate `6a9f3e21c631dd20a8a866391fa7cecb7d5ca4be6563fea9b347149c721b6f4e` is rejected as a completion gate under decision:

`jarvis-v01-l09-6a9f3e21-reject-001`

The audit proves that the current V01 render ancestry first violates an absolute scene-continuity lock at Layer 02.

## Repair root

The exact approved Layer 01 parent is the only valid repair root:

- file: `layer-01-front-display-counter-downlights-v4.png`
- SHA-256: `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217`
- approval: `jarvis-v01-l01-bb0eda1c-approve-001`

Do not alter or regenerate Layer 01.

## Defective historical Layer 02

The previously approved Layer 02 remains immutable historical evidence but is no longer a valid cumulative parent:

- file: `layer-02-wall-shelf-wall-wash-v3.png`
- SHA-256: `fc47cfc6a1ccbaac2e8103d2b013036716f43395fba0a0c8a393f797dcf1599e`

Audit evidence shows:

- dimensions remain `1624 x 968`;
- best registration against approved Layer 01 is `0 px horizontal, +1 px vertical` rather than `0,0`;
- zero-shift edge correlation is `0.650410`;
- applying the +1 px vertical registration raises correlation to `0.766104`;
- `41.341207%` of pixels change by more than 3 luminance levels;
- `16.470466%` become darker by more than 3 levels;
- the exact-difference bounding box spans the full frame;
- Layers 03, 04, 05, 06 and Final inherit this shifted coordinate frame.

JARVIS independently retrieved the exact Layer 01 and Layer 02 GitHub Actions artifacts, verified both candidate SHA-256 values, and repeated registration analysis. The one-pixel vertical mismatch was independently reproduced.

## Required action

Create a NEW repaired Layer 02 candidate from the exact approved Layer 01 parent only.

Add exactly one lighting family:

**controlled deep-recessed 3000K wall-washer downlighting serving the visible wall-mounted shelf compositions.**

The old Layer 02 may be used only as a visual design reference for wall-wash distribution, warmth, hierarchy and restraint. Do not use it as a pixel parent.

Do not simply shift the completed defective Layer 02 raster and invent or crop edge pixels. Rebuild the wall-wash contribution on the exact approved Layer 01 coordinate grid.

## Visual intent to preserve

The repaired Layer 02 should retain the useful design character already achieved:

- the principal sweet display counter remains the first visual destination;
- wall merchandise becomes a clear but secondary vertical layer;
- wall-wash remains selective rather than blanket ambient illumination;
- shelf walls gain depth and merchandise legibility without stealing hierarchy from the sweets;
- added electric light reads consistently at 3000K, warm but not orange;
- the ceiling remains visually quiet;
- no visible pendant, track, surface fitting or glowing ceiling aperture appears;
- glass remains readable and free from new bloom or harsh white reflection blobs.

## Absolute freezes

Preserve exactly from approved Layer 01:

- camera position, crop, perspective, focal character and every image coordinate;
- architecture, ceiling grid, walls, counters, shelves, joinery and doors;
- furniture, products, materials and colours;
- Layer 01 counter-downlight intensity, beam character, colour, shadow and reflection behaviour;
- all unrelated zones except physically credible wall-wash spill or bounce.

No global exposure, gamma, contrast or colour lift is permitted.

## Deterministic acceptance gates

Before publication, prove all of the following:

1. Candidate dimensions are exactly `1624 x 968`.
2. Best edge-registration against approved Layer 01 is exactly `dx=0, dy=0` and zero-shift is the registration optimum.
3. No whole-frame coordinate drift or crop shift exists.
4. Broad negative deltas outside physically credible wall-wash interaction are absent.
5. Protected unrelated regions remain materially frozen to Layer 01.
6. The new contribution is localized to the intended wall-shelf/wall-wash zones plus plausible secondary bounce.
7. No uniform scene-wide exposure-lift signature is present.
8. The candidate contains only the Layer 01 parent plus the released wall-wash family.

If any of these fail, correct the candidate autonomously before publication.

## Review package

Publish the repaired Layer 02 through the content-addressed GitHub Actions binary review path.

Include:

- candidate master and review-sized preview;
- exact approved Layer 01 parent versus repaired Layer 02 side-by-side;
- difference / registration evidence;
- updated `STATUS.md`;
- updated `manifest.json`;
- updated `SELF_QA.md`;
- deterministic alignment and protected-region metrics;
- candidate SHA-256, artifact ID, workflow run ID and provenance verification.

Then set V01 to `READY_FOR_JARVIS_REVIEW` and stop.

## Downstream lock

Do not regenerate or begin Layer 03 until this repaired Layer 02 receives exact candidate-bound independent JARVIS approval.

The historical Layers 03-06 and Final remain reference evidence only. After repaired Layer 02 approval, each downstream layer must be rebuilt sequentially from the newly approved immediate parent and independently reviewed before progression.

The approved concept sketch remains communication-only and is never a pixel parent.

V01 contact-sheet/review-board production and presentation generation remain locked until the repaired chain is independently approved through Final and a fresh cross-layer continuity audit passes.
