# G Pulla Reddy Sweets, HSR | View 01 Production Task

## Objective
Build the first complete layered lighting sequence for the main retail view. This view becomes the golden reference for all later views.

## Source-view reading
The view looks through the main retail floor. The long sweet display counter dominates the right side, with a secondary counter on the left, central circular merchandise displays, wall shelves on both sides and seating visible toward the rear. The timber ceiling grid is visually strong and must not become cluttered with visible fittings.

## Naming
Create the first actual view folder in the local project using the existing folder-creation workflow. Keep every resulting image directly inside that one view folder.

Recommended semantic name: `V01_Main_Retail`.

## Permanent scene requirements before Layer 00

- Preserve source camera and architecture exactly.
- Remove / avoid any visible non-recessed light fixtures if present or accidentally introduced.
- If any portion of the curved seating planter intervention is visible in this camera, include it from Layer 00. If the curved seating zone is not meaningfully visible, do not force planter geometry into this view.
- Do not change products, shelves, counters, furniture or ceiling-grid design.

## Layer sequence

### Sketch
Create one Ashwamedha-style lighting concept sketch before the rendered sequence.

Requirements:
- architectural scene rendered as restrained charcoal / grayscale sketch;
- lighting additions and beams indicated selectively in warm orange / amber;
- do not alter camera or architecture;
- show only the intended lighting families clearly enough to communicate design intent.

### Layer 00 | Night base
Create a true night-state base image:

- all proposed electric lighting OFF;
- no glowing shelves;
- no lit counters;
- no seat underglow;
- no wall-washer effects;
- no global brightening;
- retain just enough physically believable residual/environmental visibility to read the architecture.

This becomes the immutable base.

### Layer 01 | Front sweet display counter lighting
Add only controlled recessed downlighting above the principal front sweet display counter(s).

Intent:
- sweets become the strongest visual priority;
- high-quality 3000K appearance;
- controlled beam placement;
- avoid harsh glare or obvious reflected luminaire hot spots in counter glass;
- do not brighten shelves or architecture beyond unavoidable realistic spill.

Everything from Layer 00 remains frozen.

### Layer 02 | Wall shelf wall-wash
Add only recessed wall-washer downlights serving the wall-mounted shelving compositions.

Intent:
- softly model cream walls and timber shelves;
- improve vertical merchandise readability;
- no visible fixtures;
- avoid uniform floodlighting of the whole wall.

Layer 01 remains unchanged.

### Layer 03 | Concealed shelf-integrated light
Add concealed integrated light to every wall-mounted shelf visible in this view, following the office Minions display-shelf intent.

Intent:
- hidden source;
- soft shelf/product glow;
- no visible LED dots or raw strip lines;
- 3000K;
- integrated light supplements, rather than replaces, the wall-wash layer.

Layers 01 and 02 remain frozen.

### Layer 04 | Central merchandise / circulation emphasis
Add the minimum recessed lighting necessary to give the central freestanding displays and circulation zone visual legibility.

Intent:
- selective pools, not blanket ambient illumination;
- retail hierarchy must remain product-first;
- do not let the ceiling become visually dominant.

Previous layers remain frozen.

### Layer 05 | Rear seating comfort
Add only the recessed 3000K lighting needed to give the visible rear seating area comfortable local illumination.

Intent:
- softer than the sweet-counter lighting;
- calm hospitality character;
- no pendants or decorative fittings.

Previous layers remain frozen.

### Layer 06 | Under-seater glow, if built-in seater is visible
If a built-in seater is meaningfully visible in this camera, add concealed under-seater lighting only.

If there is no meaningful built-in seater in frame, omit this layer and renumber subsequent layers accordingly.

Intent:
- restrained floating glow;
- no exposed strip source;
- 3000K;
- no global exposure change.

### Final render
The final render is simply the last cumulative layer with no extra unlisted lighting or exposure manipulation.

## Quality gates

Before marking View 01 complete, verify:

- pixel-level camera/crop consistency as far as the production method allows;
- architecture and material consistency;
- all lighting at 3000K;
- no visible pendant, track or surface light added;
- no previous lighting layer materially changed in later images;
- no fake global exposure jump;
- wall shelves have both ceiling wall-wash and hidden shelf-integrated light;
- front counter lighting clearly prioritises sweets;
- glass reflections remain believable;
- final scene still looks like the original G Pulla Reddy interior, not a redesign.

## Review package to publish to Jarvis

After producing the sequence locally, publish a lightweight review package into the `jarvis` GitHub repo under:

`projects/pulla-reddy/review/V01/`

Include:

1. `STATUS.md` with exact local file paths and completion notes;
2. `manifest.json` listing each asset filename, layer number, purpose, dimensions and creation status;
3. one reasonably sized contact-sheet image showing Sketch, Layer 00 through final in sequence, if the workflow can commit it cleanly;
4. `SELF_QA.md` reporting pass/fail against every quality gate above;
5. any unresolved problems or trade-offs.

Do not claim completion unless the outputs genuinely exist in the local project.

## Stop condition

Do not start View 02. Stop after View 01 and its review package are complete. View 01 must be reviewed and approved as the golden reference first.
