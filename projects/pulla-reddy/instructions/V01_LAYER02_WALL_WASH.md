# V01 Main Retail | Release Layer 02 Wall-Wash

V01 Layer 01 candidate `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217` is independently approved and is now the immutable parent for this task.

## Required action

Create V01 Layer 02 from the exact approved Layer 01 parent only.

Add exactly one new lighting family:

- deep-recessed 3000K wall-washer downlights serving all visible wall-mounted shelving compositions.

Do not add concealed shelf-integrated lighting yet. That is Layer 03.

## Design intent

The wall-wash must lift the wall-mounted merchandise enough to become the clear second visual tier after the sweet display counters, while preserving the counter-first retail hierarchy.

The effect must read as architectural wall-wash, not as generic wall brightening or ambient exposure lift.

## Hard locks

Preserve the approved Layer 01 exactly, including:

- camera, crop, focal character and perspective;
- architecture and timber ceiling grid;
- counters, products, shelves, furniture and materials;
- Layer 01 counter-downlight intensity, colour, beam character, reflections and shadow behaviour;
- central display and rear seating at their approved parent state except for physically unavoidable secondary bounce from the new wall-wash.

All added electric light remains 3000K. Use recessed, visually quiet sources only. No pendants, tracks, surface fittings or glowing ceiling-dot effect. No global exposure or gamma lift.

## Visual acceptance criteria

The candidate is review-worthy only if:

1. wall shelves become clearly more legible than in approved Layer 01 without competing with the sweet counters;
2. the wall-wash produces believable top-down modelling and soft falloff rather than a flat uniform wall lift;
3. ceiling apertures remain visually quiet and do not read as bright dots;
4. merchandise colours remain believable and warm without orange contamination;
5. the approved Layer 01 counter lighting remains visually unchanged;
6. no unrelated zone gains unexplained brightness, colour shift, reflection change or darkening;
7. the difference from Layer 01 is strong enough to communicate as a distinct presentation layer.

## Review output

Publish the exact candidate through the `jarvis-return-path-v1` GitHub Actions binary artifact path with:

- candidate PNG;
- manifest and provenance;
- exact candidate SHA-256;
- approved-parent SHA-256 bound to `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217`;
- workflow run ID and artifact ID;
- deterministic QA evidence for protected-region continuity and exposure integrity.

Set V01 to `READY_FOR_JARVIS_REVIEW` only after remote artifact retrievability and provenance are verified.

Stop there. Do not begin Layer 03 until Layer 02 receives an exact candidate-bound independent JARVIS approval.
