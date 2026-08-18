# V01 Main Retail | Layer 01 Review Status

## State

Layer 00 is approved and remains the immutable parent. Layer 01 has been produced locally and submitted for ChatGPT review. Production is stopped at Layer 01. Layer 02 has not been generated.

## Authoritative local masters

- Approved parent: `D:/Codex/G Pulla Reddy Sweets/01_Views/V01_Main_Retail/layer-00-base-dark.png`
- Layer 01 candidate: `D:/Codex/G Pulla Reddy Sweets/01_Views/V01_Main_Retail/layer-01-front-display-counter-downlights.png`

Both files are 1624 x 968 pixels.

## Exact circuit introduced

Controlled deep-recessed 3000K downlighting serving only:

- the long glass sweet display counter on the right;
- the secondary front display/service counter on the left;
- physically necessary local spill immediately around those counters.

No other lighting family was activated.

## Autonomous corrections completed

1. The first lighting proposal contained ceiling apertures that read too brightly. These were corrected to tiny, dark, deep-recessed apertures with restrained warm inner glints.
2. The initial candidate darkened unrelated rear and shelf zones. The final master was rebuilt as a positive-only lighting contribution over approved Layer 00.
3. Camera and crop were normalized to the approved 1624 x 968 parent with zero detected alignment offset.
4. Protected rear, central-display and wall-shelf control regions were restored to exact Layer 00 pixels.

## Final QA evidence

- Best edge alignment offset: x=0, y=0.
- Negative RGB channel deltas relative to Layer 00: 0.
- Rear center, central display, left wall shelves and right wall shelves: exact pixel freeze in tested control regions.
- Right counter region mean luminance increase: 21.28.
- Left counter region mean luminance increase: 11.79.
- No Layer 02 work has started.

## Review assets

- `layer-01-front-display-counter-downlights-preview.jpg`
- `layer-00-vs-layer-01.jpg`
- `manifest.json`
- `SELF_QA.md`

## Requested review

Please approve Layer 01 or publish a correction instruction through `CURRENT_INSTRUCTION.md` and set `STATE.json` to `codex_action_required`.

## Known uncertainty

The proposed light appearance originated from a generative edit, but the final cumulative master applies only positive lighting contribution over the approved parent. Fine detail within the intentionally lit counter regions should still be independently reviewed, particularly glass reflection quality and preferred intensity.
