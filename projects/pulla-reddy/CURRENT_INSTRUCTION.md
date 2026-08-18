# Current Instruction | V01 Main Retail | REWORK LAYER 01

The previous provisional Layer 01 approval is revoked.

Layer 00 remains the only approved visual base for View 01.

Do not generate Layer 02.

Read:
- `projects/pulla-reddy/PROJECT_RULES.md`
- `projects/pulla-reddy/V01_EXECUTION_QUEUE.md`
- `projects/pulla-reddy/REVIEWER_RUBRIC.md`
- `projects/pulla-reddy/review/V01/CHATGPT_REVIEW_LAYER_01_REJECTED.md`

## Required action

Rebuild Layer 01 from approved Layer 00 only.

### Layer 01 intent
Add only controlled deep-recessed 3000K downlighting over the principal front sweet display counters.

The lighting must create a clear product-first hierarchy and must look like deliberate architectural lighting rather than generic image brightening.

### Visual targets
- sweets immediately become the strongest visual attraction;
- clear but restrained pools of light with believable beam direction and falloff;
- recessed sources remain visually quiet, dark and deep-set;
- no ceiling-dot effect;
- warm appetising product rendering without orange cast or blown highlights;
- glass remains transparent/readable with no ugly hot spots;
- unrelated shelves, walls, central displays and rear seating remain visually at Layer 00;
- no ambient fill and no global exposure lift.

### Absolute locks
Preserve exactly:
- camera, crop, perspective and focal character;
- architecture and ceiling grid;
- counters, products, shelves, furniture and materials;
- approved Layer 00 outside physically necessary spill.

## Self-correction before review
If the first attempt feels flat, overly bright, too diffuse, too spotty, too orange, or creates visible luminous apertures, iterate autonomously before publishing.

## Review output
Publish a fresh Layer 01 review package under `projects/pulla-reddy/review/V01/` with:
- updated `STATUS.md`;
- updated `manifest.json`;
- updated `SELF_QA.md`;
- fresh Layer 01 preview;
- fresh Layer 00 vs Layer 01 side-by-side;
- a short `DESIGN_INTENT_CHECK.md` explaining how the final candidate achieves product hierarchy, beam realism and glass control.

Then set `STATE.json` to `waiting_for_chatgpt_review`, with:
- `current_layer`: 1
- `approved_through_layer`: 0
- `next_required_action`: `Independent ChatGPT visual/design review of reworked Layer 01`
- `user_decision_required`: false

STOP after publishing. Do not advance to Layer 02 until explicitly approved.