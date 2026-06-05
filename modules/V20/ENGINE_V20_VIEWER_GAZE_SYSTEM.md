# ENGINE_V20_VIEWER_GAZE_SYSTEM

**Engine ID:** V20-ENG-014
**Engine name:** Viewer Gaze Engine (R014)
**Canon status:** BLOCKED — awaiting production testing per VERIFICATION_R014
**Version:** 0.1.0
**Last updated:** 2026-06-05
**Owner:** V20 production track
**Research file:** `research/V20_RESEARCH/R014_VIEWER_GAZE_ENGINE.md`
**Verification file:** `verification/V20_RESEARCH/VERIFICATION_R014_VIEWER_GAZE.md`
**Companion engines:** R012 (Conversation Illusion), R013 (Object Motivation)

---

## 1. Mission

Give every generated image in the V20 pipeline a **gaze itinerary**: a deterministic plan for where the viewer's eye lands first, where it goes second, and what makes it return. The engine exists to convert *glanceable* images (technically beautiful, immediately forgotten) into *watchable* images (the viewer's eye returns, dwells, and remembers).

The engine does NOT decide:
- Who the persona is (R015 / Persona Visual Anchor)
- What she is wearing (R016 / Outfit Card)
- Where she is (R017 / Environment Engine)
- What she is doing (R011 / Scene Composition)
- What her expression is *about* (R012 / Conversation Illusion)
- What objects surround her (R013 / Object Motivation)

The engine DOES decide, given the above inputs:
- How the face is framed in the image.
- Where the eye vector points.
- What secondary anchors exist.
- How the face is lit to maximize the gaze anchor.
- What micro-expression state the face is in.

---

## 2. Inputs

| Input | Type | Source | Required? |
|---|---|---|---|
| `persona_id` | string | R015 | required |
| `persona_face_signature` | object (face anchor, micro-distinctive features, default expression) | R015 | required |
| `scene_id` | string | R011 | required |
| `scene_emotional_target` | enum { tease, intimate, playful, contemplative, confident, candid } | R011 | required |
| `expression_intent` | enum { half_smile, duchenne_smile, suppressed_smile, decay_smile, neutral_plus, caught_looking, pre_speech, knowing, post_laugh, listening, neutral_engaged } | R012 | required |
| `gaze_mode` | enum { mitsumeru, miseru, nagasu, half_lidded_flirty, recovered_from_away } | R012 | required |
| `lighting_brief` | object (key_direction, intensity, shadow_fill) | R017 | required |
| `composition_crop` | enum { headshot, head_shoulders, chest_up, mid_body, full_body } | this engine | required |
| `attention_anchors_request` | object { foreground, midground, background } | R013 | required |
| `platform_target` | enum { instagram, xiaohongshu, twitter, douyin, generic } | R018 | required |
| `unintentional_action` | string (mid-step, mid-gesture, mid-laugh, etc.) | R011 | optional, default = static |

---

## 3. Output contract — the gaze itinerary

The engine emits a JSON object describing the gaze path, the face state, and the attention anchors. The downstream generator consumes this to produce the actual image.

```json
{
  "primary_anchor": "eyes | mouth | hand | prop | environment",
  "secondary_anchor": "...",
  "gaze_vector": {
    "direction": "direct | offset_15 | offset_30 | offset_45+",
    "return_from_away": true | false,
    "hold_intensity": 0.0..1.0
  },
  "eye_state": {
    "mode": "mitsumeru | miseru | nagasu | closed | blink",
    "lid_ratio": 0.0..1.0,
    "brow_state": "neutral | raised | furrowed | asymmetric",
    "periorbital_engagement": 0.0..1.0,
    "catchlight_position": "upper_30 | upper_15 | side | absent"
  },
  "mouth_state": {
    "type": "duchenne | suppressed | decay | neutral_plus | smirk | closed | parted | open",
    "asymmetry": 0.0..1.0
  },
  "micro_expression": "you_caught_me | shared_joke | teasing | thinking | listening | resting",
  "face_first_hierarchy": {
    "face_in_upper_third": true | false,
    "face_is_largest": true | false,
    "face_is_sharpest": true | false,
    "face_is_brightest": true | false,
    "face_no_occlusion": true | false
  },
  "attention_anchors": {
    "foreground": "...",
    "midground": "...",
    "background": "..."
  },
  "personal_details": ["..."],
  "second_person_trace": "...",
  "incomplete_pattern": "...",
  "returning_detail_echo": "...",
  "retention_estimate": {
    "three_second_hold": 0.0..1.0,
    "return_fixation_probability": 0.0..1.0
  }
}
```

