# Pulla Reddy Multi-View Coordinator Status

Updated: 2026-08-19T09:36:52Z

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Candidate SHA-256 | Artifact ID | Workflow run ID | State | Blocker | Next machine action |
|---|---|---|---|---|---|---|---|
| V01 Main Retail | Lighting concept sketch task ID 07 | `0b0e4bacdf2961335fe1d82cae6d86f9fc0ce3511ad6fa5e16fcf82c8feaeb78` | `9359748337` | `32238231642` | `READY_FOR_JARVIS_REVIEW` | Independent concept-sketch approval pending | Review the exact content-addressed concept-sketch artifact. Do not release the Final V01 Composite without exact candidate-bound approval. |
| V02 Curved Seating | Establish shared planter, then Layer 00 | None | None | None | `codex_action_required` | Shared V02/V06 planter specification does not yet exist | Create `SHARED_PLANTER_SPEC.md`, build Layer 00 with planter present and unlit, publish artifact. |
| V03 Reverse Retail | Layer 01 counter downlighting released from approved Layer 00 | Approved parent `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a` | Parent artifact `9353996410` | Parent run `32221280077` | `codex_action_required` | None | Execute `instructions/V03_LAYER01_COUNTER_DOWNLIGHTING.md`, publish exact Layer 01 artifact, stop at `READY_FOR_JARVIS_REVIEW`. |
| V04 Product Elevation | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V05 Window Shelving | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V06 Curved Seating Hero | Repair authoritative parent chain at Layer 00 | None for current Layer 00 | Rejected Layer 03 artifact `9345373457` only | Rejected Layer 03 run `32194514959` only | `codex_action_required` | Mandatory shared planter absent; prior Layer 03 is rejected and invalid as parent | Create shared planter spec, rebuild Layer 00 with planter present and unlit, publish artifact, stop for review. |

## V01 concept-sketch publication awaiting independent review

Candidate `0b0e4bacdf2961335fe1d82cae6d86f9fc0ce3511ad6fa5e16fcf82c8feaeb78` is published as task/layer ID `07` with task kind `concept-sketch` through GitHub Actions artifact `9359748337`, run `32238231642`, from commit `a8a60adec5fbaac99a4ef64f550a67a6403133f4`.

The downloaded artifact archive digest is `sha256:0c10aa104541d98f2a79d81d676546138123c8ea326ca23828d208f59c2727fe`. Its `candidate.png`, candidate manifest and generated provenance independently match the exact candidate SHA-256, publication commit and workflow run.

The sketch preserves the 1624 x 968 source coordinate grid and maps selective warm amber only to the six independently approved lighting families. Deterministic QA records zero amber pixels outside all approved family support. The Final V01 Composite remains locked pending exact candidate-bound independent approval.

## V01 Layer 06 independent approval

Candidate `a059b10401f0e9b8c3d235630a3e2c43e5e70a3925022a05f65d71744d06bc30` is independently approved under decision `jarvis-v01-l06-a059b104-approve-001`.

The exact GitHub Actions artifact was downloaded and candidate.png independently hashed to the published SHA-256. The approved Layer 05 parent artifact was also retrieved and independently verified at `eda764d05c8880522a22098f653f234e54e4194c859a718f026d8040e4b45065` for direct visual comparison.

The new contribution is confined to two tight warm reflected-floor zones immediately beneath the visible rear built-in banquette. The source remains fully concealed and the effect reads as restrained low-level under-seater support rather than a visible strip, luminous ribbon, broad floor wash or dramatic floating bench. It is deliberately subtle but remains legible in direct parent-versus-candidate comparison, which is appropriate for this layer. Principal sweet counters remain strongest, wall shelves remain second, central merchandise remains third, and the hospitality zone remains calmer than retail. Camera, crop, architecture, ceiling grid, counters, shelves, products, central display, furniture, glass/reflection character and all previously approved lighting families remain visually frozen outside physically plausible local interaction.

Deterministic QA confirms zero changed pixels outside the allowed under-seater zones, zero protected-region drift, no negative/darkening adjustment and no global exposure lift. V01 is therefore released to the lighting concept sketch task only. The exact approved Layer 06 render remains immutable and the final-composite task stays locked until the sketch receives candidate-bound independent approval.

## V01 Layer 05 independent approval

Candidate `eda764d05c8880522a22098f653f234e54e4194c859a718f026d8040e4b45065` is independently approved under decision `jarvis-v01-l05-eda764d0-approve-001`.

The exact GitHub Actions artifact was downloaded and candidate.png independently verified against the published SHA-256. The approved Layer 04 parent artifact was also retrieved for direct visual comparison. The new contribution remains confined to the two rear hospitality table/seating zones and their tight local floor support. The rear seating becomes readable through restrained warm comfort pools while remaining clearly subordinate to the principal sweet counters, wall shelf compositions and central merchandise. The added contribution is presentation-legible without flattening the scene into a broad ambient wash. Ceiling sources remain visually quiet, the added light reads consistently at 3000K, and camera, crop, architecture, ceiling grid, counters, shelves, products, glass character and all earlier approved lighting families remain visually frozen outside physically plausible local interaction.

V01 was released to Layer 06 under-seater lighting only after that approval.

## V01 Layer 04 independent approval

Candidate `58553357484f01018a2d8a3929c3c662d67b3fbc21143847bb255d1c7d2ed837` is independently approved under decision `jarvis-v01-l04-58553357-approve-001`.

The exact GitHub Actions artifact was downloaded and independently hashed. Visual comparison against approved Layer 03 confirms the new contribution remains localized to the central freestanding merchandise display and its immediate floor pool. The principal sweet counters remain the strongest retail destination, wall-shelf compositions remain second tier, and the central display reads as a controlled third tier. The added warm contribution is restrained and source-invisible, with no scene-wide exposure lift or visible ceiling fixture. Camera, architecture, ceiling grid, counters, wall shelves and previously approved lighting remain visually intact.

V01 was released to Layer 05 rear-seating comfort only after that approval.

## Independent review actions completed previously

### V01 Layer 03

Candidate `9c855ce50bea0032a17e0b6a230d7282dc1c078116dc0210b7fd33bcc525b6af` is independently approved under decision `jarvis-v01-l03-9c855ce5-approve-001`.

The added integrated shelf contribution remains confined to the wall-shelf compositions, reads as a gentle merchandise/shelf glow, and does not introduce raw LED ribbons, visible fixture bodies, ceiling clutter or meaningful shifts to the approved counter hierarchy.

### V03 Layer 00

Candidate `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a` is independently approved under decision `jarvis-v03-l00-a6056c69-approve-001`.

The all-proposed-electric-lighting-off baseline remains dark enough to preserve contrast headroom for later retail lighting while retaining source-consistent residual environmental readability. No active proposed lighting family, glowing ceiling aperture, shelf-strip effect or artificial hero emphasis is visible.
