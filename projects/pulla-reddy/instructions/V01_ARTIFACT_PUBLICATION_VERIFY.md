# V01 Main Retail | Verify Layer 01 Review Artifact Publication

V01 Layer 01 v4 remains UNAPPROVED. Do not regenerate it, do not visually modify it, and do not start Layer 02.

The exact candidate is:

- file: `layer-01-front-display-counter-downlights-v4.png`
- SHA-256: `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217`
- approved parent SHA-256: `17f3d0fdb900ef897762ab4df0f464ea04d6ae09808569073d0c7863cc5b3fd9`
- active manifest: `projects/pulla-reddy/control/review-candidates/pulla-reddy/V01/01/active.json`
- expected artifact name: `jarvis-pulla-reddy-v01-l01-bb0eda1c017f`

## Why this correction is required

The active candidate manifest currently says `READY_FOR_JARVIS_REVIEW`, but it does not record the GitHub Actions workflow run ID or artifact ID. The current coordinator instruction explicitly requires those identifiers and requires the artifact to be remotely retrievable before V01 is considered ready for independent review.

This is a transport/control failure, not a design rejection. The candidate pixels must remain frozen.

## Required machine action

1. Locate the GitHub Actions run triggered by the exact active-manifest publication commit.
2. Confirm the `JARVIS Visual Candidate` workflow completed successfully.
3. Resolve the uploaded artifact named `jarvis-pulla-reddy-v01-l01-bb0eda1c017f`.
4. Record:
   - workflow run ID;
   - artifact ID;
   - artifact name;
   - publication commit SHA;
   - candidate SHA-256;
   - remote retrievability verification.
5. Download or otherwise verify the artifact is actually retrievable and that its `candidate.png` SHA-256 exactly matches `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217`.
6. Update V01 control/review state with those identifiers.
7. Only then set the per-view state to `READY_FOR_JARVIS_REVIEW` and stop for independent JARVIS visual review.

## Frozen items

Do not change:

- candidate image bytes;
- approved Layer 00 parent;
- camera, crop, architecture, materials, products or lighting;
- current design intent;
- Layer 01 QA package.

## Acceptance criteria

V01 is review-ready only when the exact artifact can be retrieved remotely, the candidate hash matches exactly, provenance is valid, workflow run ID and artifact ID are recorded, and Layer 02 remains unstarted.
