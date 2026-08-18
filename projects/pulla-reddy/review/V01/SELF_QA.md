# V01 Layer 01 Rework | Self-QA

This document records production QA only. It does not substitute for the independent reviewer decision required by `REVIEWER_RUBRIC.md`.

## Hard-lock checks

| Check | Result | Evidence |
|---|---|---|
| Dimensions | PASS | Layer 00 and candidate are both 1624 x 968 |
| Camera, perspective and crop | PASS | Candidate is composited directly on the approved Layer 00 pixel grid |
| Architecture and ceiling grid | PASS | Ceiling is exact Layer 00, maximum pixel delta 0 |
| Shelves and unrelated walls | PASS | Protected shelf regions restored to exact Layer 00 pixels |
| Central merchandise display | PASS | Protected region maximum pixel delta 0 |
| Rear seating | PASS | Protected region maximum pixel delta 0 |
| Previous-layer purity | PASS | Layer 00 is the sole parent; no other circuit is present |
| Negative pixel deltas | PASS | 0 negative RGB channel deltas |
| Global exposure cheat | PASS | Illumination is limited to counter-localized masks and restrained adjacent spill |
| Added CCT | PASS | Positive contribution follows a consistent warm 3000K channel balance |
| Visible fixture bodies | PASS | No ceiling apertures or fixture faces are introduced |
| Output clipping | PASS | 0 output channels at clipping threshold in the final candidate |
| Glass readability | PASS | Display glass remains transparent with no white blobs, bloom, or duplicated reflections |

## Hierarchy checks

- Right sweet counter mean luminance increase: **+15.156**.
- Left-front counter mean luminance increase: **+9.077**.
- Ceiling, central display, and rear seating protected regions: **exactly unchanged**.
- The right counter is intentionally the dominant hero; the left display is a secondary member of the same circuit.

## Rework corrections

The first rework attempt was rejected internally before publication because floor spill was too broad and the light was too orange.

The submitted v4 candidate:

1. narrows the contribution to overlapping counter-localized beam footprints;
2. lowers secondary floor spill;
3. reduces red dominance while preserving a warm 3000K appearance;
4. suppresses all luminous ceiling-dot behavior;
5. restores protected non-counter zones to exact Layer 00 pixels;
6. preserves glass transparency and avoids clipped product highlights.

## Known limitation

Pixel statistics prove continuity and layer purity, not presentation quality. Independent ChatGPT visual/design review is still required before Layer 01 can become an approved parent.
