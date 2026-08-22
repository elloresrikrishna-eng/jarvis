# Light the Space V2 — Alya Mentor Architect Specification V1

Status: RELEASE SPECIFICATION
Architect: JARVIS_CHATGPT
Project: light-the-space
Approved foundation head: `781dceb4001076a2aa0340174ebf9d03b7d86946`

## 1. Mission

Judge 1 answers: **Is the lighting solution technically and geometrically admissible?**

Judge 2 answers: **Does the rendered consequence communicate the intended visual hierarchy and perceptual quality?**

Alya Mentor answers: **What should the player understand from those results, and what is the smallest useful next insight that helps them become a better lighting designer?**

Alya Mentor is the teaching layer of Light the Space. It must convert deterministic evidence into concise, specific, confidence-aware coaching without inventing measurements, pretending taste is objective, or silently redesigning the player's solution.

The first challenge remains:

> Make the artwork the hero without making the room uncomfortable.

Alya Mentor V1 should make the player feel that an expert lighting designer is beside them: observant, calm, precise, encouraging, and demanding when necessary.

## 2. Product north star

Alya must not feel like a generic chatbot bolted onto a game.

It should behave like an intelligent design mentor embedded in the lighting workflow.

The player should experience:

1. **Observe** — Alya identifies the most important evidence-backed condition.
2. **Interpret** — Alya explains why it matters in lighting-design language.
3. **Guide** — Alya proposes the smallest useful direction for improvement.
4. **Teach** — Alya names the principle the player is learning.
5. **Challenge** — when appropriate, Alya asks the player to solve the next step rather than giving away a complete answer.

The mentor should create understanding, not dependency.

## 3. Non-negotiable architecture

Preserve the existing evaluation chain:

`SimulationState -> SimulationSnapshot -> Judge 1`

and:

`SimulationState + semantic space + authored viewpoint -> frozen capture -> PerceptualEvidenceSnapshot -> Judge 2`

Add Alya as a separate interpretation layer:

`Judge 1 Result + Judge 2 Result + evidence provenance + authored lesson context -> MentorEvidenceBundle -> Alya Mentor`

Alya must never:

- mutate `SimulationState`
- move, aim, dim, switch, or recolor luminaires
- change camera or exposure
- recompute Judge 1 geometry
- recompute Judge 2 image metrics
- override a Judge verdict
- convert LOW-confidence proxies into certain claims
- invent lux, UGR, photometry, or measured values

Alya consumes evidence. It does not create hidden evidence.

## 4. V1 runtime model

Alya Mentor V1 should have two layers:

### A. Deterministic Mentor Planner

A pure TypeScript planner consumes structured evidence and produces a versioned `MentorPlan`.

The planner decides:

- what issue or success to discuss first
- severity / priority
- applicable teaching principle
- allowed evidence references
- hint depth
- whether to praise, critique, teach, or challenge
- what the player should pay attention to next
- whether the current solution is complete enough for a closing reflection

The planner must be deterministic and fully testable.

### B. Language Realizer

The plan may then be rendered into human-facing copy.

V1 should support a deterministic template realizer first.

An optional LLM adapter may exist behind a strict interface only if it does not become required for correctness, testing, or evaluation. If implemented, the LLM may paraphrase a validated MentorPlan but may not add new claims, metrics, recommendations, actions, or evidence.

The game must remain functional and pedagogically correct without any external AI API.

## 5. Mentor roles

Alya supports four explicit roles.

### TEACH

Used when the player needs a principle explained.

Example style:

> The artwork is brighter than its surroundings, but hierarchy is not only about brightness. A tighter relationship between beam shape and artwork boundary will make the emphasis feel intentional rather than accidental.

### HINT

Used before giving away a solution.

Hints should be progressive.

- Hint 1: directs attention.
- Hint 2: names the relevant variable or relationship.
- Hint 3: gives a more explicit corrective direction.

Alya should not immediately say "use 34° at 70%."

### CRITIQUE

Used after submission or when the player explicitly requests feedback.

Critique should distinguish:

- what is working
- what is limiting the design
- why it matters
- what principle to test next

### CHALLENGE

Used when the solution passes but the player can learn more.

Examples:

- achieve similar hierarchy with less output
- retain the artwork as hero with a different beam angle
- move the fixture while preserving comfort
- create a second valid solution using a warmer/cooler allowed CCT

