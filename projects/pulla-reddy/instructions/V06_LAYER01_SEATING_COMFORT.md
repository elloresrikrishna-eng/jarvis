# V06 Curved Seating Hero | Layer 01 Seating / Table Comfort

## Approved immutable parent

Repaired V06 Layer 00 candidate:

`a2c3f2bcb59ebf7e35b2c6e5842f1196227cc7ef6dad3bb6f6de469151ebcff3`

Decision:

`jarvis-v06-l00-a2c3f2bc-approve-001`

The approved Layer 00 includes the mandatory shared planter, physically present and electrically unlit. It is the immutable repaired parent.

## Required action

Create V06 Layer 01 from the exact approved Layer 00 parent only.

Add exactly one new lighting family:

**restrained deep-recessed 3000K table / seating comfort lighting over the visible hospitality zone.**

This is the hero seating view, so the light must make tables and seating feel comfortable and usable while retaining darkness between pools. It must not become a uniformly bright room.

## Lighting character

- 3000K only.
- Deep recessed / visually quiet ceiling sources.
- No visible fixture faces, glowing ceiling dots, pendants, tracks or decorative luminaires.
- Soft pools with believable beam geometry and falloff on tables, seats and immediate floor.
- Preserve some darkness between pools and toward the room edges.
- Faces are not present, so prioritize table surfaces and seating comfort without flattening the wall.
- The shared planter and foliage remain electrically unlit.
- Do not add under-seater lighting, shelf light, planter lighting or vertical architectural accents yet.

## Absolute freeze

Preserve exactly:

- camera, crop, perspective and focal character;
- ceiling grid, walls, built-in seater, tables, chairs and loose furniture;
- shared planter geometry, timber detailing, foliage cluster order, plant height, density and rhythm;
- materials and colours;
- Layer 00 residual ambient state outside physically plausible seating-light spill;
- overall exposure and gamma.

Do not brighten the rear wall broadly. Do not globally lift exposure.

## Acceptance criteria

- Tables and seating become comfortably legible through restrained local pools.
- Hospitality remains calm and warm, not theatrical or restaurant-stage bright.
- Planter stays unlit and visually secondary for now.
- Ceiling remains quiet and sources visually disappear.
- Pool edges and shadows are physically plausible.
- No unrelated region changes, camera drift or architecture/material change.
- Layer difference is presentation-legible while preserving darkness.

## Review package

Publish the exact candidate through the GitHub Actions binary review-artifact path with parent-versus-candidate comparison, focused seating/table crop, difference evidence, deterministic QA, manifest and SELF_QA. Verify exact parent/candidate hashes, provenance and remote retrievability.

Set V06 to `READY_FOR_JARVIS_REVIEW` and stop. Do not begin repaired Layer 02 under-seater lighting until the exact Layer 01 candidate receives independent candidate-bound JARVIS approval.
