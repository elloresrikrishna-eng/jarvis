# V01 Main Retail | Connector-Readable Visual Evidence Request

V01 remains frozen at the reworked Layer 01 v4 review gate. Layer 00 is the only approved parent. Do not change the render and do not start Layer 02.

The current blocker is review transport, not production quality. The independent reviewer must see the actual pixels before deciding APPROVE or CORRECT.

## Authoritative files

- Approved parent: `D:/Codex/G Pulla Reddy Sweets/01_Views/V01_Main_Retail/layer-00-base-dark.png`
- Candidate: `D:/Codex/G Pulla Reddy Sweets/01_Views/V01_Main_Retail/layer-01-front-display-counter-downlights-v4.png`
- Source: `D:/Codex/G Pulla Reddy Sweets/01_Views/V01_Main_Retail/source-view-01-original.jpg`

Do not alter any of these files.

## Required action

Create a tiny connector-readable evidence pack under:

`projects/pulla-reddy/review/V01/connector/`

Generate these JPEG derivatives directly from the authoritative files:

1. `parent-full-480.jpg`
2. `candidate-full-480.jpg`
3. `parent-right-counter-crop-512.jpg`
4. `candidate-right-counter-crop-512.jpg`
5. `parent-left-counter-crop-512.jpg`
6. `candidate-left-counter-crop-512.jpg`
7. `parent-ceiling-glass-crop-512.jpg`
8. `candidate-ceiling-glass-crop-512.jpg`

For every derivative:

- preserve aspect ratio;
- no colour grading, exposure change, sharpening, denoise, relighting, retouching or annotation;
- resizing and JPEG compression only;
- crop pairs must use identical crop coordinates;
- target file size `<= 10 KB` each where practical, hard maximum `15 KB` each;
- if necessary reduce JPEG quality before reducing dimensions below the specified nominal width;
- do not upscale a crop beyond its native pixel dimensions.

Create `projects/pulla-reddy/review/V01/connector/TRANSPORT_MANIFEST.json` containing for every file:

- filename;
- source authoritative file;
- crop coordinates in source pixels, or `full_frame`;
- output width and height;
- byte size;
- SHA-256;
- JPEG quality used.

Also record the authoritative parent and candidate SHA-256 values in the manifest. The candidate SHA must remain `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217`.

## Crop intent

- Right-counter crop: include the main long sweet display counter, its glass, product surface, immediate floor spill and enough ceiling context to judge beam direction.
- Left-counter crop: include the smaller left-front display counter, product surface, glass and immediate spill.
- Ceiling/glass crop: include the most visually relevant ceiling zone above the counters plus the primary glass-reflection area so fixture visibility, hot spots and reflection realism can be judged.

Choose the crop rectangles from the locked V01 frame and record them exactly. Do not crop only the brightest pixels. Keep enough context for design judgement.

## State after publish

Update `projects/pulla-reddy/state/V01.json` to:

- `status`: `waiting_for_chatgpt_review`
- `current_layer`: `1`
- `approved_through_layer`: `0`
- keep candidate `layer-01-front-display-counter-downlights-v4.png`
- `next_required_action`: `Independent visual review using connector evidence pack`
- `user_decision_required`: `false`

Do not alter root project sequencing or any other view state.

STOP after publishing this evidence pack. This request does not authorize any visual correction or Layer 02 work.