Challenges must remain within the currently supported simulation capabilities and Judge profiles.

## 6. Evidence bundle

Create a versioned `MentorEvidenceBundle` bound to the exact evaluated design.

Include at minimum:

- bundle version
- level ID
- lesson/challenge ID
- state provenance / canonical state SHA where available
- Judge 1 result version/profile/version
- Judge 1 overall status
- all Judge 1 metric evidence with confidence and limitations
- Judge 2 result version/profile/version
- Judge 2 overall status
- all Judge 2 dimensions with confidence and limitations
- perceptual evidence IDs and viewpoint IDs
- authored lesson objective
- authored learning principles
- player attempt metadata available locally (attempt number / hint depth / prior mentor messages only if already present in session state)

The bundle must be immutable for one mentor response.

Do not allow a response for state A to be attached to state B.

## 7. Teaching principles for the current challenge

Seed an authored principle library for L01 Quiet Evening.

At minimum:

### PRINCIPLE_HIERARCHY

The visual hero should be distinct from its context without requiring the entire scene to become bright.

### PRINCIPLE_BEAM_FIT

Beam distribution should relate intentionally to the size and location of the target.

### PRINCIPLE_RESTRAINT

Good lighting often depends as much on what remains dark as what is illuminated.

### PRINCIPLE_COMFORT

Strong emphasis should not create visually aggressive brightness or expose uncomfortable direct light.

### PRINCIPLE_EFFICIENCY

The desired visual effect should not require unnecessary fixtures or output.

### PRINCIPLE_ITERATION

There can be several good lighting solutions; compare consequences instead of hunting for one magic setting.

Principles must be authored content, not improvised labels.

## 8. Priority model

MentorPlanner must rank findings in a stable order.

Recommended priority:

1. Judge 1 BLOCKING failures
2. Judge 2 BLOCKING dimensions
3. Judge 2 NEEDS_REFINEMENT / WARN findings
4. LOW-confidence caveats that materially affect interpretation
5. successful design principles worth reinforcing
6. optional challenge / exploration

Within the same severity, use authored profile priority rather than arbitrary object order.

Alya should normally discuss one primary issue and at most one secondary issue per response.

Do not dump twelve metrics on the player.

## 9. Feedback progression

Alya Mentor should support a staged learning loop.

### During exploration

Use short observations and hints.

Target length: roughly 1–3 sentences.

### On submission

Use structured critique.

Target shape:

- one sentence: what the design is communicating now
- one sentence: strongest success or failure
- one sentence: next design experiment

### After a PASS

Acknowledge the design principle, then offer an optional challenge.

Do not merely say "Correct" or "100%."

Example:

> The artwork now reads first without flattening the room. You achieved hierarchy through contrast rather than global brightness. Try keeping that hierarchy while reducing output and see how much darkness you can preserve.

## 10. Language style

Alya must sound like a sophisticated lighting mentor, not a game narrator and not a customer-support bot.

Voice:

- concise
- calm
- observant
- technically literate
- human
- confident only when evidence supports confidence
- never patronizing
- never excessively celebratory

Prefer:

- "The artwork is reading clearly, but..."
- "Notice what happens to the wall when..."
- "Your beam is reaching the target, yet the room is losing hierarchy because..."
- "Try changing one variable at a time."

Avoid:

- "Awesome job!!!"
- "You failed."
- "The AI thinks..."
- "Perfect solution."
- unexplained engineering jargon

## 11. Explainability contract

Every MentorPlan statement that contains a factual judgement must carry evidence references.

Conceptually:

```ts
interface MentorClaim {
  claimId: string;
  claimType: "SUCCESS" | "ISSUE" | "CAUTION" | "TEACHING";
  principleId: string;
  evidenceIds: string[];
  confidence: "HIGH" | "MEDIUM" | "LOW";
  limitation?: string;
}
```

The human-facing text need not expose raw evidence IDs, but the developer/debug view must show them.

If evidence confidence is LOW, wording must soften accordingly.

Examples:

HIGH:
> The beam axis is missing the artwork.

LOW:
> This view suggests the highlight may feel aggressive, although the current comfort metric is only a display-referred proxy.

## 12. No hallucination / no hidden design authority

Add explicit guardrails.

Alya must never state:

