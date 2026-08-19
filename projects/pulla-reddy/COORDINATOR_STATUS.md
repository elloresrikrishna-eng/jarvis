# Pulla Reddy Multi-View Coordinator Status

Updated: `2026-08-19T05:41:02.500Z`

Presentation generation remains `LOCKED` until every required view has a valid independent JARVIS approval chain.

| View | Current layer/task | Candidate SHA-256 | Artifact ID | Workflow run ID | State | Blocker | Next machine action |
|---|---|---|---|---|---|---|---|
| V01 Main Retail | Layer 03 concealed shelf-integrated lighting published | `9c855ce50bea0032a17e0b6a230d7282dc1c078116dc0210b7fd33bcc525b6af` | `9353602039` | `32219997021` | `READY_FOR_JARVIS_REVIEW` | None | Independent external JARVIS review of the exact Layer 03 artifact. Do not start Layer 04 without approval. |
| V02 Curved Seating | Establish shared planter, then Layer 00 | None | None | None | `codex_action_required` | Shared V02/V06 planter specification does not yet exist | Create `SHARED_PLANTER_SPEC.md`, build Layer 00 with planter present and unlit, publish artifact. |
| V03 Reverse Retail | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V04 Product Elevation | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V05 Window Shelving | Initialize and create Layer 00 | None | None | None | `codex_action_required` | No current candidate | Build Layer 00 with all electric lighting off and publish artifact. |
| V06 Curved Seating Hero | Repair authoritative parent chain at Layer 00 | None for current Layer 00 | Rejected Layer 03 artifact `9345373457` only | Rejected Layer 03 run `32194514959` only | `codex_action_required` | Mandatory shared planter absent; prior Layer 03 is rejected and invalid as parent | Create shared planter spec, rebuild Layer 00 with planter present and unlit, publish artifact, stop for review. |

## V01 Layer 03 publication result

The exact Layer 03 candidate `9c855ce50bea0032a17e0b6a230d7282dc1c078116dc0210b7fd33bcc525b6af` was produced from the approved Layer 02 parent `fc47cfc6a1ccbaac2e8103d2b013036716f43395fba0a0c8a393f797dcf1599e`.

Deterministic QA confirms that the only changed pixels are inside the three permitted shelf-local zones. The approved counter lighting, wall-wash, central display, rear seating, circulation floor, camera and architecture remain frozen. No raw LED line, visible dots, luminous brass support or global exposure lift is present.

GitHub Actions run `32219997021` completed successfully. Artifact `9353602039` was downloaded and its candidate, manifest and provenance all matched the exact candidate SHA, publication commit and run ID.

V01 is now `READY_FOR_JARVIS_REVIEW`. Layer 04 remains locked.
