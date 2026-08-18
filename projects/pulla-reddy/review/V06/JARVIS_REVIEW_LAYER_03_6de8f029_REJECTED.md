# V06 Curved Seating Hero | Layer 03 Independent Review

## Decision

**REJECT / DO NOT ADVANCE**

Candidate SHA-256: `6de8f029666f724431a22d80eec24a9f287123fb0aca9f9af751c5f0f3d7bd6f`

Artifact: `9345373457`

## What improved

The correction to the under-seater lighting is materially better than the previously rejected candidate. The visual contribution is reduced, the brightest emission is pulled further under the seating, the floor pool is calmer, and the effect is less like a continuous luminous ribbon. Deterministic QA also confirms the requested contribution reduction and no global exposure shift.

That specific correction should be preserved as the target character when Layer 03 is regenerated later.

## Hard failure found during independent review

The current V06 image still has no continuous integrated planter and no foliage behind the curved built-in seater.

This violates `PROJECT_RULES.md`, which requires the planter to be permanent architecture from Layer 00 onward whenever the curved seating zone is visible.

The shared dependency is also unresolved:

- `projects/pulla-reddy/SHARED_PLANTER_SPEC.md` does not exist.
- V02 still has `approved_through_layer: -1` and is waiting to establish the shared planter and Layer 00.

Therefore this V06 Layer 03 candidate does not sit on a valid reviewer-approved cumulative parent chain containing the mandatory architectural intervention.

## Why this blocks approval

Approving Layer 03 now would legitimise a chain that is architecturally incomplete from Layer 00 onward. Fixing the planter later at Layer 04 would be worse because it would introduce a permanent architectural change in the middle of a lighting sequence and invalidate every preceding comparison.

This is an objective production/control defect, not a user design decision.

## Required correction

1. Freeze V06 at this rejection. Do not create Layer 04.
2. Establish one shared V02/V06 planter design and publish `SHARED_PLANTER_SPEC.md`.
3. Rebuild V06 Layer 00 from the authoritative source with that planter physically present and all electric lighting off.
4. Submit the V06 Layer 00 review package and stop for independent review.
5. After Layer 00 approval, regenerate Layer 01 and Layer 02 sequentially from approved parents.
6. Regenerate Layer 03 only after Layer 02 approval.
7. For the regenerated Layer 03, retain the corrected under-seater character achieved here: source hidden, no luminous furniture outline, approximately 40% lower contribution than the original rejected Layer 03, and only restrained reflected floor glow.
8. Publish parent-versus-candidate evidence at every regenerated stage.

## Locks while repairing the chain

- Camera, perspective and crop locked.
- Original architecture, furniture, tables, chairs, materials and colours locked except for the explicitly mandated planter intervention.
- Planter present but unlit in Layer 00.
- No electric lighting in Layer 00.
- Later electric light remains 3000K and recessed/concealed/integrated only.
- No global exposure or gamma changes.
- Current Layer 03 is not an approved parent.
- Presentation generation remains locked.
