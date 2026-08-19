# Pulla Reddy Multi-View Coordinator Status

Updated: 2026-08-19T10:26:46Z

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Candidate / approved reference | State | Blocker | Next machine action |
|---|---|---|---|---|---|
| V01 Main Retail | Final V01 Composite, task/layer ID 08 | Candidate `a059b10401f0e9b8c3d235630a3e2c43e5e70a3925022a05f65d71744d06bc30`; artifact `9361335925`; run `32242528619` | `READY_FOR_JARVIS_REVIEW` | Independent Final Composite approval pending | Review the exact byte-identical Final Composite artifact. Do not release the cross-layer continuity audit without candidate-bound approval. |
| V02 Curved Seating | Establish shared planter, then Layer 00 | None | `codex_action_required` | Shared V02/V06 planter specification does not yet exist | Create `SHARED_PLANTER_SPEC.md`, build Layer 00 with planter present and unlit, publish artifact. |
| V03 Reverse Retail | Layer 01 counter downlighting | Approved parent `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a` | `codex_action_required` | None | Execute `instructions/V03_LAYER01_COUNTER_DOWNLIGHTING.md`, publish Layer 01 artifact, stop at `READY_FOR_JARVIS_REVIEW`. |
| V04 Product Elevation | Initialize and create Layer 00 | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V05 Window Shelving | Initialize and create Layer 00 | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V06 Curved Seating Hero | Repair authoritative parent chain at Layer 00 | Rejected Layer 03 `6de8f029666f724431a22d80eec24a9f287123fb0aca9f9af751c5f0f3d7bd6f` remains invalid as parent | `codex_action_required` | Mandatory shared planter absent | Create shared planter spec, rebuild V06 Layer 00 with planter present and unlit, publish artifact. |

## V01 Final Composite publication awaiting independent review

Candidate `a059b10401f0e9b8c3d235630a3e2c43e5e70a3925022a05f65d71744d06bc30` is published as task/layer ID `08` with task kind `final-composite` through GitHub Actions artifact `9361335925`, run `32242528619`, from commit `ec2ebaf7448481c41f9253f011ec36d2ae7183c3`.

The downloaded artifact archive digest is `sha256:9d3bfdc89d92b8a0d6e5952badbcd580a5d04721cc90d0e230ae12fda9108a69`. Its `candidate.png`, candidate manifest and generated provenance independently match the exact candidate SHA-256, publication commit and workflow run.

The Final V01 Composite is byte-for-byte identical to the independently approved Layer 06 master: both files contain 2,824,770 bytes and share the same SHA-256. No render processing or new lighting, exposure, reflection, geometry, material, camera or colour decision exists. The cross-layer continuity audit remains locked pending exact candidate-bound independent approval.

## V01 concept-sketch independent approval

Candidate `0b0e4bacdf2961335fe1d82cae6d86f9fc0ce3511ad6fa5e16fcf82c8feaeb78` is independently approved under decision `jarvis-v01-l07-0b0e4bac-approve-001`.

The exact GitHub Actions artifact `9359748337`, workflow run `32238231642`, was downloaded. `candidate.png` independently hashes to the published candidate SHA-256 and matches manifest/provenance. Full-resolution visual comparison against the approved Layer 06 render confirms the sketch preserves the locked source geometry and reads as a restrained charcoal/grayscale architectural sketch with selective warm amber only where approved lighting families exist.

The principal sweet-display counter is the strongest amber destination, wall-shelf compositions remain second, central merchandise third, rear seating comfort fourth, and under-seater support the faintest. The ceiling remains grayscale and visually quiet. No visible pendant, track, surface fitting, raw strip, seventh lighting family, new geometry, text or watermark is introduced. Deterministic QA confirms all six approved families are mapped and zero amber pixels exist outside approved family support.

V01 is released only to the Final Composite task. The concept sketch is an approved communication artifact, not a render parent. The Final Composite should preferably be a byte-for-byte copy of the independently approved Layer 06 master so no lighting, exposure, reflection, geometry or camera change can be introduced.

## Existing independent approvals still binding

- V01 Layer 06: `jarvis-v01-l06-a059b104-approve-001`
- V01 Layer 05: approved parent chain remains binding
- V01 Layer 04: approved parent chain remains binding
- V01 Layer 03: `jarvis-v01-l03-9c855ce5-approve-001`
- V03 Layer 00: `jarvis-v03-l00-a6056c69-approve-001`

## Active quality hold

V06 cannot advance beyond Layer 00 until the mandatory shared V02/V06 planter specification is established and the planter-bearing Layer 00 through Layer 02 chain is independently rebuilt. The previously rejected Layer 03 remains invalid as a cumulative parent.
