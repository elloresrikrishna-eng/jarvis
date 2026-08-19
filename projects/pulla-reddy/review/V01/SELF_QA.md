# V01 Layer 02 | Self QA

Candidate: `layer-02-wall-shelf-wall-wash-v3.png`

Candidate SHA-256: `fc47cfc6a1ccbaac2e8103d2b013036716f43395fba0a0c8a393f797dcf1599e`

Approved parent SHA-256: `bb0eda1c017f3be550e9c8a613ed4e1fa5ccc0e8f849c0786fdfd96e841f3217`

## Quality gates

| Gate | Result | Evidence |
|---|---|---|
| Exact approved parent used | PASS | Parent SHA matches the Layer 01 approval decision. |
| Camera, crop and canvas continuity | PASS | Both parent and candidate are 1624 x 968 with matching composition. |
| Architecture and material continuity | PASS | Visual inspection confirms no scene redesign or product movement. |
| Exactly one new lighting family | PASS | Only the wall-shelf wall-wash circuit is added. |
| 3000K warm-white lighting | PASS | Wall-wash is warm, neutral and not orange-contaminated. |
| Recessed or concealed source only | PASS | No visible fixture bodies, tracks, pendants or surface lights. |
| No shelf-integrated light | PASS | No shelf-edge glow, raw strip or shelf-underside source. |
| Approved counter lighting preserved | PASS | Right counter mean shift +0.2008; left counter mean shift -0.1490. |
| Central ceiling protected | PASS | Central ceiling mean shift -0.1301 with no visible ceiling dots. |
| Central display protected | PASS | Mean shift +1.2088, within restrained secondary-bounce tolerance. |
| Rear seating protected | PASS | Mean shift +0.9741, within restrained secondary-bounce tolerance. |
| No global exposure cheat | PASS | Protected cores remain stable while shelf target regions gain about 20.4 to 20.7 luminance levels. |
| No target clipping | PASS | Both wall-wash target regions have zero pixels at luminance 250 or above. |
| Remote artifact integrity | PASS | Downloaded candidate, manifest and provenance all match the exact candidate SHA. |

## Correction record

The first attempt was rejected locally because it lifted protected regions and produced a 1624 x 969 canvas. It was not published.

The final candidate reasserts Layer 01 as the immutable base, localizes the wall-wash to shelf zones, and restores the locked 1624 x 968 canvas.

## Review posture

Deterministic QA is Gate 1 only. Independent external JARVIS review is still required before Layer 03 can be released.
