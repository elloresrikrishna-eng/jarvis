# Pulla Reddy Multi-View Coordinator Status

Updated: 2026-08-19T14:39:28.4609845Z

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Candidate / approved reference | State | Blocker | Next machine action |
|---|---|---|---|---|---|
| V01 Main Retail | Repaired Layer 04 central merchandise / circulation | Candidate `a3d00e7526313425428e1375d0765ad652a12d9ee43883815a83abacc193ba8e`; artifact `9369801718`; run `32265010608`; approved repaired Layer 03 parent `8e2a2b196904a132c2c18ffd20f7035cf1689656ccea1c3cc871aa714ccc2bba` | `READY_FOR_JARVIS_REVIEW` | Independent candidate-bound review | JARVIS reviews exact Layer 04 artifact. Do not release Layer 05 without exact APPROVE. |
| V02 Curved Seating | Establish shared planter, then Layer 00 | None | `codex_action_required` | Shared V02/V06 planter specification does not yet exist | Create `SHARED_PLANTER_SPEC.md`, build Layer 00 with planter present and unlit, publish artifact. |
| V03 Reverse Retail | Layer 01 counter downlighting | Approved parent `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a` | `codex_action_required` | None | Execute `instructions/V03_LAYER01_COUNTER_DOWNLIGHTING.md`, publish Layer 01 artifact, stop at `READY_FOR_JARVIS_REVIEW`. |
| V04 Product Elevation | Initialize and create Layer 00 | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V05 Window Shelving | Initialize and create Layer 00 | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V06 Curved Seating Hero | Repair authoritative parent chain at Layer 00 | Rejected Layer 03 `6de8f029666f724431a22d80eec24a9f287123fb0aca9f9af751c5f0f3d7bd6f` remains invalid as parent | `codex_action_required` | Mandatory shared planter absent | Create shared planter spec, rebuild V06 Layer 00 with planter present and unlit, publish artifact. |

## V01 repaired Layer 04 candidate publication

The repaired Layer 04 candidate `a3d00e7526313425428e1375d0765ad652a12d9ee43883815a83abacc193ba8e` was built only from exact approved repaired Layer 03 parent `8e2a2b196904a132c2c18ffd20f7035cf1689656ccea1c3cc871aa714ccc2bba` under decision `jarvis-v01-l03-8e2a2b19-approve-002`.

Only selective deep-recessed 3000K central-merchandise lighting and minimum adjacent circulation support were added. Deterministic QA reports dx=0, dy=0, zero negative RGB deltas, zero changed pixels outside the allowed central zones, a 2.844471% changed-pixel fraction and exact freeze of ceiling, shelves, counters, rear seating and foreground floor. Sweet counters remain first, wall merchandise second and central merchandise third.

The exact GitHub Actions artifact `9369801718` from workflow run `32265010608` was downloaded. Its archive digest is `sha256:9b84bdc4be98486e7a586b81f599fdd650f73a674557912846c958106737f944`; candidate.png independently hashes to the published candidate SHA. Candidate manifest and artifact provenance also bind to the same hash, publication commit `3fc2a5719572009538103abc605e14bda14652e8` and workflow run.

V01 is now stopped at `READY_FOR_JARVIS_REVIEW`. Layer 05 remains locked.

## Still-valid independent approvals

- V01 Layer 01: `jarvis-v01-l01-bb0eda1c-approve-001`, exact repair root
- V01 repaired Layer 02: `jarvis-v01-l02-c6bb3f56-approve-002`
- V01 repaired Layer 03: `jarvis-v01-l03-8e2a2b19-approve-002`, exact current approved render parent
- V01 Concept Sketch: `jarvis-v01-l07-0b0e4bac-approve-001`, communication-only and never a pixel parent
- V03 Layer 00: `jarvis-v03-l00-a6056c69-approve-001`

Historical V01 approvals for Layers 02-06 and Final remain part of immutable provenance, but the failed cross-layer audit supersedes their use as valid production ancestry. Repaired Layers 04-06 and Final must still be independently approved sequentially.

## Active quality holds

1. V01 contact-sheet/review-board production remains locked until repaired Layers 04-06 and Final are sequentially rebuilt and independently approved, followed by a fresh passing continuity audit.
2. V06 cannot advance beyond Layer 00 until the mandatory shared V02/V06 planter specification is established and the planter-bearing Layer 00 through Layer 02 chain is independently rebuilt. The previously rejected Layer 03 remains invalid as a cumulative parent.
