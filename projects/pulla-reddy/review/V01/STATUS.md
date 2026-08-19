# V01 Main Retail | Repaired Layer 05 Rear Seating Comfort Candidate

Status: READY_FOR_JARVIS_REVIEW

Task/layer ID: 05 (sequential repaired-chain rebuild)

Candidate: layer-05-rear-seating-comfort-v5.png

Candidate SHA-256: f8335d6a5081b096e396a62af688dca39dca95d6a007b08cad4467046b6095ca

Approved parent: layer-04-central-merchandise-circulation-v5.png

Approved parent SHA-256: a3d00e7526313425428e1375d0765ad652a12d9ee43883815a83abacc193ba8e

Approved parent decision: jarvis-v01-l04-a3d00e75-approve-002

## Change from approved repaired Layer 04

Only restrained deep-recessed 3000K comfort lighting for the visible rear hospitality tables and seating was added. Approved counter downlighting, repaired wall-wash, repaired concealed shelf lighting, and repaired central-merchandise/circulation lighting remain frozen. The rear seating is readable but remains distinctly softer than every retail tier.

## Deterministic continuity result

- Dimensions: 1624 x 968.
- Best edge registration against exact approved repaired Layer 04: dx=0, dy=0.
- Zero-shift edge correlation: 0.99842083.
- Negative RGB deltas: 0.
- Changed pixels: 2.855095%, confined exactly to the two rear table/seating pools and weaker local-floor zone.
- Changed pixels outside allowed rear zones: 0.
- Full-frame mean luminance shift: +0.231303, attributable only to the released circuit.
- Rear-left seating mean luminance shift: +4.668100.
- Rear-right seating mean luminance shift: +5.107600.
- Rear local-floor support: +0.277200.
- Ceiling, wall shelves, both sweet counters, central merchandise, approved central floor pool, and foreground floor: exactly frozen.
- Maximum channel addition: 36 counts, with warm R > G > B mean ordering in both seating targets.
- Historical defective Layer 05 pixels reused: no.

## Review evidence

- layer-05-rear-seating-comfort-preview.jpg
- layer-04-vs-layer-05.jpg
- layer-04-vs-layer-05-rear-seating-focus.jpg
- layer-05-rear-seating-comfort-v5-difference.jpg
- SELF_QA.md
- manifest.json
- content-addressed deterministic-qa.json and generation-provenance.json

## GitHub Actions transport

- Artifact name: jarvis-pulla-reddy-v01-l05-f8335d6a5081
- Artifact ID: 9372085257
- Workflow run ID: 32270868999
- Publication commit: 7b63b7abb7d1b557341a64951603f5bdad617542
- Artifact archive digest: sha256:395b33d0f4ce09dbe3724cccb05a722f46bba32d94a46a9ffb9f8a03c74c3474
- Downloaded candidate.png SHA-256: f8335d6a5081b096e396a62af688dca39dca95d6a007b08cad4467046b6095ca
- Candidate manifest and generated artifact provenance match the same candidate hash, publication commit, and workflow run.
- Remote retrievability verified: true

Independent candidate-bound JARVIS review is required. V01 is locked at repaired Layer 05 and repaired Layer 06 must not begin without exact approval.
