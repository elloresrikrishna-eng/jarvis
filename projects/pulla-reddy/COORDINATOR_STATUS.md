# Pulla Reddy Multi-View Coordinator Status

Updated: 2026-08-19T15:38:00Z

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Candidate / approved reference | State | Blocker | Next machine action |
|---|---|---|---|---|---|
| V01 Main Retail | Repaired Layer 05 rear seating comfort | Candidate `f8335d6a5081b096e396a62af688dca39dca95d6a007b08cad4467046b6095ca`; artifact `9372085257`; run `32270868999`; approved repaired Layer 04 parent `a3d00e7526313425428e1375d0765ad652a12d9ee43883815a83abacc193ba8e` | `READY_FOR_JARVIS_REVIEW` | Exact candidate-bound external JARVIS review | Review repaired Layer 05. Do not begin repaired Layer 06 without exact approval. |
| V02 Curved Seating | Establish shared planter, then Layer 00 | None | `codex_action_required` | Shared V02/V06 planter specification does not yet exist | Create `SHARED_PLANTER_SPEC.md`, build Layer 00 with planter present and unlit, publish artifact. |
| V03 Reverse Retail | Layer 01 counter downlighting | Approved parent `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a` | `codex_action_required` | None | Execute `instructions/V03_LAYER01_COUNTER_DOWNLIGHTING.md`, publish Layer 01 artifact, stop at `READY_FOR_JARVIS_REVIEW`. |
| V04 Product Elevation | Initialize and create Layer 00 | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V05 Window Shelving | Initialize and create Layer 00 | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V06 Curved Seating Hero | Repair authoritative parent chain at Layer 00 | Rejected Layer 03 `6de8f029666f724431a22d80eec24a9f287123fb0aca9f9af751c5f0f3d7bd6f` remains invalid as parent | `codex_action_required` | Mandatory shared planter absent | Create shared planter spec, rebuild V06 Layer 00 with planter present and unlit, publish artifact. |

## V01 repaired Layer 05 publication

The repaired Layer 05 candidate `f8335d6a5081b096e396a62af688dca39dca95d6a007b08cad4467046b6095ca` was built from exact approved repaired Layer 04 parent `a3d00e7526313425428e1375d0765ad652a12d9ee43883815a83abacc193ba8e` under decision `jarvis-v01-l04-a3d00e75-approve-002`.

Only restrained deep-recessed 3000K rear-seating comfort illumination was added. The two rear table/seating pools are presentation-legible but remain softer than the sweet counters, wall merchandise and central display. Ceiling, shelves, both sweet counters, central merchandise, the approved Layer 04 floor pool and foreground remain exact parent pixels.

Deterministic QA passes: `dx=0, dy=0`, zero negative RGB deltas, zero changed pixels outside the allowed rear zones, 2.855095% changed pixels and a +0.231303 full-frame mean luminance shift. The GitHub Actions artifact `9372085257` from run `32270868999` was downloaded independently. Its archive digest is `sha256:395b33d0f4ce09dbe3724cccb05a722f46bba32d94a46a9ffb9f8a03c74c3474`, and candidate, manifest and workflow provenance all resolve to the exact candidate SHA and publication commit `7b63b7abb7d1b557341a64951603f5bdad617542`.

V01 now rests at `READY_FOR_JARVIS_REVIEW`. Repaired Layer 06 remains locked until exact candidate-bound approval.

## Still-valid independent approvals

- V01 Layer 01: `jarvis-v01-l01-bb0eda1c-approve-001`, exact repair root
- V01 repaired Layer 02: `jarvis-v01-l02-c6bb3f56-approve-002`
- V01 repaired Layer 03: `jarvis-v01-l03-8e2a2b19-approve-002`
- V01 repaired Layer 04: `jarvis-v01-l04-a3d00e75-approve-002`, exact current approved render parent
- V01 Concept Sketch: `jarvis-v01-l07-0b0e4bac-approve-001`, communication-only and never a pixel parent
- V03 Layer 00: `jarvis-v03-l00-a6056c69-approve-001`

Historical V01 approvals for the defective downstream chain remain part of immutable provenance, but the failed cross-layer audit supersedes their use as valid production ancestry. Repaired Layer 05 is awaiting review; repaired Layer 06 and Final must still be independently approved sequentially.

## Active quality holds

1. V01 contact-sheet/review-board production remains locked until repaired Layer 05, Layer 06 and Final are sequentially rebuilt and independently approved, followed by a fresh passing continuity audit.
2. V06 cannot advance beyond Layer 00 until the mandatory shared V02/V06 planter specification is established and the planter-bearing Layer 00 through Layer 02 chain is independently rebuilt. The previously rejected Layer 03 remains invalid as a cumulative parent.
