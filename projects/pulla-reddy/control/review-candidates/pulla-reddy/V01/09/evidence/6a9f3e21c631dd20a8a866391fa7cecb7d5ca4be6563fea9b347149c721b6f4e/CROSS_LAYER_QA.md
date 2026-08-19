# V01 Main Retail | Cross-Layer Continuity Audit

## Conclusion

**FAIL**

The exact approved master chain is hash-complete, dimensionally consistent at 1624 × 968, warm-light behavior is additive in Layers 01 and 03–06, no uniform global-exposure-lift signature was detected, and the Final V01 Composite is byte-for-byte identical to approved Layer 06.

However, Layer 02 fails the locked camera/crop/perspective continuity gate. Edge-registration analysis against approved Layer 01 finds a best alignment of **0 px horizontal, +1 px vertical**, not zero shift. The zero-shift edge correlation is `0.650410`; shifting Layer 02 by +1 px vertically raises it to `0.766104`. The exact-difference bounding box covers the full `1624 × 968` frame, `41.341207%` of pixels change by more than 3 luminance levels, and `16.470466%` become darker by more than 3 levels. Those broad negative deltas are consistent with coordinate misregistration and cannot be the physical contribution of an added wall-wash circuit.

Layer 01 anchor comparisons find the same `0,+1 px` best alignment for Layers 02, 03, 04, 05, 06 and Final. Therefore the earliest affected layer is Layer 02 and the shifted coordinate frame is inherited by every downstream render.

No approved image was rewritten. No repair was attempted.

## Earliest affected layer and dependency impact

- Earliest affected layer: **Layer 02**
- Defect: **+1 px vertical coordinate drift relative to approved Layer 01**
- Violated locks: camera, crop, perspective, exact parent-coordinate continuity, and freeze of prior-layer pixels outside physically necessary new-light interaction
- Directly affected candidate: `layer-02-wall-shelf-wall-wash-v3.png`
- Downstream dependants: Layers 03, 04, 05, 06 and `final-v01-composite.png`
- Communication-only asset: the approved concept sketch is not a pixel parent and is not part of the defective render ancestry
- Required control decision: JARVIS must choose the smallest safe repair and sequential re-approval path beginning at Layer 02

## Gate summary

| Gate | Result | Evidence |
|---|---:|---|
| Exact approved hashes present | PASS | Source, Layer 00, Layers 01–06, concept sketch and Final match the recorded SHA-256 values. |
| Dimensions and crop size | PASS | Every audited image is 1624 × 968. |
| Source → Layer 00 | PASS | Zero-shift is the best edge alignment. Scene-wide darkening is expected for the lights-off base. |
| Layer 00 → Layer 01 | PASS | Best shift `0,0`; `8.324831%` changed >3; `0%` negative >3; warm additive delta `R 45.156 / G 32.147 / B 12.210`; no uniform-lift signature. |
| Layer 01 → Layer 02 | **FAIL** | Best shift `0,+1`; full-frame diff; `41.341207%` changed >3; `16.470466%` negative >3. |
| Layer 02 → Layer 03 | PASS relative to its immediate parent | Best shift `0,0`; `7.106471%` changed >3; `0%` negative >3; warm additive shelf contribution. Parent is already downstream of the Layer 02 defect. |
| Layer 03 → Layer 04 | PASS relative to its immediate parent | Best shift `0,0`; `1.472744%` changed >3; `0%` negative >3; localized warm central contribution. Parent remains in shifted ancestry. |
| Layer 04 → Layer 05 | PASS relative to its immediate parent | Best shift `0,0`; `2.761458%` changed >3; `0%` negative >3; localized warm rear-hospitality contribution. Parent remains in shifted ancestry. |
| Layer 05 → Layer 06 | PASS relative to its immediate parent | Best shift `0,0`; `0.630267%` changed >3; `0%` negative >3; localized warm concealed under-seater contribution. Parent remains in shifted ancestry. |
| Layer 06 → Final | PASS | Byte-for-byte identical; SHA-256 `a059b10401f0e9b8c3d235630a3e2c43e5e70a3925022a05f65d71744d06bc30`; zero changed pixels. |
| Concept sketch ancestry | PASS | Approved concept sketch is verified by hash and explicitly excluded as a pixel parent. |
| Global exposure cheating | PASS for uniform-lift test | No transition exhibits the defined uniform whole-frame lift signature. Layer 02 nevertheless fails for coordinate drift and non-additive negative deltas. |
| Visible fixture / CCT / material / hierarchy visual screen | PASS, subject to ancestry failure | Labeled sheets show no newly introduced pendant, track, surface fixture, raw strip or luminous ceiling-dot condition. Added families read warm and retail hierarchy remains counter-led. |

