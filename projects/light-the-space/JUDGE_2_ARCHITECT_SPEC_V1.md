# Light the Space V2 — Judge 2 Architect Specification V1

Status: RELEASE SPECIFICATION
Architect: JARVIS_CHATGPT
Project: light-the-space
Approved foundation head: `30cb150e9e36292325f4069f317571a356db1037`

## 1. Mission

Judge 1 answers: **Is the solution technically and geometrically admissible?**

Judge 2 answers: **Does the lighting actually communicate the intended visual hierarchy and feel intentional from the human viewpoints that matter?**

Judge 2 must move Light the Space from a geometry simulator toward a lighting-design learning system. It is not an LLM, not Alya, not a personality score, and not a replacement for Judge 1.

The first challenge remains:

> Make the artwork the hero without making the room uncomfortable.

Judge 2 V1 must evaluate the rendered consequence of a valid design from authored viewpoints while preserving fixed exposure and the exact player state.

## 2. Non-negotiable architecture

Preserve this chain:

`SimulationState -> SimulationSnapshot -> Judge 1`

Add a separate perceptual branch:

`SimulationState + SpaceDefinition + authored viewpoints -> deterministic render capture -> PerceptualEvidence -> Judge 2`

Then later:

`Judge 1 + Judge 2 -> Alya Mentor`

Judge 2 must not mutate SimulationState, rerun geometry rules already owned by Judge 1, change exposure, alter luminaire output, or infer hidden photometry.

Judge 2 must never silently substitute renderer settings that change the lighting design.

## 3. Evidence, not taste

Create a versioned `PerceptualEvidenceSnapshot` produced from deterministic captures of authored evaluation viewpoints.

It must include at least:

- evidence version
- level ID
- space ID/version
- render profile ID/version
- exact candidate state revision/hash if available; otherwise explicit state provenance fields already available
- viewpoint ID
- image dimensions
- fixed exposure value
- target-region screen mask or projected polygon
- protected comfort-region masks where applicable
- image-space luminance statistics
- target luminance statistics
- surrounding-wall luminance statistics
- brightest-region statistics
- highlight/clipping fraction
- shadow-crush / near-black fraction
- target-to-context contrast ratio
- target prominence ratio
- target visual-area share
- off-target bright-pixel share
- spatial brightness distribution / entropy or another documented concentration metric
- screenshot artifact path and SHA-256
- explicit limitations

All evidence calculations must be deterministic and renderer-independent after capture.

## 4. Deterministic render capture

Add a browser/evidence capture path dedicated to Judge 2.

Requirements:

- capture authored evaluation viewpoints only
- fixed ACES exposure remains exactly `0.72`
- no adaptive exposure
- no camera auto-framing
- no user UI in evidence captures
- no debug overlays in the pixels being measured
- deterministic canvas size
- deterministic DPR
- deterministic HIGH/BALANCED policy chosen and versioned for perceptual evidence
- same state must produce byte-stable evidence JSON and materially stable image metrics
- capture metadata must record renderer/profile/version

Judge 2 V1 may use BALANCED if HIGH cannot meet evidence runtime constraints, but the evidence profile must be frozen and must not change state, exposure, CCT, output, beam, or geometry.

## 5. Target projection

Judge 2 must know where the artwork is in screen space without asking an AI model.

Use the existing semantic target rectangle and authored camera/viewpoint transforms to project the artwork target into screen coordinates.

Produce a target mask/polygon per evaluation viewpoint.

Do not use hand-painted pixel coordinates.

If the target is not visible from a viewpoint, that viewpoint must say so explicitly rather than fabricate target metrics.

## 6. Judge 2 V1 dimensions

Judge 2 V1 evaluates five perceptual dimensions.

### A. Visual Hierarchy

Question:

> Does the artwork read as the visual hero?

Evidence examples:

- target median luminance vs immediate context
- target high-percentile luminance vs room high-percentile luminance
- target prominence ratio
- fraction of the room's highest-luminance pixels that occur on/near the artwork

The artwork does not need to be the single brightest pixel. Avoid rewarding tiny specular hotspots.

### B. Restraint

Question:

> Is the emphasis achieved without lighting unrelated surfaces excessively?

Evidence examples:

