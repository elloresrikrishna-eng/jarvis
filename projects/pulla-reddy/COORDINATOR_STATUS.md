# Pulla Reddy Multi-View Coordinator Status

Updated: `2026-08-19T04:09:41Z`

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Candidate SHA-256 | Artifact ID | Workflow run ID | State | Blocker | Next machine action |
|---|---|---|---|---|---|---|---|
| V01 Main Retail | Layer 02 wall-wash released | Approved parent `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217` | Approved parent `9350820837` | Approved parent `32211254927` | `codex_action_required` | None | Execute `instructions/V01_LAYER02_WALL_WASH.md`, publish exact candidate artifact, verify provenance, stop at `READY_FOR_JARVIS_REVIEW`. |
| V02 Curved Seating | Establish shared planter, then Layer 00 | None | None | None | `codex_action_required` | Shared V02/V06 planter specification does not yet exist | Create `SHARED_PLANTER_SPEC.md`, build Layer 00 with planter present and unlit, publish artifact. |
| V03 Reverse Retail | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V04 Product Elevation | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V05 Window Shelving | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V06 Curved Seating Hero | Repair authoritative parent chain at Layer 00 | None for current Layer 00 | Rejected Layer 03 artifact `9345373457` only | Rejected Layer 03 run `32194514959` only | `codex_action_required` | Mandatory shared planter absent; prior Layer 03 is rejected and invalid as parent | Create shared planter spec, rebuild Layer 00 with planter present and unlit, publish artifact, stop for review. |

## V01 approval result

V01 Layer 01 v4 was independently reviewed from the exact remotely retrievable GitHub Actions artifact and approved as the immutable parent for Layer 02. The approved candidate hash is `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217`, decision `jarvis-v01-l01-bb0eda1c-approve-001`. Layer 02 is now released with wall-wash only; integrated shelf lighting remains locked for Layer 03.
