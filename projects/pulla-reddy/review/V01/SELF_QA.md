# V01 Layer 05 | Self QA

Candidate SHA-256: eda764d05c8880522a22098f653f234e54e4194c859a718f026d8040e4b45065

Approved parent SHA-256: 58553357484f01018a2d8a3929c3c662d67b3fbc21143847bb255d1c7d2ed837

## PASS

- Exact approved Layer 04 parent hash verified.
- Candidate and parent are both 1624 x 968 with identical camera and crop.
- Only the two rear table/seating zones and their tight local floor support changed.
- Changed pixels outside the permitted rear zones: 0.
- Rear-left table/seating mean luminance shift: +5.0039.
- Rear-right table/seating mean luminance shift: +6.1532.
- Rear local-floor mean luminance shift: +1.6851.
- Global mean luminance shift: +0.253448, caused only by the localized new circuit.
- Left and right counters: 0.0 shift.
- Left and right wall-shelf lighting: 0.0 shift.
- Central merchandise and its approved floor pool: 0.0 shift.
- Ceiling: 0.0 shift and no visible aperture introduced.
- Foreground floor: 0.0 shift.
- Negative channel deltas: 0.
- Target-region clipping: 0 pixels.
- 3000K warm-white character only.
- Principal sweet counters remain first tier, wall shelves second, central merchandise third, rear hospitality fourth.

## Production judgment

The image-generation draft was not published directly. Its broad rear contribution was localized onto the exact approved parent. Layer 05 v2 was rejected because 44 feather-boundary pixels touched protected shelf/counter boundaries. Final v3 tightens those mask edges and leaves every protected retail family unchanged.

Deterministic QA is Gate 1 only. Independent JARVIS visual review remains mandatory.