## Transition 1 | Source → Layer 00

**PASS**

The full-frame luminance reduction is intentional and required to form the night base with proposed electric lighting off. The best edge-registration result is zero shift. Architecture remains legible at restrained ambient level and no new visible luminaire family appears.

## Transition 2 | Layer 00 → Layer 01

**PASS**

The change is localized to the front sweet-counter lighting family. The best alignment is `0,0`. Exact unchanged pixels remain `85.781269%`; the changed-pixel bounding box is `x 242, y 375, width 1257, height 552`. No pixel becomes darker by more than 3 luminance levels. The positive channel delta is strongly warm-biased (`R > G > B`) and counter glass clipping remains negligible.

## Transition 3 | Layer 01 → Layer 02

**FAIL**

The released warm wall-wash family is visible and the automated whole-frame uniform-lift test remains false, but the child is not in the exact approved Layer 01 coordinate frame. The best edge alignment is `0,+1`, and every later approved render inherits the same offset when compared with Layer 01. Because an added circuit cannot move the camera/crop or darken broad protected areas, this is an objective continuity failure.

## Transition 4 | Layer 02 → Layer 03

**PASS relative to immediate parent, downstream-invalidated**

Layer 03 keeps Layer 02's shifted frame and adds only a warm concealed shelf-integrated contribution. Immediate-parent alignment is `0,0`, negative >3 is `0%`, and no uniform global lift is detected. It cannot cure the upstream Layer 02 failure.

## Transition 5 | Layer 03 → Layer 04

**PASS relative to immediate parent, downstream-invalidated**

The new contribution is compact and centered on merchandise/circulation. Immediate-parent alignment is `0,0`; negative >3 is `0%`; unchanged exact pixels are `97.715695%`.

## Transition 6 | Layer 04 → Layer 05

**PASS relative to immediate parent, downstream-invalidated**

The added rear-hospitality family is warm and localized. Immediate-parent alignment is `0,0`; negative >3 is `0%`; unchanged exact pixels are `96.161592%`.

## Transition 7 | Layer 05 → Layer 06

**PASS relative to immediate parent, downstream-invalidated**

The concealed under-seater addition is the smallest cumulative delta. Immediate-parent alignment is `0,0`; negative >3 is `0%`; unchanged exact pixels are `99.200271%`.

## Transition 8 | Layer 06 → Final

**PASS**

The files are exactly identical in bytes, SHA-256, dimensions and pixels. The final introduces no lighting or visual change.

## Evidence files

- `cross-layer-metrics.json`: machine metrics, protected-region results, alignment search, anomaly binding and Layer 01 anchor comparisons
- `cross-layer-hash-decision-manifest.json`: every audited master bound to its exact hash and available approval/decision record
- `cross-layer-contact-sheet.png`: Source, Layer 00, Layers 01–06 and Final at identical crop and scale
- `cross-layer-pair-audit-board.png`: every adjacent parent-child pair, with the failed Layer 01 → Layer 02 gate highlighted
- `cross-layer-provenance.json`: approved-master selection and rejected-alternative exclusions

## Stop condition

Audit package published as `READY_FOR_JARVIS_REVIEW` with result **FAIL**. Contact-sheet/review-board production and presentation generation remain locked pending a candidate-bound JARVIS audit decision.
