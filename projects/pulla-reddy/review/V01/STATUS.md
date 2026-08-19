# V01 Main Retail | Repaired Layer 02 Wall-Wash Candidate

Status: READY_FOR_JARVIS_REVIEW

Task/layer ID: 02 (coordinate-continuity repair)

Candidate: layer-02-wall-shelf-wall-wash-v4.png

Candidate SHA-256: c6bb3f56cd3f2f4372c2aaf8d5ada39bbc7b156c270e46a5235498fd41dd7d27

Approved parent: layer-01-front-display-counter-downlights-v4.png

Approved parent SHA-256: bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217

Repair source decision: jarvis-v01-l09-6a9f3e21-reject-001

## Change from approved Layer 01

Only controlled deep-recessed 3000K wall-washer illumination was added to the visible left and right wall-mounted shelf compositions. Counter downlighting remains the first visual tier; the wall merchandise is secondary; central merchandise, rear seating and under-seater circuits remain off.

## Deterministic continuity result

- Dimensions: 1624 x 968.
- Best edge registration against exact approved Layer 01: dx=0, dy=0.
- Zero-shift edge correlation: 0.99988043.
- Negative RGB deltas: 0.
- Pixels darker by more than 3 luminance levels: 0%.
- Changed pixels: 18.815075%, confined to intended shelf-wall masks and feathered local spill.
- Full-frame mean luminance shift: +2.695243, attributable only to the released wall-wash family.
- Central ceiling registration anchor: exactly frozen.
- Historical defective Layer 02 pixels reused: no.

## Review evidence

- layer-02-wall-shelf-wall-wash-v4-preview.jpg
- layer-01-vs-layer-02-wall-wash-repair-v4.jpg
- layer-02-wall-shelf-wall-wash-v4-difference.jpg
- SELF_QA.md
- manifest.json
- content-addressed deterministic-qa.json and generation-provenance.json

## GitHub Actions transport

- Artifact name: jarvis-pulla-reddy-v01-l02-c6bb3f56cd3f
- Artifact ID: 9365354131
- Workflow run ID: 32253524484
- Publication commit: fa550aa06ec67c00ddb30373ce15b5df83121a9a
- Artifact archive digest: sha256:71095a2ef12a4fc2d79cff27efa9b1984a1d7926cc6c3d288c57e2fe94030de8
- Downloaded candidate.png SHA-256: c6bb3f56cd3f2f4372c2aaf8d5ada39bbc7b156c270e46a5235498fd41dd7d27
- Candidate manifest and generated artifact provenance match the same candidate hash, publication commit and workflow run.
- Remote retrievability verified: true

Independent candidate-bound JARVIS review is required. V01 remains locked at repaired Layer 02; Layer 03 must not begin without exact approval.
