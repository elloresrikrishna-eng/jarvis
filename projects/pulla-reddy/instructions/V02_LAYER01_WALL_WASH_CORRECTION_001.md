# V02 Curved Seating | Layer 01 Wall-Wash Correction 001

## Decision binding

Rejected candidate:

`af3045bc9902183b15c7dd43878f87c5586b51cf2fc743317753b8d0564da619`

Rejected under:

`jarvis-v02-l01-af3045bc-reject-001`

Approved immutable parent remains:

`c0db62b789677bef3390003a97230c6a442018005d1f6c9b73f1bebd20851540`

Do not advance to integrated shelf lighting. Rebuild the same Layer 01 task from the exact approved Layer 00 parent only.

## What failed

The candidate passes deterministic continuity checks, but it fails the independent visual-design gate.

At normal presentation scale, the Layer 01 change is too weak to read as a meaningful architectural-lighting layer. The parent and candidate are nearly indistinguishable in the full view.

The added wall-wash also reads as two faint localized oval/spot patches centred behind the shelf compositions. It does not yet read as a believable recessed wall-washer distribution with vertical continuity from the ceiling plane down the shelf walls.

This conflicts with the intended effect because the released circuit is specifically a clear but restrained recessed wall-wash. It must visibly model the shelf/wall compositions without becoming retail-bright, and it must be presentation-legible enough to deserve its own cumulative layer.

## Required correction

1. Start from the exact approved Layer 00 parent only.
2. Increase the 3000K wall-wash contribution on both visible wall-mounted shelf compositions enough that the effect is clearly visible in the full-frame presentation view.
3. Replace the current isolated glow-island character with a broader, vertically coherent wall-washer distribution. The wash should feel physically sourced from deep-recessed ceiling wall-washers and fall naturally down the wall/shelf composition.
4. Keep beam transitions soft and believable. Avoid perfectly circular or oval painted blobs, hard-edged masks, or airbrushed-looking patches.
5. Allow the wall-wash to gently improve shelf/product legibility, but do not activate concealed integrated shelf lighting yet.
6. Keep the hospitality seating and planter deliberately darker than the shelf compositions at this stage so later seating/table comfort lighting still has room to become the hospitality hero.
7. Keep all ceiling apertures visually quiet. No glowing dots, bright fixture faces, tracks, pendants or surface luminaires.
8. Any floor or adjacent-surface contribution must be only low-energy, physically plausible secondary spill from the wall-wash. Do not add a separate floor pool or circulation circuit.

## Absolute freeze

Preserve exactly:

- camera, crop, focal character and perspective;
- ceiling grid and all architecture;
- walls, door, glazing, counters, shelves, tables, chairs and loose furniture;
- shared V02/V06 planter geometry, timber detailing, foliage cluster order, height, density and rhythm;
- all materials and colours;
- approved Layer 00 residual ambient state outside physically plausible wall-wash spill;
- overall exposure and gamma.

The planter remains physically present and completely unlit.

Do not activate:

- integrated shelf lighting;
- planter lighting;
- under-seater lighting;
- seating/table comfort lighting;
- circulation lighting;
- any unrelated circuit.

## Acceptance criteria

The next candidate may be submitted only when all of the following are true:

- The wall-wash is clearly distinguishable from Layer 00 at normal presentation scale without requiring a difference map to notice it.
- Both visible shelf-wall compositions are softly and deliberately modelled vertically rather than receiving isolated glow patches.
- The effect reads as recessed architectural wall-wash, not painted image brightening.
- Shelf products become more readable, but no concealed shelf-integrated source is active yet.
- Ceiling remains visually quiet with no visible luminous fixture faces.
- Seating and planter remain darker and calmer than the shelf compositions.
- No unrelated zone activation, darkening, camera drift, architecture change, material change, colour shift, exposure lift or gamma change occurs.
- Deterministic QA passes against the exact approved Layer 00 parent.

## Required review package

Publish a fresh revisioned Layer 01 candidate through the GitHub Actions binary review-artifact path with:

- exact approved-parent SHA and new candidate SHA;
- full-frame candidate preview;
- approved-parent versus candidate comparison;
- focused shelf crop showing both wall-wash zones where practical;
- difference evidence;
- deterministic QA;
- manifest;
- SELF_QA.

Verify provenance and remote retrievability, set V02 to `READY_FOR_JARVIS_REVIEW`, and stop.

Do not begin Layer 02 until the new exact Layer 01 candidate receives independent candidate-bound JARVIS approval.
