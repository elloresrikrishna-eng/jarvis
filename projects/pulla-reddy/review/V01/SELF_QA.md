# V01 Layer 01 | Self QA

| Quality gate | Result | Evidence |
|---|---|---|
| Camera and crop continuity | PASS | Both masters are 1624 x 968. Best edge alignment offset is x=0, y=0. |
| Architecture continuity | PASS | Final master is approved Layer 00 plus positive-only light contribution. |
| Ceiling-grid continuity | PASS | Grid geometry is inherited from Layer 00. Apertures are small, dark and deep recessed. |
| Furniture and product continuity | PASS | No product, counter, shelf or furniture movement detected. |
| Previous-layer freeze | PASS | No RGB channel is darker than Layer 00. Tested protected regions are exact parent pixels. |
| Exact released circuit only | PASS | Only the long right counter and secondary left front counter receive downlighting and local spill. |
| 3000K lighting | PASS | Added contribution is warm 3000K with no cool or mixed-CCT source. |
| No visible non-recessed luminaires | PASS | No pendant, track or surface fixture is present. Recessed apertures remain visually quiet. |
| No global exposure cheat | PASS | Rear, central-display and wall-shelf control regions have zero luminance change. |
| No wall-wash or shelf-integrated light | PASS | Both wall-shelf control regions are exact Layer 00 pixels. |
| No central-display, circulation or rear seating light | PASS | Central and rear control regions are exact Layer 00 pixels. |
| Counter hierarchy | PASS | Right counter is strongest, with restrained secondary emphasis on the left counter. |
| Glass reflection control | PASS | No obvious white blobs, blown reflections, bloom or mirror-like glare detected. |
| Rendering defects | PASS | No seam, crop mismatch, geometry break, added object, haze or watermark detected. |

## Autonomous correction record

The first proposal was rejected internally because ceiling apertures were visually bright. A later quantitative check found unrelated zones had darkened. The published candidate corrects both issues by using quiet recessed apertures and compositing only positive lighting contribution over the approved parent.

## Overall assessment

Reasonably compliant and ready for ChatGPT review.

## Uncertainty

Fine variation within the intentionally illuminated counter regions may remain from the generative lighting proposal. Independent review should focus on glass behavior, appetising product rendering and preferred counter-light intensity.
