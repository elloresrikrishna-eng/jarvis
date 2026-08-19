# V01 Main Retail | Release Layer 04 Central Merchandise / Circulation

## Approved immutable parent

Layer 03 candidate:

`9c855ce50bea0032a17e0b6a230d7282dc1c078116dc0210b7fd33bcc525b6af`

Decision:

`jarvis-v01-l03-9c855ce5-approve-001`

Do not regenerate, reinterpret, rebalance or otherwise modify the approved Layer 03 parent.

## Required action

Create V01 Layer 04 from the exact approved Layer 03 parent only.

Add exactly one new lighting family:

**selective recessed 3000K lighting for the central freestanding merchandise display and only the minimum physically necessary adjacent circulation support.**

This layer must make the central merchandise legible without competing with the principal sweet counters or flattening the retail hierarchy.

## Design target

The completed cumulative hierarchy should remain:

1. principal sweet counters as the strongest visual destination;
2. wall merchandise and shelf compositions as the second tier;
3. central freestanding merchandise as a clearly readable third tier;
4. rear hospitality and background zones still calm and subordinate;
5. ceiling visually quiet.

The new central-lighting family must be visually clear enough to deserve its own presentation layer, but restrained enough that it never becomes the hero.

## Lighting character

- 3000K only.
- Deep recessed / visually quiet ceiling sources only.
- No pendant, track, surface or decorative luminaires.
- No visible glowing ceiling dots or bright apertures.
- Use believable beam direction and falloff corresponding to recessed source positions.
- Prefer focused merchandise readability over general floor brightness.
- Avoid broad ambient wash, haloing around the display, or a scene-wide gamma/exposure lift.
- Keep product colours believable and appetising.
- Keep floor spill narrow and physically credible.

## Absolute freeze

Preserve the exact approved Layer 03 parent except for physically unavoidable local interaction from the new central/circulation circuit.

Freeze:

- camera, crop, focal character and perspective;
- architecture and ceiling grid;
- counters, shelves, furniture, products and materials;
- approved Layer 01 sweet-counter downlighting;
- approved Layer 02 recessed wall-wash;
- approved Layer 03 concealed shelf-integrated lighting;
- all glass/reflection character associated with those approved layers;
- rear seating and hospitality zone;
- overall exposure and gamma.

Do not brighten wall shelves, counters, rear seating, ceiling or peripheral walls to make the new layer feel stronger.

## Self-correction before publication

Reject and iterate locally before publishing if the first attempt:

- makes the central display brighter than the sweet counters;
- creates obvious ceiling-dot fixtures;
- broadly brightens circulation or the full floor;
- changes the approved counter, wall-wash or shelf-light character;
- alters glass highlights unrelated to the central circuit;
- looks like painted-on or airbrushed glow;
- is too weak to communicate as a distinct presentation layer;
- introduces mixed-CCT contamination.

## Review package

Publish the exact Layer 04 candidate through the GitHub Actions binary review-artifact path.

The review package must include or reference:

- exact candidate SHA-256;
- exact approved Layer 03 parent SHA-256;
- parent decision ID;
- candidate preview;
- Layer 03 vs Layer 04 comparison;
- deterministic QA for dimensions, alignment, protected zones, global-exposure continuity and layer purity;
- manifest and SELF_QA;
- artifact ID and workflow run ID;
- independently verified remote candidate SHA-256 and provenance.

After remote retrievability is verified, set V01 to `READY_FOR_JARVIS_REVIEW` and STOP.

Do not begin Layer 05 until the exact Layer 04 candidate receives independent candidate-bound JARVIS approval.
