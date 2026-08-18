# G Pulla Reddy Sweets | 10-Step Autonomous Production Pipeline

This file defines the ordered production queue for V01_Main_Retail and the transition into final presentation assembly.

The purpose is to let Codex work in meaningful chunks while giving the reviewer a strict approval gate between chunks.

## Global rule

Codex may execute only the CURRENT released step. After each step, it must publish a review package and move to `waiting_for_chatgpt_review` unless the instruction explicitly allows a two-layer chunk. ChatGPT/reviewer must either APPROVE and release the next step, or REJECT with exact corrections and keep the same step active.

A rejection must never be vague. It must state:
- what is wrong;
- why it fails the lighting/design intent;
- what must remain unchanged;
- exactly what needs to change;
- the acceptance criteria for the corrected version.

## Step 1 | Layer 02: Recessed wall-wash to wall-mounted shelving
Starting from approved Layer 01, add only recessed 3000K wall-washer downlights serving all visible wall-mounted shelving compositions. No integrated shelf lighting yet. Keep the counter lighting exactly frozen.

Approval focus: vertical readability, controlled wall grazing/washing, no blanket flood, no fixture visibility, no global ambient lift.

## Step 2 | Layer 03: Concealed integrated shelf lighting
Starting from approved Layer 02, add only concealed 3000K shelf-integrated lighting to all wall-mounted shelves, inspired by the user's office Minions display shelf. Source must be hidden. No raw strip, no LED dots, no shelf becoming a glowing line.

Approval focus: product emphasis, hidden source, natural wood/brass rendering, wall-wash from Layer 02 unchanged.

## Step 3 | Layer 04: Central merchandise/circulation emphasis
Starting from approved Layer 03, add the minimum recessed 3000K lighting required to make central merchandise displays and circulation legible. Use selective pools, not blanket ambient light.

Approval focus: hierarchy remains sweets first, wall shelves second, centre displays third. Ceiling should not become dominant.

## Step 4 | Layer 05: Rear seating comfort
Starting from approved Layer 04, add only recessed 3000K local lighting for the visible rear seating/hospitality zone.

Approval focus: softer and calmer than retail counter lighting; no pendants; no decorative fixtures; hospitality contrast distinct from sales zone.

## Step 5 | Layer 06: Under-seater light if visible
If a built-in seater is meaningfully visible in V01, add concealed 3000K under-seater lighting only. If not meaningfully visible, formally mark this layer NOT_APPLICABLE and do not invent geometry.

Approval focus: restrained floating glow, no exposed strip source, no exposure lift.

## Step 6 | Final cumulative V01 render
Create the final V01 render as the last approved cumulative layer only. Add no new lighting family, no exposure boost, no colour-grade cheat, no architecture change.

Approval focus: commercial hierarchy, appetising sweets, glass reflection control, visual comfort, ceiling restraint, overall Ashwamedha quality.

## Step 7 | V01 concept sketch
Create the Ashwamedha-style lighting concept sketch from the approved V01 final lighting design.

Requirements:
- architecture in restrained charcoal/grayscale;
- lighting effects and intended beams in warm amber/orange only;
- same camera/composition;
- clearly communicate each lighting family without becoming diagram-heavy.

Approval focus: clarity, elegance, visual consistency with Ashwamedha sketch language.

## Step 8 | V01 sequence QA + contact sheet
Produce one consolidated QA package containing:
- source;
- Layer 00;
- every approved layer;
- final render;
- sketch;
- contact sheet in correct sequence;
- continuity report;
- camera/crop alignment report;
- cumulative-lighting verification;
- final self-QA.

No new rendering is allowed in this step except correction of an identified failure.

Approval focus: sequence integrity and cumulative logic.

## Step 9 | Presentation reference study
Before assembling the Pulla Reddy presentation, inspect the Art Villa and Purva Bluebelle presentation files placed directly in the root of `D:/Codex/G Pulla Reddy Sweets` alongside the source Pulla Reddy presentation.

Extract their presentation grammar, including:
- title/section card language;
- sketch placement;
- layered-render sequence;
- final-render pages;
- fixture-reference treatment where relevant;
- Ashwamedha branding rhythm;
- typography, spacing, full-bleed behaviour and visual restraint.

Do not blindly copy either deck. Use them as authoritative style references and adapt the grammar to an interior retail project.

Publish a concise `PRESENTATION_STYLE_ANALYSIS.md` for review before assembly.

## Step 10 | Build Pulla Reddy presentation
After presentation-style approval, assemble the first complete Pulla Reddy presentation in `02_Presentation` using only approved imagery.

For V01 include, at minimum:
- project / section title;
- V01 lighting concept sketch;
- Layer 00;
- approved cumulative layers in order;
- final render;
- fixture references only if useful.

If additional views have been completed by then, include only those whose final sequences are approved.

Export PPTX and PDF.

Final approval focus: Ashwamedha presentation quality, sequence logic, image quality, no accidental crop/bleed issues, no generic AI-deck feel.

## Reviewer behaviour

For every step, the reviewer must make one of three decisions:

### APPROVE
State why it works and release the next step.

### REJECT_AND_CORRECT
State exactly what failed, why it failed, what must remain frozen, the required correction, and measurable/visual acceptance criteria. Keep the same pipeline step active until corrected.

### ESCALATE_USER
Use only when there is a genuine subjective design decision that cannot be resolved from project rules, source material, or prior approvals.

Technical defects are NEVER user escalations.