- off-target bright-area fraction
- brightness concentration outside the artwork zone
- wall spill prominence
- proportion of top luminance percentile outside authored emphasis region

Judge 2 must not duplicate Judge 1's geometric spill rule. This is rendered consequence, not cone geometry.

### C. Comfort

Question:

> Does the rendered view avoid visually aggressive brightness?

V1 may use perceptual proxies only.

Evidence examples:

- clipped/highlight fraction
- extreme local contrast near authored eye/view zones
- very bright source/hotspot area fraction
- luminance percentile spread

Do not call this UGR, disability glare, discomfort glare rating, or a standards-compliant metric.

### D. Legibility / Dark Retention

Question:

> Does the room remain readable without becoming flat or crushed?

Evidence examples:

- near-black pixel fraction in authored useful scene region
- mid-tone occupancy
- target/context separation
- clipping-vs-crush balance

Do not reward simply making the entire frame brighter.

### E. Composition / Balance

Question:

> Does the lighting distribution feel intentionally composed rather than random?

Use deterministic image-space proxies such as:

- luminance centroid relative to authored emphasis region
- bright-region fragmentation count
- concentration/entropy metric
- left/right or upper/lower imbalance only where authored viewpoint policy declares it meaningful

Do not pretend these metrics are universal aesthetic truth. They are authored perceptual proxies for this challenge.

## 7. Result structure

Create a versioned `Judge2Result`.

Each dimension must report:

- dimension ID
- measured evidence values
- target band(s)
- PASS / WARN / BLOCKING
- confidence HIGH / MEDIUM / LOW
- source evidence IDs
- limitation
- explanation key
- evaluator version
- perceptual profile version

Judge 2 V1 should expose dimension verdicts, not one opaque percentage.

An optional overall status may be:

- PASS
- NEEDS_REFINEMENT
- BLOCKING

Rules must be explicit and profile-driven.

## 8. Relationship to Judge 1

Judge 2 must never overturn a Judge 1 blocking failure.

Product pipeline:

1. Judge 1 evaluates admissibility.
2. If Judge 1 is BLOCKING, Judge 2 may be skipped or marked `NOT_EVALUATED_JUDGE_1_BLOCKING`.
3. If Judge 1 passes, Judge 2 evaluates rendered perceptual consequence.

Judge 2 must consume the exact same design state/candidate provenance.

## 9. Multiple valid solutions

This is critical.

Judge 2 must not encode one magic screenshot.

Create at least five authored/golden design states:

- three materially different PASS solutions
- one NEEDS_REFINEMENT solution
- one clearly BLOCKING perceptual solution

Passing solutions should vary at least two of:

- beam angle
- output
- fixture position within valid mount
- aim point within artwork
- CCT within Judge 1 profile

A solution should be judged by intent outcome, not by matching one set of fixture coordinates.

## 10. Anti-gaming requirements

Add adversarial cases proving:

- globally brightening the scene is impossible because exposure is fixed
- a tiny overbright hotspot on the artwork does not automatically win hierarchy
- making the entire wall bright does not satisfy artwork prominence
- a technically valid but visually flat scene does not receive a strong hierarchy PASS
- a technically valid but extremely dim scene does not pass legibility/hierarchy
- a technically valid but clipped/harsh scene is penalized on comfort
- geometry-good spill but visually dominant off-target brightness is caught by Judge 2 restraint

## 11. Image metric implementation

Prefer a small pure TypeScript image-analysis module operating on deterministic RGBA buffers.

No cloud API is required for Judge 2 V1.

Do not add OpenAI/Anthropic/Gemini vision calls to the runtime judge.

If a lightweight image library is required, justify it and avoid native dependencies that complicate the Windows worker.

Prefer browser canvas/ImageData or pure JS/TS processing.

## 12. Perceptual profile

Create a versioned profile for the current challenge, conceptually:

`L01_QUIET_EVENING_JUDGE_2`

Thresholds must live in profile data with rationales.

Do not bury threshold literals in evaluator functions.

Document which thresholds are:

- physically motivated
- perceptually motivated
- authored gameplay thresholds
- provisional calibration values

## 13. UI proof

Add a developer-only Judge 2 evidence panel or route, not final game UX.

It should allow inspection of:

- selected evaluation viewpoint
- clean rendered capture
- target polygon/mask overlay shown only in debug mode
- key perceptual metrics
- dimension verdicts
- evidence provenance

