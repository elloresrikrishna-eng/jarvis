# Current Instruction | V01 Main Retail | Execute 10-Step Queue

Layer 00 and Layer 01 are approved and locked.

Do not recreate or reinterpret either approved layer.

## Required action now

Execute the released autonomous work plan in:

`projects/pulla-reddy/V01_EXECUTION_QUEUE.md`

Use:

`projects/pulla-reddy/REVIEWER_RUBRIC.md`

as the quality standard for your own internal pre-publication checks. The independent ChatGPT reviewer will also use this rubric and may be stricter than your self-QA.

## Execution mode

Proceed through Tasks 01 to 10 in order.

For each task:

1. Complete the task locally in the existing `V01_Main_Retail` workspace.
2. Preserve all global project locks.
3. Run objective QA.
4. If the candidate clearly fails any hard rule, correct it before proceeding.
5. Publish the task result/review package into Jarvis with an explicit task number and status.
6. Continue to the next queue item only if the current task passes your internal QA and no `blocked_user_decision` state is required.

Do not wait for Srikrishna between routine tasks.

## Important

The reviewer is intentionally independent. Do not treat your own `SELF_QA.md` as proof of approval. The external reviewer may reject technically valid work for weak hierarchy, poor product appetite appeal, fixture visibility, bad glass behavior, over-ambient lighting, poor shelf-light character, weak presentation value or other design-quality reasons defined in `REVIEWER_RUBRIC.md`.

## Final state

After Task 10:

- if all mandatory gates pass, set `STATE.json` to `view_complete`;
- if a genuine subjective design decision remains, set `blocked_user_decision`;
- do not start View 02.
