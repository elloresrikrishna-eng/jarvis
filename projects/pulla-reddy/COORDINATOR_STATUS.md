# Pulla Reddy Multi-View Coordinator Status

Updated: `2026-08-19T03:13:22.497Z`

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Candidate SHA-256 | Artifact ID | Workflow run ID | State | Blocker | Next machine action |
|---|---|---|---|---|---|---|---|
| V01 Main Retail | Layer 01 v4 | `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217` | `9350820837` | `32211254927` | `READY_FOR_JARVIS_REVIEW` | External review pending | JARVIS reviews the exact artifact. Do not advance to Layer 02. |
| V02 Curved Seating | Establish shared planter, then Layer 00 | None | None | None | `codex_action_required` | Shared V02/V06 planter specification does not yet exist | Create `SHARED_PLANTER_SPEC.md`, build Layer 00 with planter present and unlit, publish artifact. |
| V03 Reverse Retail | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V04 Product Elevation | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V05 Window Shelving | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V06 Curved Seating Hero | Repair authoritative parent chain at Layer 00 | None for current Layer 00 | Rejected Layer 03 artifact `9345373457` only | Rejected Layer 03 run `32194514959` only | `codex_action_required` | Mandatory shared planter absent; prior Layer 03 is rejected and invalid as parent | Create shared planter spec, rebuild Layer 00 with planter present and unlit, publish artifact, stop for review. |

## V01 artifact migration result

The existing V01 Layer 01 v4 PNG was migrated without regeneration or visual modification. The published artifact was downloaded and independently hash-checked after workflow completion. Candidate, manifest, and artifact provenance all bind to the same SHA-256.
