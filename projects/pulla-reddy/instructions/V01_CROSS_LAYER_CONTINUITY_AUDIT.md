# V01 Main Retail | Cross-Layer Continuity Audit

The exact Final V01 Composite is independently approved under decision:

`jarvis-v01-l08-a059b104-approve-001`

Approved immutable final render:

`a059b10401f0e9b8c3d235630a3e2c43e5e70a3925022a05f65d71744d06bc30`

This task is audit-only. Do not redesign or silently replace any independently approved V01 layer.

## Required action

Create task/layer ID `09` as the V01 Cross-Layer Continuity Audit.

Audit the full approved chain from Source through Layer 00, Layers 01-06, the approved concept sketch, and the exact Final V01 Composite.

For every cumulative transition, compare the exact independently approved child against its exact independently approved parent and verify:

- camera, crop, focal character and perspective remain locked;
- architecture, ceiling grid, counters, shelves, products, furniture and materials remain locked;
- each cumulative layer introduces only its released lighting family;
- all earlier approved lighting families remain frozen in position, apparent CCT, intensity character, beam shape, shadows and reflection behaviour except for physically unavoidable interaction from the newly introduced circuit;
- no global exposure, gamma, contrast or colour lift is used to simulate illumination;
- all added electric lighting reads consistently as 3000K;
- no visible pendant, track, surface fixture, raw LED strip or luminous ceiling-dot condition appears;
- sweet-counter glass remains readable without obvious white bloom, fake glowing edges, duplicated reflections or clipping;
- timber, brass, cream walls, terracotta flooring, white counters and glass respond materially rather than through uniform RGB lifting;
- retail hierarchy remains coherent across the chain: sweets first, wall merchandise second, central merchandise third where visible, hospitality softer, ceiling subordinate;
- the Layer 06 image and Final V01 Composite are byte-for-byte identical and share SHA-256 `a059b10401f0e9b8c3d235630a3e2c43e5e70a3925022a05f65d71744d06bc30`;
- the approved concept sketch remains a communication artifact only and is not a pixel parent.

## Required evidence

Publish:

1. `CROSS_LAYER_QA.md` with one section per parent-child transition and a clear PASS/FAIL conclusion.
2. `cross-layer-metrics.json` containing the exact candidate hashes, dimensions, alignment results, protected-region checks, exposure checks and any detected anomalies.
3. A labeled contact sheet showing Source, Layer 00, Layers 01-06 and Final at identical crop/scale.
4. A second labeled comparison sheet showing each parent-child pair side-by-side or as a compact audit board.
5. A manifest binding every audited image to its exact SHA-256 and prior JARVIS decision ID.
6. Provenance proving the audit used the independently approved masters, not local unapproved alternatives.

Publish the review bundle through the GitHub Actions review-artifact path so the contact sheet and supporting evidence are remotely retrievable.

## Failure handling

If the audit finds any objective defect, do NOT silently rewrite an independently approved master.

Instead:

- identify the earliest affected layer;
- identify exactly which downstream layers depend on it;
- state the defect, location, violated lock and evidence;
- set the audit package to `READY_FOR_JARVIS_REVIEW` with a FAIL result;
- stop for JARVIS control.

JARVIS will decide the smallest safe repair and re-approval path.

## Success handling

If every continuity gate passes, publish the complete audit package, set V01 to `READY_FOR_JARVIS_REVIEW`, and stop.

Do not begin the V01 contact-sheet/review-board task until this exact audit package receives candidate-bound independent JARVIS approval.

Presentation generation remains locked.
