# V01 Layer 04 | Self QA

Candidate SHA-256: `58553357484f01018a2d8a3929c3c662d67b3fbc21143847bb255d1c7d2ed837`

Approved parent SHA-256: `9c855ce50bea0032a17e0b6a230d7282dc1c078116dc0210b7fd33bcc525b6af`

## PASS

- Exact approved parent hash verified.
- Candidate and parent are both `1624 x 968` with identical camera and crop.
- Only the central merchandise and tight adjacent-floor zones changed.
- Changed pixels outside the two permitted zones: `0`.
- Central merchandise mean luminance shift: `+4.7258`.
- Adjacent floor mean luminance shift: `+2.4627`.
- Global mean luminance shift: `+0.141173`, caused only by the localized new circuit.
- Left and right counters: `0.0` shift.
- Left and right wall-shelf lighting: `0.0` shift.
- Ceiling: `0.0` shift and no visible aperture introduced.
- Rear seating: `0.0` shift.
- Foreground floor: `0.0` shift.
- Negative channel deltas: `0`.
- Target-region clipping: `0` pixels.
- 3000K warm-white character only.
- Principal sweet counter remains first tier, wall shelves second, central merchandise third.

## Production judgment

The first localized candidates were not published. The floor ellipse was tightened to avoid the left counter, and the contribution was clamped below the protected rear-seating boundary. The final v4 is restrained but clearly legible in sequence and contains no global exposure cheat.

Deterministic QA is Gate 1 only. Independent JARVIS visual review remains mandatory.