- a lux value unless that value exists in evidence and is clearly labelled analytical/provisional where applicable
- a UGR value
- code/standards compliance
- fixture performance not present in the catalogue/evidence
- that a subjective composition is universally correct
- that a player must use a specific beam/output if multiple valid solutions exist

If evidence cannot support a statement, the planner must not emit it.

## 13. Hint system

Implement progressive hints for L01.

Each authored principle should have at least three hint depths where applicable.

Example hierarchy hints:

Depth 1:
> Look at what your eye notices first. Is it the artwork or the surrounding wall?

Depth 2:
> Compare the artwork with its immediate context. The difference between them matters more than making the whole scene brighter.

Depth 3:
> Try changing beam width, aim, or output so the artwork gains separation while the wall around it stays quieter.

Hints should reference permitted control families, not exact winning values.

Persist hint depth only in session/game state if a suitable local session model already exists; otherwise keep V1 stateless and return the next requested depth explicitly.

## 14. Success reinforcement

A passing design should generate meaningful positive teaching feedback.

Alya should identify what the player did well based on evidence.

Examples:

- hierarchy achieved with strong target/context separation
- restrained off-target brightness
- acceptable dark retention
- valid mount/aim with efficient fixture count

Avoid praising unsupported aesthetic qualities.

## 15. Multiple valid solutions

This is a hard requirement.

Alya must never teach one hidden answer.

Use the existing Judge 1 and Judge 2 golden PASS cases to prove that MentorPlanner produces sensible feedback for materially different passing solutions.

For different PASS solutions, Alya may reinforce different strengths.

One solution might be praised for restraint; another for stronger hierarchy; another might pass while receiving a challenge to reduce output.

## 16. Submission outcome model

Create an explicit product-level outcome derived from the two judges.

Recommended states:

- `TECHNICAL_CORRECTION_REQUIRED` — Judge 1 blocking
- `VISUAL_REFINEMENT_REQUIRED` — Judge 1 passes, Judge 2 blocking/needs refinement
- `DESIGN_INTENT_ACHIEVED` — both pass

Alya explains the outcome but does not define it independently.

## 17. Player-facing V1 UI

This phase may add the first real Mentor surface, but keep scope controlled.

Create a polished Alya Mentor panel integrated into the Light the Space interaction route.

It should support:

- Alya identity/name
- current mentor role (Teach / Hint / Critique / Challenge) subtly, not as a loud game badge
- primary mentor message
- optional secondary insight
- `Give me a hint` action with progressive depth
- `Critique my design` / submission feedback action
- evidence-aware "Why?" expansion that explains the principle without exposing raw implementation noise
- optional next challenge after PASS

Design direction:

- premium architectural product
- dark graphite/black surface
- restrained white typography
- warm amber/golden light accent
- minimal lime/yellow accent only where useful
- strong spacing
- no cartoon speech bubbles
- no game-console neon
- no excessive gradients
- no cluttered metric dashboard in player view

Developer mode may expose raw plan/evidence IDs separately.

## 18. Interaction behavior

Alya must react only to explicit player actions in V1.

Do not create a constantly chattering mentor.

Allowed triggers:

- player asks for hint
- player submits design
- player asks "why"
- player selects an optional challenge after PASS

Do not interrupt every slider movement.

## 19. Performance and latency

The deterministic MentorPlanner should be effectively instantaneous.

Target:

- planner <= 50 ms typical
- deterministic template realization <= 20 ms typical

If an optional LLM adapter exists later, it must not block the deterministic result. The UI should be able to show the deterministic mentor response immediately.

No runtime FPS regression is acceptable from Alya Mentor.

## 20. Tests

Required groups:

MENTOR BUNDLE
- exact Judge 1/Judge 2 provenance preserved
- state mismatch rejected
- missing required evidence rejected
- limitations preserved

PRIORITY
- Judge 1 blocking outranks Judge 2
- Judge 2 blocking outranks warning
- one primary finding chosen deterministically
- authored priority stable

HINTS
- 3 progressive levels
- later hint is more explicit than earlier hint
- no exact magic settings leaked
- invalid control suggestions impossible

LANGUAGE / CLAIM SAFETY
- claims contain evidence references
- LOW confidence produces qualified wording
- no UGR/standards hallucination
- no unsupported lux claims
- no universal aesthetic claim
- no invented fixture facts

OUTCOMES
- technical correction required
- visual refinement required
- design intent achieved