The `retention_estimate` is the engine's own prediction of how the viewer's eye will behave. A `three_second_hold < 0.5` is flagged for review.

---

## 4. State

The engine maintains a per-character, per-session state:

- `default_gaze_mode`: the character's default gaze mode (usually mitsumeru).
- `default_mouth_state`: the character's default mouth state (usually neutral_plus or suppressed).
- `recent_personal_details`: list of personal details used in recent frames (to prevent repetition).
- `recent_second_person_traces`: list of traces used.
- `recent_returning_details`: list of echoes used.

The state persists across frames within a session.

---

## 5. Core rules (from research file §13)

The engine enforces the 12 R014 rules. Each rule is a *hard* constraint.

| Rule ID | Rule | Pass criteria |
|---|---|---|
| R014-01 | Mitsumeru-me default | Lid 50–65%, brow neutral, eye engagement 0.6+, catchlight upper-30° |
| R014-02 | Three-plane anchoring | Anchor at foreground, midground, and background depth |
| R014-03 | Face-first hierarchy | Face in upper third, largest, sharpest, brightest, no occlusion |
| R014-04 | Suppressed/decay smile default | Mouth in suppression, decay, or neutral-plus state |
| R014-05 | Return-from-away residue | Gaze vector carries "just returned" signature |
| R014-06 | Personal detail density 2–3 | Exactly 2–3 specific personal details |
| R014-07 | Second-person trace mandatory | ≥ 1 environmental element implying another person |
| R014-08 | One incomplete pattern | Exactly 1 visual/narrative element implied but not fully shown |
| R014-09 | One returning detail | Exactly 1 detail discoverable on second look |
| R014-10 | No face-occluding props | Nothing crosses the face plane |
| R014-11 | No symmetric eye state | Lid, catchlight, brow, gaze all show small asymmetries |
| R014-12 | Catchlight consistency | Catchlight position consistent with implied light source |

---

## 6. Forbidden patterns (from research file §14)

| FP ID | Pattern |
|---|---|
| FP-01 | Single-fixation frame (no peripheral anchors) |
| FP-02 | Single-plane composition (everything at the same depth) |
| FP-03 | Face competing with body (body as detailed as face) |
| FP-04 | Face in shadow (face darker than surroundings) |
| FP-05 | Closed-lip performed smile (model smile, no orbicularis) |
| FP-06 | Big toothy smile, no eye change (max amplitude performed) |
| FP-07 | Static direct gaze, no away-look residue (performed stare) |
| FP-08 | Pure smirk (both corners up, closed lip, smug) |
| FP-09 | Fully-revealed tease (nothing withheld) |
| FP-10 | No second-person trace (single-subject frame) |
| FP-11 | No personal details (no specific brand, name, place) |
| FP-12 | No incomplete pattern (frame fully resolved) |
| FP-13 | No returning detail (all visible on first look) |
| FP-14 | Bilateral eye symmetry (AI tell) |
| FP-15 | Catchlight contradiction (catchlight vs implied light) |
| FP-16 | Face occluded (hand, hair, prop crosses face) |
| FP-17 | Mid-blink frame (eye in transit) |

---

## 7. Interaction with sibling engines

### R012 (Conversation Illusion) — the engine reads from and writes to R012

R014 reads R012's `gaze_mode` and `expression_intent`. These determine the eye state and mouth state defaults.

R014 writes the `eye_state` and `mouth_state` to R012 so R012 can factor the gaze into the conversation-illusion scoring.

### R013 (Object Motivation) — the engine reads from and writes to R013

R014 reads R013's `attention_anchors_request` to know which objects should be at which depth plane.

