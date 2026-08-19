# V01 Main Retail | Release Lighting Concept Sketch

## Approved render chain

V01 is independently approved through Layer 06.

Latest immutable cumulative render:

`a059b10401f0e9b8c3d235630a3e2c43e5e70a3925022a05f65d71744d06bc30`

Decision:

`jarvis-v01-l06-a059b104-approve-001`

Do not regenerate, rebalance or alter any approved render layer while creating the sketch.

## Required action

Create the Ashwamedha lighting concept sketch for V01 using the exact locked source camera, crop, perspective and architecture.

The sketch is a communication artifact, not a new lighting layer and not a redesign.

### Visual language

- Convert architecture and scene content into restrained charcoal / grayscale line-and-tone treatment.
- Indicate only the approved lighting families selectively in warm amber/orange.
- Keep the page quiet, premium, architectural and presentation-led.
- Preserve enough source detail that the client can immediately map the sketch to the approved render.
- Do not turn the image into a stylised illustration, cinematic artwork or generic AI concept image.

### Approved lighting families to communicate

1. Principal sweet display-counter recessed downlighting.
2. Recessed wall-wash serving wall-mounted shelving compositions.
3. Concealed integrated shelf lighting to the wall-mounted shelves.
4. Selective central-merchandise / circulation support.
5. Restrained rear seating-comfort downlighting.
6. Concealed under-seater lighting to the visible rear built-in banquette.

The sketch must not invent any seventh lighting family, decorative fixture, pendant, track, surface fitting, raw LED strip, architectural feature or lighting effect.

## Hierarchy

The sketch should visually explain the same approved hierarchy as the render chain:

1. sweets / principal front display strongest;
2. wall merchandise and shelves second;
3. central merchandise third;
4. rear seating comfort fourth;
5. under-seater support subtle and subordinate;
6. ceiling visually quiet.

Use amber emphasis sparingly enough that the drawing still reads as a design sketch rather than a heatmap.

## Absolute locks

Preserve exactly:

- source camera, focal character, crop and perspective;
- architecture and ceiling grid;
- counters, shelves, central display, furniture, products and material boundaries;
- spatial relationships and proportions;
- approved lighting locations and intended beam/effect logic.

Do not modify the approved Layer 06 render itself.

## Self-correction before publication

Reject and iterate locally before publication if the sketch:

- changes camera, crop, perspective or geometry;
- omits any approved lighting family that is meaningfully visible in V01;
- invents lighting not present in the approved chain;
- makes the whole image amber instead of selectively annotating light;
- makes fixture bodies or ceiling apertures visually dominant;
- becomes too stylised, painterly, cinematic or diagrammatic to map cleanly to the source view;
- is so faint or cluttered that the lighting sequence is difficult to understand.

## Review package

Publish the exact concept-sketch image through the GitHub Actions binary review-artifact path with a dedicated V01 concept-sketch task/layer ID.

The review package must include or reference:

- exact sketch candidate SHA-256;
- approved Layer 06 render SHA-256 `a059b10401f0e9b8c3d235630a3e2c43e5e70a3925022a05f65d71744d06bc30`;
- approval decision `jarvis-v01-l06-a059b104-approve-001`;
- authoritative V01 source image reference;
- candidate preview;
- source-versus-sketch comparison;
- short mapping from each amber annotation/effect to the six approved lighting families;
- deterministic geometry/crop/alignment evidence where applicable;
- manifest, provenance and SELF_QA;
- artifact ID and workflow run ID;
- independently verified remote candidate SHA-256.

After remote retrievability and provenance are verified, set V01 to `READY_FOR_JARVIS_REVIEW` for the concept sketch and STOP.

Do not begin the Final V01 Composite task until the exact concept-sketch candidate receives independent JARVIS approval.
