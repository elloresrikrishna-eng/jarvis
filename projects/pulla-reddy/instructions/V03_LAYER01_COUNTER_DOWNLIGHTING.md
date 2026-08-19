# V03 Reverse Retail | Release Layer 01 Counter Downlighting

## Approved immutable parent

Layer 00 candidate:

`a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a`

Decision:

`jarvis-v03-l00-a6056c69-approve-001`

This approved Layer 00 is the locked all-proposed-electric-lighting-off baseline. Do not regenerate or reinterpret it.

## Required action

Create V03 Layer 01 from the exact approved Layer 00 parent only.

Add exactly one new lighting family:

**controlled deep-recessed 3000K downlighting over the visible sweet display counter(s).**

The sweets and front retail display must become the first visual destination while the rest of the store remains substantially at Layer 00.

## Design target

- Sweets read rich, fresh and appetising.
- Counter lighting is clearly intentional and architectural, not a global image lift.
- Beam pools are controlled with believable direction and falloff.
- Glass remains transparent and readable.
- Counter highlights stay premium, not harsh or jewellery-store cold.
- The ceiling remains visually quiet.
- Wall shelves, central merchandise, circulation and seating remain at the Layer 00 visual state except for physically unavoidable local spill.

## Lighting character

- 3000K only.
- Deep recessed / visually quiet sources only.
- No pendant, track, surface or decorative luminaires.
- No glowing ceiling dots or oversized luminous apertures.
- No broad ambient wash.
- No scene-wide exposure/gamma lift.
- Warmth must not become orange or muddy.
- Avoid clipped white counter surfaces and ugly hot spots in display glass.
- Preserve believable material differences between sweets, glass, white counters, dark timber, brass, cream walls and terracotta/red flooring.

## Absolute freeze

Preserve exactly:

- camera, crop, focal character and perspective;
- architecture and ceiling grid;
- counters, shelves, furniture, products and materials;
- Layer 00 residual environmental light;
- wall shelves and their unlit state;
- central merchandise and seating;
- overall exposure and gamma.

Do not use brighter shelves, walls, circulation or seating to make the counter lighting feel stronger.

## Self-correction before publication

Reject and iterate locally before publishing if the first attempt:

- looks flat or diffuse;
- creates ceiling-dot fixtures;
- makes the sweets overly orange, washed out or clipped;
- creates white reflection blobs, fake glowing glass edges or duplicated reflections;
- brightens unrelated areas;
- lifts the full scene;
- makes the counter effect too weak to communicate in a layered presentation.

## Review package

Publish the exact Layer 01 candidate through the GitHub Actions binary review-artifact path.

The review package must include or reference:

- exact candidate SHA-256;
- exact approved Layer 00 parent SHA-256;
- parent decision ID;
- candidate preview;
- Layer 00 vs Layer 01 comparison;
- deterministic QA for dimensions, alignment, protected zones, global-exposure continuity and layer purity;
- glass/highlight checks;
- manifest and SELF_QA;
- artifact ID and workflow run ID;
- independently verified remote candidate SHA-256 and provenance.

After remote retrievability is verified, set V03 to `READY_FOR_JARVIS_REVIEW` and STOP.

Do not begin the V03 wall-wash layer until this exact Layer 01 candidate receives independent candidate-bound JARVIS approval.
