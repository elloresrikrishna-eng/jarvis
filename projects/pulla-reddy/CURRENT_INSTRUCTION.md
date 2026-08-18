# Current Instruction | V01 Main Retail | Execute Task 01 Only

Layer 00 and Layer 01 are approved and locked.

Use:

`projects/pulla-reddy/V01_EXECUTION_QUEUE.md`

and

`projects/pulla-reddy/REVIEWER_RUBRIC.md`

as the authoritative production and quality references.

## Execute now

Complete **Task 01 | Layer 02 Wall-Wash** only.

Starting from approved Layer 01, add only recessed 3000K wall-washer downlights serving all visible wall-mounted shelving compositions. Keep the effect selective, not a blanket wash. Preserve Layer 01 exactly.

## After Task 01

Publish the complete Task 01 review package to Jarvis, including preview, side-by-side comparison, manifest, and self-QA.

Then set `STATE.json` to `waiting_for_chatgpt_review` with `current_layer` 2 and `approved_through_layer` 1.

STOP.

Do not execute Task 02 until the independent ChatGPT reviewer explicitly approves Task 01 and releases Task 02 through Jarvis.

## Review gate rule for all future tasks

This is the permanent operating model:

Codex produces one queue task -> publishes review package -> stops -> independent reviewer either approves and releases the next task, or rejects and issues an exact correction for the same task.

Codex must not self-approve progression between queue tasks.

If rejected, correct only the rejected task while keeping all approved parents frozen, republish, and wait again.

Srikrishna is not part of routine approvals or corrections.
