# V01 Main Retail | Autonomous Execution Queue

This queue is the released work plan for Codex. Execute tasks in order. Do not skip ahead. After each task, publish the required review package and wait for the next scheduled Jarvis check unless the task explicitly says it may continue automatically.

## Task 01 | Layer 02 Wall-Wash
Starting from approved Layer 01, add only recessed 3000K wall-washer downlights serving all visible wall-mounted shelving compositions. Keep the effect selective, not a blanket wash. Preserve Layer 01 exactly. Publish preview, side-by-side comparison, manifest and self-QA.

## Task 02 | Layer 03 Shelf-Integrated Lighting
Starting from approved Layer 02, add concealed integrated 3000K shelf lighting to all visible wall-mounted shelves. Source hidden. No raw strip lines or visible LED dots. This supplements the wall-wash and must not replace or alter it. Preserve all previous layers exactly. Publish review package.

## Task 03 | Layer 04 Central Merchandise / Circulation
Starting from approved Layer 03, add only the minimum recessed 3000K lighting needed to give central freestanding merchandise displays and circulation selective legibility. Avoid blanket ambient light. Keep the counters strongest in hierarchy. Preserve previous layers exactly. Publish review package.

## Task 04 | Layer 05 Rear Seating Comfort
Starting from approved Layer 04, add only recessed 3000K lighting required for the visible rear seating area. Softer than the retail counter lighting. No pendants. No decorative luminaires. Preserve previous layers exactly. Publish review package.

## Task 05 | Layer 06 Under-Seater Lighting
If a built-in seater is meaningfully visible in View 01, add restrained concealed 3000K under-seater lighting only. If no built-in seater is meaningfully visible, document that the layer is omitted and proceed to the next task without inventing geometry. Preserve previous layers exactly. Publish review package.

## Task 06 | V01 Lighting Concept Sketch
Create the Ashwamedha lighting concept sketch for View 01 using the exact locked camera and architecture. Architecture in restrained charcoal/grayscale. Intended lighting families shown selectively in warm amber/orange. Do not add fixtures or change geometry. Publish a review-sized preview and a short mapping of sketch annotations to rendered layers.

## Task 07 | Final V01 Composite
Confirm that the final render is exactly the last approved cumulative layer with no unlisted lighting, no extra exposure lift and no additional fixture effects. Export a final hero render master. Publish final render preview and final continuity report.

## Task 08 | V01 Cross-Layer Continuity Audit
Run a dedicated cross-layer audit across Layer 00 through final. Check camera/crop, architecture, materials, product/furniture position, ceiling grid, CCT, previous-layer freeze, visibility of luminaires, exposure continuity, glass reflections and hierarchy. If any objective failure is found, repair it autonomously and regenerate only the affected downstream layers as needed. Publish `CROSS_LAYER_QA.md`.

## Task 09 | V01 Contact Sheet / Review Board
Create a clean review contact sheet showing Source, Sketch, Layer 00, Layer 01, Layer 02, Layer 03, Layer 04, Layer 05, Layer 06 if used, and Final in order. Use consistent sizing/crop so progression is easy to judge. Publish review-sized version to Jarvis and keep high-resolution local master.

## Task 10 | V01 Completion Package
Create the complete V01 completion package in Jarvis with `STATUS.md`, `manifest.json`, `SELF_QA.md`, `CROSS_LAYER_QA.md`, final contact sheet, final render preview, and a concise summary of what changed layer by layer. Mark `STATE.json` as `view_complete` only if all mandatory quality gates pass. If a genuine subjective design decision remains, mark `blocked_user_decision` instead.

# Global Rules For Every Task

- 3000K only.
- Recessed/concealed/integrated luminaires only.
- No visible pendants, tracks or surface fixtures.
- Camera, perspective and crop absolutely locked.
- Architecture, ceiling grid, counters, shelves, furniture, materials and products locked.
- Layer N = approved Layer N-1 + exactly one new lighting circuit.
- No global exposure cheating.
- Previous lighting layers frozen.
- Correct objective defects autonomously before review.
- Never ask Srikrishna to solve technical production errors.
