# G Pulla Reddy Sweets | Parallel Multi-View Execution Plan

## Objective
Run Views 01-06 in parallel as independent production lanes, while preserving one shared lighting language and strict cross-view continuity.

## Core model
- Each view has its own local view folder and its own production lane.
- Each view may progress independently through its layer queue.
- A view must still stop at each review gate unless explicitly released for a batch of steps.
- Cross-view architectural elements, especially the curved-seater planter intervention, are shared assets and must remain visually consistent wherever the same physical zone appears.
- Final presentation assembly begins only after every view is independently approved.

## Source mapping
Use the root project PDF `26.08.12 -G Pulla Reddy-HSR-Sweets-3D View.pdf` as the authoritative source.

- V01_Main_Retail = page 2 / 3D VIEW 01
- V02_Curved_Seating = page 3 / 3D VIEW 02
- V03_Reverse_Retail = page 4 / 3D VIEW 03
- V04_Product_Elevation = page 5 / 3D VIEW 04
- V05_Window_Shelving = page 6 / 3D VIEW 05
- V06_Curved_Seating_Hero = page 7 / 3D VIEW 06

## Shared global rules
All views obey `PROJECT_RULES.md`.

Hard locks:
- 3000K only
- recessed / concealed / integrated lighting only
- no visible pendants, tracks or surface luminaires
- camera, crop, perspective, architecture, materials, furniture, products and ceiling grid locked
- no global exposure cheating
- previous approved layers frozen
- Layer N = approved Layer N-1 + exactly one new lighting family
- all wall-mounted shelves receive recessed wall-wash plus concealed integrated shelf lighting
- all front sweet display counters receive controlled recessed downlighting
- all built-in seaters receive restrained under-seater lighting where visible
- curved seating zone receives the permanent planter intervention from Layer 00 onward
- planter lighting must create soft foliage shadow play on the background wall

# View lanes

## V01_Main_Retail
Existing active lane. Continue using `V01_EXECUTION_QUEUE.md`.

## V02_Curved_Seating
Source: page 3.
Permanent Layer 00 intervention: continuous integrated planter behind the curved seating. Use a calm planting rhythm suitable for soft foliage shadows. This exact planter character becomes the cross-view reference for V06.

Suggested layer queue:
1. Layer 00 night base with planter present, all lights off.
2. Recessed wall-wash / shelf-composition lighting for visible wall shelves.
3. Concealed shelf-integrated lighting.
4. Recessed seating/table comfort lighting, soft and low contrast.
5. Concealed under-seater lighting to the curved built-in seater.
6. Concealed/recessed planter lighting producing soft foliage shadows on rear wall.
7. Minimum residual circulation support only if physically necessary.
8. Final cumulative render.
9. Concept sketch.
10. Cross-layer QA + contact sheet + completion package.

Hierarchy: hospitality first, shelving second, architecture third. Avoid turning this into a retail-bright scene.

## V03_Reverse_Retail
Source: page 4.
Suggested layer queue:
1. Layer 00 night base.
2. Recessed downlighting over visible sweet display counter(s).
3. Recessed wall-wash to wall-mounted shelves.
4. Concealed shelf-integrated lighting.
5. Selective central merchandise/circulation lighting.
6. Rear/background seating support only if visible and useful.
7. Final cumulative render.
8. Concept sketch.
9. Cross-layer QA + contact sheet + completion package.

Hierarchy: sweet counter remains strongest even with storefront/daylight context removed for night scene.

## V04_Product_Elevation
Source: page 5.
This is a hero merchandising elevation.

Suggested layer queue:
1. Layer 00 night base.
2. Controlled recessed downlighting over the long glass sweet counter.
3. Recessed wall-washer downlights to the wall shelf composition.
4. Concealed integrated shelf lighting to all visible wall-mounted shelves.
5. Checkout/service counter support only if needed.
6. Final cumulative render.
7. Concept sketch.
8. Cross-layer QA focused heavily on glass reflections, product colour and vertical hierarchy.
9. Contact sheet + completion package.

Hierarchy: sweets first, wall merchandise second, architecture third. Counter glass must not show ugly white hotspots.

## V05_Window_Shelving
Source: page 6.
Suggested layer queue:
1. Layer 00 night base.
2. Recessed wall-wash serving the wall-mounted shelves.
3. Concealed integrated shelf lighting inspired by the office Minions display shelf.
4. Minimal local recessed accent for any sweet trays / key merchandise not sufficiently served by shelf light.
5. Soft architectural support to brass/timber only if needed without making brass flashy.
6. Final cumulative render.
7. Concept sketch.
8. Cross-layer QA + contact sheet + completion package.

Hierarchy: intimate shelf merchandising. Products should feel edible first, premium second.

## V06_Curved_Seating_Hero
Source: page 7.
This is the hero seating / planter-shadow view.

Permanent Layer 00 intervention: same planter geometry, planting rhythm, height, density and material language established in V02. Do not independently redesign it.

Suggested layer queue:
1. Layer 00 night base with shared planter present, all lights off.
2. Recessed table/seating comfort lighting.
3. Concealed under-seater lighting.
4. Recessed wall-wash / any visible shelf lighting if present.
5. Concealed integrated shelf light if visible.
6. Planter lighting producing soft organic foliage shadows across the rear wall.
7. Subtle vertical architectural light elements only if they already belong to the design intent and do not compete with people/tables.
8. Final cumulative render.
9. Concept sketch.
10. Cross-layer QA + contact sheet + completion package.

Hierarchy: seating comfort and foliage-shadow atmosphere are the hero. Keep the scene calm, not theatrical.

# Parallelism rules

1. Views may render simultaneously.
2. Never let one view overwrite another view's files or state.
3. Each view must publish to a dedicated Jarvis review path:
   - `projects/pulla-reddy/review/V01/`
   - `projects/pulla-reddy/review/V02/`
   - ... through V06.
4. Use per-view state files under `projects/pulla-reddy/state/` once created.
5. V02 and V06 share a cross-view planter lock. The first approved planter geometry becomes authoritative for both.
6. Global lighting language must remain consistent across all views: same apparent CCT, fixture concealment, wall-wash character, shelf-light character, contrast philosophy and material response.
7. A view can be corrected without blocking unrelated views unless the correction changes a shared cross-view rule.
8. Presentation assembly is blocked until all six views have completion packages and independent approval.

# Presentation gate
After all views are approved:
1. Study the Art Villa and Purva Bluebelle reference presentations placed in the local project root.
2. Extract their presentation grammar, spacing, title/section language, sketch placement, layer sequencing, final-render treatment and overall Ashwamedha visual character.
3. Submit that style analysis for reviewer approval.
4. Assemble the complete Pulla Reddy PPTX and PDF only after style approval.
5. Run a final presentation QA for sequence, image crop consistency, typography, slide rhythm, missing layers, duplicate assets, and visual hierarchy.
