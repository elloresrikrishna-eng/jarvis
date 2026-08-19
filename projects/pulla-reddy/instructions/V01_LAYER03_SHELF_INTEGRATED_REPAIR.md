# V01 Main Retail | Repaired Layer 03 Shelf-Integrated Lighting

## Authoritative parent

Use only the independently approved repaired Layer 02 candidate:

`layer-02-wall-shelf-wall-wash-v4.png`

SHA-256:

`c6bb3f56cd3f2f4372c2aaf8d5ada39bbc7b156c270e46a5235498fd41dd7d27`

Approval decision:

`jarvis-v01-l02-c6bb3f56-approve-002`

Do not use any historical Layer 03-06 or Final raster as a pixel parent. Those files remain immutable evidence only.

## Required action

Build a NEW repaired V01 Layer 03 from the exact repaired Layer 02 parent.

Add exactly one new lighting family:

**concealed integrated 3000K shelf lighting to all visible wall-mounted shelves.**

This must supplement the approved wall-wash, not replace it.

## Design intent

The shelf lighting should make the merchandise feel gently self-presenting within the wall compositions while preserving the overall commercial hierarchy:

1. sweet counters remain the strongest visual destination;
2. wall merchandise becomes the clear second tier;
3. central merchandise remains lower;
4. rear seating remains calm and dark at this stage;
5. the ceiling remains visually quiet.

The integrated shelf-light character should resemble the intended office Minions display-shelf language: hidden source, soft product/shelf glow, premium restraint, no obvious strip-light aesthetic.

## Visual acceptance criteria

- all visible wall-mounted shelf compositions receive integrated shelf light where physically plausible;
- source remains completely concealed;
- no raw LED strip line;
- no visible LED dots;
- no glowing shelf-edge ribbon;
- no decorative luminaire appearance;
- merchandise gains localized warmth and readability without flattening product colour or making bags/boxes look washed out;
- shelf lighting reads distinctly from the approved wall-wash, but both effects work together naturally;
- right and left shelf compositions remain balanced without becoming equal in brightness to the sweet counters;
- no broad wall or scene-wide exposure lift;
- no cool or mixed-CCT contamination;
- no new glare or reflected hot spots in the sweet-counter glass;
- no change to central merchandise, rear seating or under-seater zones except physically unavoidable tiny bounce;
- the new layer is visually legible enough to justify its own presentation step.

## Absolute freezes

Preserve exactly:

- 1624 x 968 pixel dimensions;
- camera, crop, focal character and perspective;
- architecture, ceiling grid, counters, shelves, furniture, products, materials and colours;
- approved Layer 01 counter downlighting;
- repaired Layer 02 wall-wash intensity, beam character, colour and spatial footprint;
- all protected non-shelf regions.

The repaired coordinate grid is authoritative. Best registration against the repaired Layer 02 parent must remain `dx=0, dy=0`.

Do not use global exposure, gamma, contrast or colour-grading changes.

## Self-correction before publication

Reject and iterate internally if the first attempt shows any of the following:

- visible strip source or LED dots;
- shelf edges glowing more strongly than merchandise;
- excessive orange cast;
- shelves becoming brighter than sweet counters;
- wall-wash being altered or replaced;
- ceiling brightening;
- unrelated zones changing;
- camera/crop drift;
- any negative/darkening signature inconsistent with adding this lighting family.

## Review package

Publish the exact candidate through the GitHub Actions binary review-artifact path with:

- updated `STATUS.md`;
- updated `manifest.json`;
- updated `SELF_QA.md`;
- review-sized candidate preview;
- repaired Layer 02 versus new Layer 03 side-by-side;
- difference image;
- deterministic QA evidence;
- generation provenance;
- exact candidate SHA-256, artifact ID and workflow run ID.

Verify remote retrievability and provenance.

Then set V01 to `READY_FOR_JARVIS_REVIEW` and STOP.

Do not begin repaired Layer 04 until the exact Layer 03 candidate receives candidate-bound independent JARVIS approval.
