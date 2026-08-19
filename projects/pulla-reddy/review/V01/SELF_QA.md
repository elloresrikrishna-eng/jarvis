# V01 Layer 03 | Self QA

Candidate: `layer-03-concealed-shelf-integrated-lighting-v3.png`

Candidate SHA-256: `9c855ce50bea0032a17e0b6a230d7282dc1c078116dc0210b7fd33bcc525b6af`

Approved parent SHA-256: `fc47cfc6a1ccbaac2e8103d2b013036716f43395fba0a0c8a393f797dcf1599e`

## Quality gates

| Gate | Result | Evidence |
|---|---|---|
| Exact approved parent used | PASS | Parent SHA matches `jarvis-v01-l02-fc47cfc6-approve-001`. |
| Camera, crop and canvas continuity | PASS | Parent and candidate are 1624 x 968 with matching composition. |
| Architecture, material and product continuity | PASS | The approved parent is preserved pixel-for-pixel outside the permitted shelf zones. |
| Exactly one new lighting family | PASS | Only concealed shelf-integrated 3000K lighting is added. |
| Hidden source | PASS | No raw strip line, LED dots or bright shelf-edge ribbon remains. |
| Brass supports remain non-luminous | PASS | Brass receives restrained material highlights only. |
| Approved Layer 01 counter lighting preserved | PASS | Both protected counter cores have 0.0000 mean luminance shift. |
| Approved Layer 02 wall-wash preserved | PASS | Existing wall gradients remain, with only local shelf interaction. |
| Central ceiling protected | PASS | Mean shift +0.0004, with no visible new aperture or source. |
| Central display protected | PASS | Mean shift 0.0000. |
| Rear seating protected | PASS | Mean shift 0.0000. |
| Circulation floor protected | PASS | Mean shift 0.0000. |
| No global exposure cheat | PASS | Global shift is only +0.658515 and no pixels change outside the shelf-local masks. |
| No target clipping | PASS | Combined shelf target clipping fraction at luminance 250 or above is 0.0. |
| 3000K warm-white character | PASS | Merchandise glow is warm, restrained and not orange-contaminated. |
| No visible pendant, track or surface fixture | PASS | No new fixture body is introduced. |
| Remote artifact integrity | PASS | Downloaded candidate, manifest and provenance all bind to the exact candidate SHA, publication commit and workflow run. |

## Correction record

The first Layer 03 draft was rejected locally because the shelf-edge emission read as a visible luminous line.

The second draft was rejected locally because it weakened the approved wall-wash and darkened protected regions.

The final candidate reasserts the exact approved Layer 02 parent outside three tight shelf zones and carries only a restrained positive integrated-light contribution inside those zones.

## Artifact evidence

- Workflow run: `32219997021`
- Artifact ID: `9353602039`
- Archive digest: `sha256:744ea00bed8c71841f81b0ec870d4b5f23d1143339e843e3dd0f89ea41f2c362`
- Publication commit: `35a099ec992d999bd0a3582413c9d3f63c878d0a`

## Review posture

Deterministic QA and artifact publication are Gate 1 only. Independent external JARVIS review is still required before Layer 04 can be released.
