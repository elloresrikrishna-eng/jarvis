# Pulla Reddy Multi-View Coordinator Status

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Immutable approved reference | State | Blocker | Next machine action |
|---|---|---|---|---|---|
| V01 Main Retail | Repaired-chain lighting concept sketch | Repaired Layer 06 `318b1237c35905e21720e8fc38054b4e93fb93202cfca07cd8b2a8233cf14904`, approved under `jarvis-v01-l06-318b1237-approve-002` | `codex_action_required` | None for sketch production | Execute `instructions/V01_CONCEPT_SKETCH_REPAIRED.md`, publish sketch artifact, stop at `READY_FOR_JARVIS_REVIEW`. Do not begin Final/composite yet. |
| V02 Curved Seating | Layer 01 recessed wall-wash correction | Layer 00 `c0db62b789677bef3390003a97230c6a442018005d1f6c9b73f1bebd20851540`, approved under `jarvis-v02-l00-c0db62b7-approve-001` | `codex_action_required` | Previous Layer 01 candidate `af3045bc9902183b15c7dd43878f87c5586b51cf2fc743317753b8d0564da619` rejected for weak presentation legibility and isolated glow-patch character | Execute `instructions/V02_LAYER01_WALL_WASH_CORRECTION_001.md`, rebuild from exact approved Layer 00, keep shared planter unlit, publish fresh candidate and stop at review. Do not begin integrated shelf lighting. |
| V03 Reverse Retail | Layer 01 sweet-counter downlighting | Layer 00 `a6056c69baaab4912169e78e0d7883fa666bc215e3cf3144c3df03efccb80a1a`, approved under `jarvis-v03-l00-a6056c69-approve-001` | `codex_action_required` | None | Execute `instructions/V03_LAYER01_COUNTER_DOWNLIGHTING.md`, publish and stop at review. |
| V04 Product Elevation | Layer 00 initialization | None yet | `codex_action_required` | No current candidate | Build authoritative lights-off Layer 00 from page 5, publish review artifact and stop at review. |
| V05 Window Shelving | Layer 01 recessed wall-wash | Layer 00 `76326a4e726229fc343ee401b49a696d4132968c9e776e0d05e07546c9e42be1`, approved under `jarvis-v05-l00-76326a4e-approve-001` | `codex_action_required` | None | Execute `instructions/V05_LAYER01_WALL_WASH.md`, publish and stop at review. |
| V06 Curved Seating Hero | Repaired Layer 01 seating/table comfort | Repaired Layer 00 `a2c3f2bcb59ebf7e35b2c6e5842f1196227cc7ef6dad3bb6f6de469151ebcff3`, approved under `jarvis-v06-l00-a2c3f2bc-approve-001` | `codex_action_required` | None for Layer 01 | Execute `instructions/V06_LAYER01_SEATING_COMFORT.md`, keep shared planter unlit, publish and stop at review. |

## Latest independent approvals consumed

- V01 repaired Layer 06: `jarvis-v01-l06-318b1237-approve-002`
- V02 Layer 00 with shared planter: `jarvis-v02-l00-c0db62b7-approve-001`
- V05 Layer 00: `jarvis-v05-l00-76326a4e-approve-001`
- V06 repaired Layer 00 with shared planter: `jarvis-v06-l00-a2c3f2bc-approve-001`

These candidate-bound approvals have been consumed into the per-view states and exact next-task releases.

## Active rejection / correction

V02 Layer 01 candidate `af3045bc9902183b15c7dd43878f87c5586b51cf2fc743317753b8d0564da619` is independently rejected under `jarvis-v02-l01-af3045bc-reject-001`. The approved Layer 00 parent remains immutable. V02 must execute `instructions/V02_LAYER01_WALL_WASH_CORRECTION_001.md` and remain on Layer 01 until a fresh exact candidate receives independent approval.

## Shared planter status

`SHARED_PLANTER_SPEC.md` is authoritative. V02 and V06 each have an independently approved Layer 00 containing the shared planter physically present and electrically unlit. The earlier V06 parent-chain blocker is resolved at Layer 00.

The historical rejected V06 Layer 03 remains invalid as a raster parent. Its restrained under-seater character may be consulted only as a non-authoritative visual target when the repaired chain reaches the appropriate layer.

## V01 repair status

The repaired V01 cumulative render chain is independently approved through repaired Layer 06. The historical defective downstream Final remains invalid as a production parent. V01 must now complete the repaired-chain communication/final stages in order:

1. concept sketch review;
2. repaired Final/composite release and review;
3. fresh cross-layer continuity audit;
4. contact sheet/review board;
5. completion package.

Contact-sheet/review-board production remains locked until repaired Final and fresh continuity audit pass.

## Global locks

- 3000K only for added electric lighting.
- Recessed, concealed or integrated sources only.
- No visible pendants, tracks or surface fixtures.
- No camera, crop, architecture, material, product or furniture drift.
- No global exposure/gamma cheating.
- One new lighting family per cumulative layer.
- Every approved immediate parent remains frozen.
- Deterministic QA is evidence, not design approval.
- Every candidate must be bound to its exact SHA-256 and remotely retrievable through the review-artifact path.

## Presentation gate

Presentation state: `WAITING_FOR_ALL_VIEWS`

Presentation generation: `LOCKED`

No user decision is currently required.
