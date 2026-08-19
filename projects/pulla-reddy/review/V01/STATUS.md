# V01 Main Retail | Repaired Layer 04 Central Merchandise Candidate

Status: READY_FOR_JARVIS_REVIEW

Task/layer ID: 04 (sequential repaired-chain rebuild)

Candidate: layer-04-central-merchandise-circulation-v5.png

Candidate SHA-256: a3d00e7526313425428e1375d0765ad652a12d9ee43883815a83abacc193ba8e

Approved parent: layer-03-concealed-shelf-integrated-lighting-v5.png

Approved parent SHA-256: 8e2a2b196904a132c2c18ffd20f7035cf1689656ccea1c3cc871aa714ccc2bba

Approved parent decision: jarvis-v01-l03-8e2a2b19-approve-002

## Change from approved repaired Layer 03

Only selective deep-recessed 3000K lighting for the central freestanding merchandise display and minimum physically necessary adjacent circulation support was added. Approved counter downlighting, repaired wall-wash and repaired concealed shelf lighting are unchanged. Sweet counters remain first, wall merchandise second and the central display reads as the restrained third tier. Rear seating and under-seater circuits remain at the parent state.

## Deterministic continuity result

- Dimensions: 1624 x 968.
- Best edge registration against the exact approved repaired Layer 03: dx=0, dy=0.
- Zero-shift edge correlation: 0.99850529.
- Negative RGB deltas: 0.
- Pixels darker by more than 3 luminance levels: 0%.
- Changed pixels: 2.844471%, confined exactly to the central-merchandise/minimum-circulation target zones.
- Changed pixels outside allowed central zones: 0.
- Full-frame mean luminance shift: +0.192502, attributable only to the released circuit.
- Central-merchandise mean luminance shift: +6.588640.
- Adjacent-floor mean luminance shift: +3.289053.
- Ceiling, wall shelves, both sweet counters, rear seating and foreground floor: exactly frozen.
- Mean added RGB follows warm order R > G > B in both target regions.
- Historical defective Layer 04 pixels reused: no.

## Review evidence

- layer-04-central-merchandise-circulation-v5-preview.jpg
- layer-03-vs-layer-04-central-merchandise-repair-v5.jpg
- layer-04-central-merchandise-circulation-v5-difference.jpg
- SELF_QA.md
- manifest.json
- content-addressed deterministic-qa.json and generation-provenance.json

## GitHub Actions transport

- Artifact name: jarvis-pulla-reddy-v01-l04-a3d00e752631
- Artifact ID: 9369801718
- Workflow run ID: 32265010608
- Publication commit: 3fc2a5719572009538103abc605e14bda14652e8
- Artifact archive digest: sha256:9b84bdc4be98486e7a586b81f599fdd650f73a674557912846c958106737f944
- Downloaded candidate.png SHA-256: a3d00e7526313425428e1375d0765ad652a12d9ee43883815a83abacc193ba8e
- Candidate manifest and generated artifact provenance match the same candidate hash, publication commit and workflow run.
- Remote retrievability verified: true

Independent candidate-bound JARVIS review is required. V01 remains locked at repaired Layer 04; repaired Layer 05 must not begin without exact approval.