The production render itself must remain untouched.

## 14. Performance

Judge 2 evidence does not need to run at 60 FPS.

It must, however, be bounded and predictable.

Target for one full Judge 2 evaluation across the authored V1 viewpoints on the existing machine:

- preferred <= 5 seconds after render is ready
- hard acceptance <= 15 seconds

Report capture time, image-analysis time, total evaluation time, and evidence image sizes.

Do not degrade normal interactive FPS to support Judge 2.

## 15. Tests

Required test groups:

PURE IMAGE METRICS
- luminance conversion
- percentile stability
- target mask statistics
- clipping/crush fractions
- concentration/entropy metric
- deterministic output

TARGET PROJECTION
- artwork polygon projects correctly for authored viewpoints
- hidden/out-of-frame target handled explicitly

JUDGE 2 PROFILE
- versioned thresholds
- rationale completeness
- no hidden literals controlling verdicts

GOLDEN SOLUTIONS
- at least 3 materially distinct PASS designs
- 1 NEEDS_REFINEMENT
- 1 BLOCKING

ADVERSARIAL
- hotspot gaming
- globally flat bright wall
- underlit valid geometry
- harsh/clipped valid geometry
- off-target visual dominance

ARCHITECTURE
- Judge 2 does not import React, R3F, Three, Zustand, browser globals in pure evaluator modules
- renderer adapter owns capture only
- image-analysis core owns pixel evidence
- evaluator owns policy comparison only
- no LLM/API dependency

BROWSER EVIDENCE
- deterministic authored viewpoints
- fixed exposure 0.72 preserved
- no UI/debug overlay contaminating measured pixels
- screenshots and JSON artifacts produced

FULL REGRESSION
- all existing Judge 1 tests remain passing
- Phase 2 interaction remains unchanged

## 16. Artifacts

Publish at minimum:

- `artifacts/judge-2/judge-2-evidence.json`
- one clean screenshot per evaluated viewpoint
- optional debug overlay screenshot(s), clearly separate from measured captures
- `artifacts/judge-2/architecture-invariants.json`
- `artifacts/judge-2/golden-cases.json`
- `artifacts/judge-2/performance.json`

## 17. Documentation

Create:

`docs/LTS_V2_JUDGE_2.md`

Document:

- purpose
- architecture
- evidence pipeline
- image metrics
- target projection
- perceptual dimensions
- profile thresholds and rationale classes
- limitations
- anti-gaming cases
- performance
- relationship to Judge 1
- boundary with future Alya Mentor

## 18. Forbidden scope

Do not implement:

- Alya Mentor
- LLM visual judgement
- Judge 3
- campaign progression
- accounts/auth
- persistence/backend
- final player-facing scoring UI
- badges/XP
- new room/level
- IES engine
- standards-compliant glare calculation
- automatic merge

Do not modify Pulla Reddy.

## 19. Acceptance gate

Judge 2 V1 is acceptable only if:

- exact approved Judge 1 head is preserved as foundation
- Judge 1 still passes
- fixed exposure 0.72 remains invariant
- deterministic perceptual evidence is generated from authored viewpoints
- target projection is semantic, not hardcoded pixels
- five perceptual dimensions exist
- thresholds are profile-driven/versioned
- at least 3 materially distinct designs pass
- obvious visually bad but technically valid scenes fail or need refinement
- adversarial gaming cases are covered
- no LLM/cloud dependency exists
- no runtime FPS regression is introduced for normal interaction
- full tests/typecheck/lint/build pass
- browser evidence is published

## 20. JARVIS review contract

When implementation finishes, JARVIS must independently verify and publish a package bound to exact base/head SHA.

External JARVIS review must inspect:

- code diff
- image-analysis semantics
- profile thresholds
- golden cases
- adversarial cases
- clean screenshots
- evidence JSON
- performance artifact
- regression suite

Do not self-approve.

Stop at `READY_FOR_JARVIS_REVIEW`.

## 21. Release intent

This specification is approved for implementation as the next Light the Space phase.

JARVIS may prepare and execute Judge 2 only after its local dispatcher consumes this specification through the normal safe project/task release mechanism.

Do not merge Judge 1 or Judge 2 automatically.
