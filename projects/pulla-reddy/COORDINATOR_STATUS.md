# Pulla Reddy Multi-View Coordinator Status

Updated: 2026-08-19T16:39:10.384938Z

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Candidate / approved reference | State | Blocker | Next machine action |
|---|---|---|---|---|---|
| V01 Main Retail | Repaired Layer 06 concealed under-seater lighting | Candidate `318b1237c35905e21720e8fc38054b4e93fb93202cfca07cd8b2a8233cf14904`; artifact `9374332164`; run `32276889137`; approved repaired Layer 05 parent `f8335d6a5081b096e396a62af688dca39dca95d6a007b08cad4467046b6095ca` under `jarvis-v01-l05-f8335d6a-approve-002` | `READY_FOR_JARVIS_REVIEW` | Exact candidate-bound external JARVIS review | Review repaired Layer 06. Do not begin repaired Final without exact approval. |
| V02 Curved Seating | Establish shared planter, then Layer 00 | None | `codex_action_required` | Shared V02/V06 planter specification does not yet exist | Create `SHARED_PLANTER_SPEC.md`, build Layer 00 with planter present and unlit, publish artifact. |
| V03 Reverse Retail | Layer 01 counter downlighting | Approved parent `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a` | `codex_action_required` | None | Execute `instructions/V03_LAYER01_COUNTER_DOWNLIGHTING.md`, publish Layer 01 artifact, stop at `READY_FOR_JARVIS_REVIEW`. |
| V04 Product Elevation | Initialize and create Layer 00 | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V05 Window Shelving | Initialize and create Layer 00 | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V06 Curved Seating Hero | Repair authoritative parent chain at Layer 00 | Rejected Layer 03 `6de8f029666f724431a22d80eec24a9f287123fb0aca9f9af751c5f0f3d7bd6f` remains invalid as parent | `codex_action_required` | Mandatory shared planter absent | Create shared planter spec, rebuild V06 Layer 00 with planter present and unlit, publish artifact. |

## V01 repaired Layer 05 approval

The exact repaired Layer 05 candidate `f8335d6a5081b096e396a62af688dca39dca95d6a007b08cad4467046b6095ca` was independently reviewed against exact approved repaired Layer 04 parent `a3d00e7526313425428e1375d0765ad652a12d9ee43883815a83abacc193ba8e`.

JARVIS downloaded artifact `9372085257` and independently SHA-256 verified the candidate, then separately downloaded and verified parent artifact `9369801718` before direct full-resolution comparison. The new contribution is confined to two calm rear seating/table comfort pools plus minimal nearby floor support. It materially improves hospitality readability while remaining clearly subordinate to the sweet counters, wall merchandise and central merchandise. The ceiling remains visually quiet, source visibility remains controlled, added light reads warm and believable, and no broad ambient or exposure lift is apparent.

Deterministic QA remains clean: `dx=0, dy=0`, zero negative RGB deltas, zero changed pixels outside the allowed rear zones, 2.855095% changed pixels and a +0.231303 full-frame mean luminance shift.

Decision: `jarvis-v01-l05-f8335d6a-approve-002`.

This exact repaired Layer 05 candidate is now the immutable parent for repaired Layer 06.

## V01 repaired Layer 06 publication

The repaired Layer 06 candidate `318b1237c35905e21720e8fc38054b4e93fb93202cfca07cd8b2a8233cf14904` was built from exact approved repaired Layer 05 parent `f8335d6a5081b096e396a62af688dca39dca95d6a007b08cad4467046b6095ca` under `jarvis-v01-l05-f8335d6a-approve-002`.

Only two restrained concealed 3000K under-seater floor glows were added beneath the visible rear banquette bays. The source remains hidden, the effect is presentation-legible but subordinate to the approved rear-seating comfort pools and every retail tier, and no luminous ribbon or broad rear-floor wash is present.

Deterministic QA passes: `dx=0, dy=0`, zero negative RGB deltas, zero changed pixels outside the released under-seater zones, 0.727530% changed pixels and a +0.027577 full-frame mean luminance shift. Artifact `9374332164` from run `32276889137` was independently downloaded. The archive digest is `sha256:8480b0a82dbb829f298b051bb7d4ca89158797d01d76783becc17bb33acfb957`, and candidate, manifest and workflow provenance all resolve to exact candidate SHA `318b1237c35905e21720e8fc38054b4e93fb93202cfca07cd8b2a8233cf14904` and publication commit `633f46af9f86c068bc6bba367dbd89c48ddacdd5`.

V01 now rests at `READY_FOR_JARVIS_REVIEW`. Repaired Final remains locked until exact candidate-bound approval.

## Still-valid independent approvals

- V01 Layer 01: `jarvis-v01-l01-bb0eda1c-approve-001`, exact repair root
- V01 repaired Layer 02: `jarvis-v01-l02-c6bb3f56-approve-002`
- V01 repaired Layer 03: `jarvis-v01-l03-8e2a2b19-approve-002`
- V01 repaired Layer 04: `jarvis-v01-l04-a3d00e75-approve-002`
- V01 repaired Layer 05: `jarvis-v01-l05-f8335d6a-approve-002`, exact current approved render parent
- V01 Concept Sketch: `jarvis-v01-l07-0b0e4bac-approve-001`, communication-only and never a pixel parent
- V03 Layer 00: `jarvis-v03-l00-a6056c69-approve-001`

Historical V01 approvals for the defective downstream chain remain part of immutable provenance, but the failed cross-layer audit supersedes their use as valid production ancestry. Repaired Layer 06 is awaiting review; repaired Final must still be independently approved sequentially.

## Active quality holds

1. V01 contact-sheet/review-board production remains locked until repaired Layer 06 and repaired Final are sequentially rebuilt and independently approved, followed by a fresh passing continuity audit.
2. V06 cannot advance beyond Layer 00 until the mandatory shared V02/V06 planter specification is established and the planter-bearing Layer 00 through Layer 02 chain is independently rebuilt. The previously rejected Layer 03 remains invalid as a cumulative parent.
