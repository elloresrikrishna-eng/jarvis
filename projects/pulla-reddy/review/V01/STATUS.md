# V01 Main Retail | Layer 01 Rework Review Status

## Current control state

Layer 00 remains the only approved cumulative parent.

The existing Layer 01 v4 candidate has been migrated unchanged into the active `jarvis-return-path-v1` GitHub Actions binary review-artifact path. It is now `READY_FOR_JARVIS_REVIEW`. No Layer 02 work is released by this package.

## Verified artifact publication

- Candidate SHA-256: `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217`
- GitHub Actions workflow run ID: `32211254927`
- GitHub Actions artifact ID: `9350820837`
- Artifact name: `jarvis-pulla-reddy-v01-l01-bb0eda1c017f`
- Workflow commit: `0e27fdac19ed8b33fe3b5c306c577a4d0397581c`
- Artifact archive digest: `sha256:e8ae725a9c344f7f365e571db65d71756588f05b0d9542d1cd83d8f2017e2aca`
- Remote retrieval: **PASS**
- Downloaded artifact candidate hash: **exact match**
- Downloaded manifest/provenance hash binding: **exact match**

The PNG was not regenerated, re-encoded, or visually modified during migration.

## Authoritative local files

- Source: `D:/Codex/G Pulla Reddy Sweets/01_Views/V01_Main_Retail/source-view-01-original.jpg`
- Approved parent: `D:/Codex/G Pulla Reddy Sweets/01_Views/V01_Main_Retail/layer-00-base-dark.png`
- Reworked candidate: `D:/Codex/G Pulla Reddy Sweets/01_Views/V01_Main_Retail/layer-01-front-display-counter-downlights-v4.png`

All three files are 1624 x 968 at the render stage, except the source is the original JPEG at the same dimensions.

## Candidate scope

Layer 01 adds only deep-recessed 3000K downlighting over:

- the long right-hand sweet display counter;
- the smaller left-front display counter.

The rework tightens the counter-localized beam footprints, reduces floor spill, neutralizes the earlier orange bias, keeps the ceiling completely at Layer 00, and restores unrelated shelves, the central display, and rear seating to exact Layer 00 pixels.

## Review assets

- `layer-01-front-display-counter-downlights-preview.jpg`
- `layer-00-vs-layer-01.jpg`
- `DESIGN_INTENT_CHECK.md`
- `SELF_QA.md`
- `manifest.json`

## Important review posture

The technical QA and remote artifact verification confirm continuity and provenance but are not design approval. The candidate is intentionally waiting for external JARVIS review of artifact `9350820837`.

## Local downstream note

Some downstream files were generated locally under an earlier full-sequence release that Jarvis retracted while production was in progress. They were not published by this package, are not approved, and must not be treated as current cumulative parents.

## Stop condition

Production stops at reworked Layer 01. Layer 02 must not advance until an exact external JARVIS approval is bound to the candidate SHA-256.
