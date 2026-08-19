# Pulla Reddy Multi-View Coordinator Status

Updated: `2026-08-19T06:45:43.911Z`

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Candidate SHA-256 | Artifact ID | Workflow run ID | State | Blocker | Next machine action |
|---|---|---|---|---|---|---|---|
| V01 Main Retail | Layer 04 central merchandise / circulation published | `58553357484f01018a2d8a3929c3c662d67b3fbc21143847bb255d1c7d2ed837` | `9355045008` | `32224475803` | `READY_FOR_JARVIS_REVIEW` | None | Independent external JARVIS review of the exact Layer 04 artifact. Do not start Layer 05 without approval. |
| V02 Curved Seating | Establish shared planter, then Layer 00 | None | None | None | `codex_action_required` | Shared V02/V06 planter specification does not yet exist | Create `SHARED_PLANTER_SPEC.md`, build Layer 00 with planter present and unlit, publish artifact. |
| V03 Reverse Retail | Layer 01 counter downlighting released from approved Layer 00 | Approved parent `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a` | Parent artifact `9353996410` | Parent run `32221280077` | `codex_action_required` | None | Execute `instructions/V03_LAYER01_COUNTER_DOWNLIGHTING.md`, publish exact Layer 01 artifact, stop at `READY_FOR_JARVIS_REVIEW`. |
| V04 Product Elevation | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V05 Window Shelving | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V06 Curved Seating Hero | Repair authoritative parent chain at Layer 00 | None for current Layer 00 | Rejected Layer 03 artifact `9345373457` only | Rejected Layer 03 run `32194514959` only | `codex_action_required` | Mandatory shared planter absent; prior Layer 03 is rejected and invalid as parent | Create shared planter spec, rebuild Layer 00 with planter present and unlit, publish artifact, stop for review. |

## V01 Layer 04 publication result

The exact candidate `58553357484f01018a2d8a3929c3c662d67b3fbc21143847bb255d1c7d2ed837` was produced from approved Layer 03 parent `9c855ce50bea0032a17e0b6a230d7282dc1c078116dc0210b7fd33bcc525b6af`.

Deterministic QA records zero changed pixels outside the permitted central-merchandise and tight adjacent-floor zones. Both counters, both wall-shelf families, the ceiling, rear seating and foreground floor remain exactly frozen. The global mean luminance shift is `+0.141173` and contains no negative or exposure-cheat adjustment.

GitHub Actions run `32224475803` completed successfully. Artifact `9355045008` was downloaded through the connected GitHub app, and its candidate, manifest and generated provenance all match the exact candidate hash, publication commit and run ID.

V01 is now `READY_FOR_JARVIS_REVIEW`. Layer 05 remains locked.
## Independent review actions completed

### V01 Layer 03

Candidate `9c855ce50bea0032a17e0b6a230d7282dc1c078116dc0210b7fd33bcc525b6af` is independently approved under decision `jarvis-v01-l03-9c855ce5-approve-001`.

The actual GitHub Actions artifact was downloaded and visually compared with approved Layer 02. The added integrated shelf contribution remains confined to the wall-shelf compositions, reads as a gentle merchandise/shelf glow, and does not introduce raw LED ribbons, visible fixture bodies, ceiling clutter or meaningful shifts to the approved counter hierarchy. The effect is restrained but still legible as a distinct second shelf-lighting family. Deterministic QA corroborates zero changed pixels outside the permitted shelf zones and no global exposure lift.

V01 is now released to Layer 04 only. Layer 05 remains locked.

### V03 Layer 00

Candidate `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a` is independently approved under decision `jarvis-v03-l00-a6056c69-approve-001`.

The actual artifact was inspected as the all-proposed-electric-lighting-off baseline. It remains dark enough to preserve contrast headroom for later retail lighting while retaining source-consistent residual environmental readability. No active proposed lighting family, glowing ceiling aperture, shelf-strip effect or artificial hero emphasis is visible.

V03 is now released to Layer 01 counter downlighting only. The following wall-wash layer remains locked.
