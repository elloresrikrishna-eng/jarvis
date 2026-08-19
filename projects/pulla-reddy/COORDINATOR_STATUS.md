# Pulla Reddy Multi-View Coordinator Status

Updated: 2026-08-19T07:43:09Z

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Candidate SHA-256 | Artifact ID | Workflow run ID | State | Blocker | Next machine action |
|---|---|---|---|---|---|---|---|
| V01 Main Retail | Layer 05 rear seating comfort candidate | eda764d05c8880522a22098f653f234e54e4194c859a718f026d8040e4b45065 | 9356509692 | 32228898766 | READY_FOR_JARVIS_REVIEW | Independent review pending | External JARVIS review of the exact artifact; do not start Layer 06. |
| V02 Curved Seating | Establish shared planter, then Layer 00 | None | None | None | `codex_action_required` | Shared V02/V06 planter specification does not yet exist | Create `SHARED_PLANTER_SPEC.md`, build Layer 00 with planter present and unlit, publish artifact. |
| V03 Reverse Retail | Layer 01 counter downlighting released from approved Layer 00 | Approved parent `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a` | Parent artifact `9353996410` | Parent run `32221280077` | `codex_action_required` | None | Execute `instructions/V03_LAYER01_COUNTER_DOWNLIGHTING.md`, publish exact Layer 01 artifact, stop at `READY_FOR_JARVIS_REVIEW`. |
| V04 Product Elevation | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V05 Window Shelving | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V06 Curved Seating Hero | Repair authoritative parent chain at Layer 00 | None for current Layer 00 | Rejected Layer 03 artifact `9345373457` only | Rejected Layer 03 run `32194514959` only | `codex_action_required` | Mandatory shared planter absent; prior Layer 03 is rejected and invalid as parent | Create shared planter spec, rebuild Layer 00 with planter present and unlit, publish artifact, stop for review. |

## V01 Layer 05 publication

Candidate eda764d05c8880522a22098f653f234e54e4194c859a718f026d8040e4b45065 is published through GitHub Actions artifact 9356509692 from workflow run 32228898766.

The downloaded artifact candidate, candidate manifest and generated provenance all match the exact candidate SHA-256 and publication commit 47b35fb2e861ef6d4f8c9f02578769ab4a00a1e0. Deterministic QA confirms zero changed pixels outside the permitted rear hospitality zones and zero shift in the approved counter, shelf, central-merchandise, central-floor-pool, ceiling and foreground regions.

V01 is stopped at READY_FOR_JARVIS_REVIEW. Layer 06 remains locked until this exact Layer 05 candidate receives independent candidate-bound approval.
## V01 Layer 04 independent approval

Candidate `58553357484f01018a2d8a3929c3c662d67b3fbc21143847bb255d1c7d2ed837` is independently approved under decision `jarvis-v01-l04-58553357-approve-001`.

The exact GitHub Actions artifact was downloaded and independently hashed. Visual comparison against approved Layer 03 confirms the new contribution remains localized to the central freestanding merchandise display and its immediate floor pool. The principal sweet counters remain the strongest retail destination, wall-shelf compositions remain second tier, and the central display reads as a controlled third tier. The added warm contribution is restrained and source-invisible, with no scene-wide exposure lift or visible ceiling fixture. Camera, architecture, ceiling grid, counters, wall shelves and previously approved lighting remain visually intact.

V01 is therefore released to Layer 05 rear-seating comfort only. Layer 06 remains locked until Layer 05 receives exact candidate-bound independent approval.

## Independent review actions completed previously

### V01 Layer 03

Candidate `9c855ce50bea0032a17e0b6a230d7282dc1c078116dc0210b7fd33bcc525b6af` is independently approved under decision `jarvis-v01-l03-9c855ce5-approve-001`.

The added integrated shelf contribution remains confined to the wall-shelf compositions, reads as a gentle merchandise/shelf glow, and does not introduce raw LED ribbons, visible fixture bodies, ceiling clutter or meaningful shifts to the approved counter hierarchy.

### V03 Layer 00

Candidate `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a` is independently approved under decision `jarvis-v03-l00-a6056c69-approve-001`.

The all-proposed-electric-lighting-off baseline remains dark enough to preserve contrast headroom for later retail lighting while retaining source-consistent residual environmental readability. No active proposed lighting family, glowing ceiling aperture, shelf-strip effect or artificial hero emphasis is visible.