R014 writes the `attention_anchors` to R013 so R013 can verify that the anchors it provided are actually used at the requested depth.

### R015 (Persona Visual Anchor) — the engine reads from R015

R014 reads the persona's `face_signature` (face anchor, micro-distinctive features, default expression) to seed the eye state and mouth state.

### R017 (Environment Engine) — the engine reads from R017

R014 reads the lighting brief and the environment's spatial layout to determine the catchlight position and the face-occlusion check.

### R011 (Scene Composition) — the engine reads from R011

R014 reads the scene's `emotional_target` and `unintentional_action` to determine the micro-expression and the gaze state.

---

## 8. Retention-estimation algorithm

The engine's `retention_estimate` is computed as follows:

```
three_second_hold = 0.25 * first_second_pause
                  + 0.20 * first_second_detail_capture
                  + 0.20 * second_second_detail_discovery
                  + 0.20 * return_fixation_trigger
                  + 0.15 * (1 - any_FP_match)

return_fixation_probability = 0.30 * returning_detail_presence
                            + 0.25 * incomplete_pattern_strength
                            + 0.20 * second_person_trace_strength
                            + 0.15 * personal_detail_density
                            + 0.10 * (1 - any_FP_match)
```

Each sub-score is 0–1:
- `first_second_pause`: 1.0 if the eye has a strong first-fixation bait (catchlight, mitsumeru-me engagement), 0.0 if not.
- `first_second_detail_capture`: 1.0 if there is a salient first-second detail (a coloured iris, a half-lidded beat, a suppressed smile), 0.0 if not.
- `second_second_detail_discovery`: 1.0 if there is a peripheral element to find (a hand, a prop), 0.0 if not.
- `return_fixation_trigger`: 1.0 if there is a returning detail or a return-from-away residue, 0.0 if not.
- `returning_detail_presence`, `incomplete_pattern_strength`, `second_person_trace_strength`, `personal_detail_density`: 1.0 if present and strong, scaled down by weakness.
- `any_FP_match`: 1.0 if no FP matches, 0.0 if any matches.

A `three_second_hold < 0.5` is flagged for review. A `return_fixation_probability < 0.4` is flagged for review.

---

## 9. Personal-detail and trace libraries

### Personal-detail library (per character)

The engine reads from a per-character library of specific personal details. The library is populated by R015 and curated by the production team. Examples:

- Watches: vintage Seiko, Casio F-91W, Apple Watch, no watch.
- Notebooks: Moleskine, Leuchtturm1917, Muji, no notebook.
- Pens: Lamy Safari, Muji gel pen, Montblanc, no pen.
- Jewelry: specific rings, necklaces, earrings.
- Phone cases: clear, leather, printed, specific brand.
- Coffee cups: specific mug the character uses daily.

### Second-person trace library

- Two coffee cups (paired).
- Empty chair (recently sat in).
- Half-written note (in the viewer's direction).
- Phone showing a chat (open to a recent message).
- Across-table seat (set for two).
- Half-drawn curtain (someone was just looking out).
- Second pillow (someone else sleeps here).
- A second toothbrush (shared bathroom).

### Imperfection library (per character)

- Flyaway hair (the default, neutral).
- Smudged lipstick.
- Half-buttoned shirt.
- Tag still on.
- Chipped nail polish.
- Sock slightly down.
- Pillow crease.

The engine ensures the same imperfection is not used in two consecutive frames for the same character.

---

## 10. Version and changelog

**v0.1.0** (2026-06-05) — Initial engine module. Canon status: BLOCKED.

**Planned for v0.2.0 (post-production-test):**
- Per-platform tuning of the personal-detail density (Xiaohongshu: 3; Instagram: 2; Twitter: 1–2).
- Per-character tuning of the default gaze mode (some characters lean more mitsumeru, some more half-lidded-flirty).
- Per-time-of-day tuning of the imperfection (late night: pillow crease; morning: flyaway hair).
- A learning loop that updates the retention_estimate based on production A/B test data.

---

**End R014 engine spec.** Companion: R014_VIEWER_GAZE_ENGINE.md (research), VERIFICATION_R014_VIEWER_GAZE.md (verification).