MULTIPLE VALID SOLUTIONS
- existing materially distinct Judge PASS cases receive coherent mentor feedback
- no exact-state matching

DETERMINISM
- same evidence bundle + same role + same hint depth produces byte-stable MentorPlan
- deterministic template realizer stable

ARCHITECTURE
- planner is pure TypeScript
- no React/Three/R3F/Zustand/browser imports in planner
- no renderer/evaluator mutation
- optional LLM adapter cannot bypass plan validation

REGRESSION
- all Judge 1 tests pass
- all Judge 2 tests/browser evidence pass
- Phase 2 interaction unaffected

UI / BROWSER
- Mentor panel renders
- Hint/Critique/Why actions work
- design state is unchanged by mentor actions
- screenshots demonstrate premium readable layout

## 21. Artifacts

Publish at minimum:

- `artifacts/alya-mentor/mentor-plans.json`
- `artifacts/alya-mentor/golden-feedback-cases.json`
- `artifacts/alya-mentor/claim-safety.json`
- `artifacts/alya-mentor/architecture-invariants.json`
- `artifacts/alya-mentor/browser-acceptance.json`
- clean screenshots of Mentor UI for:
  - technical blocking critique
  - visual refinement critique
  - first hint
  - deeper hint
  - successful design reflection/challenge

## 22. Documentation

Create:

`docs/LTS_V2_ALYA_MENTOR.md`

Document:

- role in architecture
- evidence bundle
- planner
- mentor roles
- priority logic
- hint progression
- claim/evidence contract
- confidence language
- multiple-valid-solution behavior
- deterministic fallback
- optional future LLM adapter boundary
- UI interaction model
- limitations

## 23. Forbidden scope

Do not implement:

- autonomous lighting design
- automatic fixture movement/aim/output changes
- voice/avatar/video
- cloud memory
- user accounts/auth
- campaign XP/badges
- final 30-level progression
- new room environment
- LLM visual judging
- Alya overriding Judge 1/Judge 2
- OpenAI/Anthropic/Gemini as a required runtime dependency
- automatic merge

Do not modify Pulla Reddy.

## 24. Human product acceptance

Alyа Mentor V1 is acceptable only if a user can:

1. create a technically invalid solution and receive a precise technical critique
2. fix technical validity but leave weak visual hierarchy and receive perceptual refinement guidance
3. ask for Hint 1 and receive direction without answer leakage
4. ask for deeper hint and receive more actionable guidance
5. submit a passing design and receive evidence-backed reinforcement
6. choose an optional challenge that encourages another valid solution
7. use `Why?` and understand the lighting principle behind the feedback
8. confirm that Alya never changes the design itself

The experience should feel like **learning lighting design with an expert beside you**, not reading error messages.

## 25. Acceptance gate

Alya Mentor V1 passes only if:

- foundation is exactly the approved Judge 2 head `781dceb4001076a2aa0340174ebf9d03b7d86946`
- Judge 1 remains unchanged and passing
- Judge 2 remains unchanged and passing
- MentorPlanner is deterministic and evidence-bound
- claims are traceable to evidence
- confidence/limitations are preserved
- hint progression is implemented
- no magic-answer leakage occurs
- multiple valid solutions remain valid
- Alya cannot mutate design state
- deterministic template realization works without external AI
- UI proof is premium and usable
- browser acceptance/screenshots are published
- tests/typecheck/lint/build pass
- no normal interaction performance regression is introduced

## 26. JARVIS review contract

When implementation completes, JARVIS must independently verify and publish an immutable review package bound to exact base/head SHA.

External JARVIS review must inspect:

- code diff
- MentorPlan schema/planner
- evidence binding
- claim safety
- priority behavior
- hints
- multiple valid solution cases
- UI screenshots
- browser acceptance
- regression suite

Do not self-approve.

Stop at `READY_FOR_JARVIS_REVIEW`.

## 27. Release intent

This specification is approved for implementation as the next Light the Space phase.

JARVIS may prepare and execute `ALYA_MENTOR` only after verifying the approved foundation head `781dceb4001076a2aa0340174ebf9d03b7d86946` and consuming this specification through the normal safe project/task release mechanism.

Do not merge automatically.
Do not begin the Five-Level MVP or environment expansion automatically after Alya Mentor. Stop for external JARVIS review and subsequent architect release.
