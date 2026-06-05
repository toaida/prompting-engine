# ENGINE_V20_DAILY_DIALOGUE_SYSTEM (v2 — lil.troublr)

**Engine ID:** V20-ENG-012
**Engine name:** Daily Dialogue Engine (R012)
**Canon status:** BLOCKED — awaiting production testing per VERIFICATION_R012
**Version:** 0.2.0
**Last updated:** 2026-06-05
**Owner:** V20 production track (lil.troublr)
**Research file:** `research/V20_RESEARCH/R012_DAILY_DAILOGUE_ENGINE.md`
**Verification file:** `verification/V20_RESEARCH/VERIFICATION_R012_DAILY_DAILOGUE.md`
**Companion engines:** R013 (Object Motivation), R014 (Viewer Gaze), R015 (Luxury Intimate Fashion), R016 (Swimwear Design Language), R017 (Female Teasing Behaviour)

---

## 1. Mission

Give every generated image in the lil.troublr pipeline a **conversation illusion** that makes the viewer feel: she noticed them, she is reacting to something, she is sharing a private joke, the photo is part of a conversation. The engine exists to convert *attractive-but-inert* portraits into *attractive-and-interactive* portraits. The reference frames are P033A (settled), P036B (interrupted), and P036C (playful embarrassment).

The engine does NOT decide:
- Who the persona is (R015 / Persona Visual Anchor)
- What she is wearing (R016 / Outfit Card, R015 / Intimate Fashion for intimate frames)
- Where she is (R017 / Environment Engine)
- What her gaze anchors are (R014 / Viewer Gaze)
- What objects surround her (R013 / Object Motivation)
- What her teasing beat is (R017 / Female Teasing Behaviour, *cross-engine*)

The engine DOES decide, given the above inputs:
- The conversation beat (which of the 11 R012 beats is active).
- The expression state (mouth, eyes, brows, micro-expression).
- The body state (posture, in-progress action, frame offset seconds).
- The "dialogue state" (pre-state, peak, decay — which phase of the beat the frame captures).

---

## 2. Inputs

| Input | Type | Source | Required? |
|---|---|---|---|
| `persona_id` | string | R015 | required |
| `persona_expression_signature` | object (default lid ratio, default mouth state, default brow state) | R015 | required |
| `scene_id` | string | R011 | required |
| `scene_conversation_beat` | enum { pre_speech, mid_speech, post_speech, pre_laugh, suppressed_laugh, post_laugh, caught_you_looking, shared_joke, teasing, playful_embarrassment, resting_with_viewer } | R011 or R017 | required |
| `gaze_mode` | enum { mitsumeru, miseru, nagasu, half_lidded_flirty, recovered_from_away } | R014 | required |
| `micro_expression` | enum { suppressed_smile, decay_smile, neutral_plus, naughty_cute, suppressed_laugh, post_punchline, you_caught_me, shared_joke, teasing, playful_embarrassment, trying_not_to_laugh, fake_innocence, listening, post_tease } | this engine | required |
| `imperfection` | enum { flyaway_hair, smudged_lipstick, half_buttoned, tag_still_on, chipped_nail, sock_slightly_down, pillow_crease, none } | this engine | required (default = flyaway_hair) |
| `unintentional_action` | string (mid-sip, mid-turn, mid-look-away, mid-cardigan-on, etc.) | R011 or R017 | optional, default = none |
| `second_person_trace` | string (two_coffee_cups, empty_chair, half_written_note, phone_with_message) | R013 | required |
| `in_progress_residue` | list of strings (half_eaten_meal, open_book_face_down, pulled_out_chair, etc.) | R013 | required, ≥ 2 items |
| `platform_target` | enum { instagram, xiaohongshu, twitter, douyin, generic } | R018 | required |
| `frame_offset_seconds` | float (-1.0 to +1.5) | this engine | required |
| `teasing_beat_ref` | EL-XX (Expression Library) | R017 | optional, required if `scene_conversation_beat` is in the teasing family |
| `behaviour_ref` | BL-XX (Behaviour Library) | R017 | optional |
| `interaction_ref` | IL-XX (Interaction Library) | R017 | optional |

---

## 3. Output contract

The engine emits a JSON object describing the conversation-illusion state of the frame. The downstream generator consumes this to produce the actual image.

```json
{
  "conversation_beat": "pre_speech | mid_speech | post_speech | pre_laugh | suppressed_laugh | post_laugh | caught_you_looking | shared_joke | teasing | playful_embarrassment | resting_with_viewer",
  "frame_offset_seconds": 0.6,
  "expression_state": {
    "eye_mode": "mitsumeru | miseru | nagasu | half_lidded_flirty | recovered_from_away",
    "lid_ratio": 0.55,
    "brow_state": "neutral | raised_asymmetric | furrowed_asymmetric | neutral_plus",
    "periorbital_engagement": 0.7,
    "mouth_type": "suppressed | decay | neutral_plus | parted | closed | smirk_asymmetric | open_5_15mm | trying_not_to_laugh",
    "mouth_asymmetry_mm": 4,
    "containment_element": "hand_on_lip | turned_head | bitten_lip | pressed_lips | shoulder_raised | none",
    "micro_expression": "suppressed_smile | decay_smile | neutral_plus | naughty_cute | suppressed_laugh | post_punchline | you_caught_me | shared_joke | teasing | playful_embarrassment | trying_not_to_laugh | fake_innocence | listening | post_tease"
  },
  "body_state": {
    "head_tilt_degrees": 8,
    "head_turn_degrees": 15,
    "shoulder_asymmetry": "left_high | right_high | neutral",
    "hip_weight": "left | right | centered",
    "spine": "S_curve | vertical | relaxed",
    "in_progress_action": "mid_sip | mid_turn | mid_look_away_then_back | mid_cardigan_on | mid_reach | mid_emerging | mid_towel_adjust | mid_brush | mid_button | none"
  },
  "hand_state": {
    "occupation": "coffee_cup | phone | pen | own_hair | own_sleeve | partner_hand | counter_top | none",
    "self_touch": "hand_on_cheek | hand_on_ear | hand_in_hair | hand_on_collar | hand_on_lip | none",
    "prop_touch": "hand_on_cup | hand_on_phone | hand_on_pen | hand_on_book | none",
    "avoid_modelling_positions": true,
    "specific_grip": "around_cup_body | around_phone | between_thumb_index | relaxed_fist"
  },
  "imperfection": {
    "type": "flyaway_hair | smudged_lipstick | half_buttoned | tag_still_on | chipped_nail | sock_slightly_down | pillow_crease | none",
    "location": "crossing_cheek | on_lower_lip | bottom_button | on_jacket_tag | on_ring_finger | on_left_ankle | under_subject_head | none"
  },
  "second_person_trace": "two_coffee_cups | empty_chair | half_written_note | phone_with_message | across_table_seat | half_drawn_curtain | second_pillow | none",
  "in_progress_residue": ["half_eaten_meal", "open_book_face_down"],
  "framing_consistency": {
    "framing_type": "phone_camera | dslr | medium_format | film_35mm",
    "lighting_type": "env_lit | studio | mixed | window | lamp | screen",
    "catchlight_source_consistent": true
  },
  "crop_joint": "chin | wrist | elbow | knee | mid_thigh",
  "library_refs": {
    "expression_ref": "EL-XX",
    "behaviour_ref": "BL-XX",
    "interaction_ref": "IL-XX"
  },
  "viewer_feels_personally_noticed_checklist": {
    "eye_contact_with_motion": true,
    "body_in_motion": true,
    "suppression_of_expression": true,
    "second_body_trace": true,
    "self_touch_or_prop_touch": true
  },
  "conversation_illusion_score": {
    "eye_contact_quality": 0.0..1.0,
    "suppression_quality": 0.0..1.0,
    "in_progress_believability": 0.0..1.0,
    "second_person_presence": 0.0..1.0,
    "imperfection_naturalness": 0.0..1.0,
    "personality_visibility": 0.0..1.0,
    "any_FP_match": 0.0..1.0,
    "overall": 0.0..1.0
  }
}
```

The `conversation_illusion_score.overall` is the engine's own estimate of how well the frame delivers the conversation illusion. A score < 0.6 should not be passed to the generator without a manual review.

---

## 4. State

The engine maintains a per-character state that persists across frames in a session:

- `current_beat_progression`: the sequence of conversation beats for the current arc (e.g., `["resting_with_viewer", "pre_speech", "mid_speech", "shared_joke", "suppressed_laugh", "post_laugh", "teasing", "playful_embarrassment", "resting_with_viewer"]`).
- `beat_index`: the current position in the progression.
- `frame_offset_accumulator`: how many seconds the character has been in the current beat.
- `imperfection_used_in_session`: list of imperfections already used (to prevent repetition).
- `second_person_trace_used_in_session`: list of traces already used.
- `el_bl_il_refs_used_in_session`: list of library refs already used.

The state is reset when a new arc starts.

---

## 5. Core rules (from research file §14)

The engine enforces the 15 R012 rules. Each rule is a *hard* constraint.

| Rule ID | Rule | Pass criteria |
|---|---|---|
| R012-01 | Mitsumeru-me as default gaze | Lid 50–65%, brow neutral, eye engagement 0.6+, catchlight upper-30° |
| R012-02 | Return-from-away residue | Gaze vector carries "just returned" signature |
| R012-03 | Suppressed or decay smile default | Mouth in suppression, decay, or neutral-plus state |
| R012-04 | Asymmetric posture, always | Shoulder or hip or head tilt asymmetry ≥ 5° |
| R012-05 | Hands occupied, not posed | At least one hand on a real object, not in modelling position |
| R012-06 | In-progress body state | Action has a defined end-state and is at a between-beat offset |
| R012-07 | Second-person trace mandatory | At least one trace from the allowed list |
| R012-08 | Environment in same temporal frame | ≥ 2 in-progress residue items consistent with the timestamp |
| R012-09 | One and only one imperfection | Exactly one imperfection, in a natural state, not feature position |
| R012-10 | No bilateral expression symmetry | Mouth, eyes, brows all show small asymmetries |
| R012-11 | Phone-camera or clean DSLR, never mixed | Framing and lighting type consistent, catchlight consistent |
| R012-12 | Crop at an emotional joint | Crop is at chin, wrist, elbow, knee, or mid-thigh |
| R012-13 | Frame offset between -1.0s and +1.5s | Frame is *between* beats, not at a beat |
| R012-14 | One personal detail in the periphery | At least one specific personal detail visible |
| R012-15 | One incomplete pattern | At least one element of the frame is implied but not fully shown |

---

## 6. Forbidden patterns (from research file §14)

| FP ID | Pattern |
|---|---|
| FP-01 | Model stare (centred iris, no orbicularis) |
| FP-02 | Symmetric 3/4 (head turned, eyes on-axis) |
| FP-03 | Catchlight contradiction (catchlight vs face shadow direction) |
| FP-04 | Pure performance (bilateral symmetry in pose, gaze, expression) |
| FP-05 | Cliché tease (wink, bite-lip, peace sign, peace + wink, tongue, finger-gun) |
| FP-06 | Smug × smug (closed-lip smirk + closed-lip smirk) |
| FP-07 | Dead candid (phone-camera framing with studio catchlights) |
| FP-08 | Empty environment (no second-person trace, no residue) |
| FP-09 | Tableau freeze (no in-progress action, no implied beat offset) |
| FP-10 | Full laugh (mouth fully open, teeth bared, no suppression) |
| FP-11 | Nagasu-me (gaze fully averted, focus in the distance) |
| FP-12 | Theatrical blush (uniform red across the cheeks) |
| FP-13 | Hair flip (signals "performance", not embarrassment) |

---

## 7. Beat-to-rule mapping (v2 — 11 beats)

| Beat | Default rules active | Default mouth | Default gaze | Default offset |
|---|---|---|---|---|
| Pre-speech | R012-01, -02, -04, -07, -11, -12, -13 | Mid-speech (vowel shape) | Mitsumeru-me | -0.4s |
| Mid-speech | R012-01, -02, -03, -04, -07, -11, -12, -13 | Vowel shape | Mitsumeru-me | 0.0s |
| Post-speech | R012-01, -02, -03, -04, -07, -11, -12, -13 | Decay | Mitsumeru-me | +0.6s |
| Pre-laugh | R012-01, -02, -04, -07, -11, -12, -13 | Eyes narrowing, mouth starting to open | Mitsumeru-me | -0.3s |
| Suppressed laugh | R012-01, -02, -03, -04, -07, -09, -11, -12, -13 | Suppressed 5–10mm open, containment element required | Mitsumeru-me | 0.0s |
| Post-laugh | R012-01, -02, -03, -04, -07, -09, -11, -12, -13 | Decay smile, eyes crinkled | Mitsumeru-me | +0.8s |
| Caught-you-looking | R012-02, -04, -06, -07, -08, -11, -12, -13 | Settling (in transit) | Mitsumeru-me return, head slightly off-axis | 0.0s |
| Shared joke | R012-01, -02, -03, -04, -07, -08, -10, -11, -12, -13 | Decay, containment element | Mitsumeru-me, one brow slightly raised | +0.6s |
| Teasing | R012-01, -02, -03, -04, -07, -11, -12, -13 | "I just said something" state, one brow raised | Mitsumeru-me with a micro-glance off-axis and back | +0.3s |
| Playful embarrassment | R012-01, -02, -04, -07, -08, -09, -10, -11, -12, -13 | Suppressed with asymmetry, containment element, cheek blush subtle | Direct → indirect → direct (recovery) | 0.0s |
| Resting with viewer | R012-01, -02, -03, -04, -07, -11, -12, -13 | Neutral-plus | Mitsumeru-me, settled | 0.0s |

---

## 8. The three reference templates (P033A, P036B, P036C)

The engine ships with three pre-built templates for the three reference frames. Production can override per-character or per-campaign.

### P033A — Settled

- **Beat:** `shared_joke` or `post_speech`
- **Gaze:** `mitsumeru_me` + return-from-away residue
- **Mouth:** `decay_smile` (post-punchline warmth)
- **Body:** asymmetric posture, one shoulder higher, head tilt 8–15°
- **Hands:** occupied (cup, pen, phone)
- **Imperfection:** flyaway hair (default)
- **Second-person trace:** `two_coffee_cups` or `empty_chair` or `half_written_note`
- **Frame:** phone-camera, env-lit, crop at chin
- **Frame offset:** +0.6s (decay)
- **EL ref:** EL-01 (mitsumeru-me) + EL-07 (decay_smile)
- **BL ref:** BL-01 (mid_sip) or BL-19 (mid_book_turn)
- **IL ref:** IL-09 (post_conversation) or IL-06 (second_person_trace)

### P036B — Interrupted

- **Beat:** `caught_you_looking`
- **Gaze:** `recovered_from_away` (mitsumeru-me + head slightly off)
- **Mouth:** `settling` (in transit) or `suppressed` (sm)
- **Body:** mid-turn, body in motion
- **Hands:** mid-gesture (the hand that was doing the private action)
- **Imperfection:** flyaway hair
- **Second-person trace:** `phone_with_message` or `half_written_note`
- **Frame:** phone-camera, env-lit, crop at chin
- **Frame offset:** 0.0s (the recovery moment)
- **EL ref:** EL-25 (caught_you_looking) or EL-34 (caught_in_progress)
- **BL ref:** BL-02 (mid_turn) or BL-33 (mid_turn_to_see_who_called)
- **IL ref:** IL-01 (caught_you_looking) or IL-02 (interrupted)

### P036C — Playful embarrassment

- **Beat:** `playful_embarrassment`
- **Gaze:** three-beat sequence (direct → indirect → direct, recovery)
- **Mouth:** suppressed with asymmetry, containment element required
- **Cheek blush:** subtle, character-dependent
- **Hands:** hand near face (self-touch: cheek, ear, hair, collar)
- **Imperfection:** one of (flyaway hair, smudged lipstick, half-buttoned)
- **Second-person trace:** optional
- **Returning detail:** one specific personal detail in the periphery
- **Frame:** phone-camera or DSLR
- **Frame offset:** 0.0s (the recovery moment)
- **EL ref:** EL-15 (playful_embarrassment) or EL-29 (playful_embarrassment_asymmetric)
- **BL ref:** BL-28 (mid_hand_over_mouth) or BL-29 (mid_bit_lip) or BL-XX (other self-touch)
- **IL ref:** IL-07 (reacting_to_viewer) or IL-14 (reacting_to_compliment)

---

## 9. Conversation-illusion scoring (v2 — extended)

```
overall = 0.18 * eye_contact_quality
        + 0.16 * suppression_quality
        + 0.14 * in_progress_believability
        + 0.16 * second_person_presence
        + 0.08 * imperfection_naturalness
        + 0.14 * personality_visibility
        + 0.14 * (1 - any_FP_match)
```

Each sub-score is 0–1:
- `eye_contact_quality`: 1.0 if R012-01 and R012-02 pass, scaled by periorbital engagement.
- `suppression_quality`: 1.0 if the mouth is in a suppression state, scaled by mouth asymmetry.
- `in_progress_believability`: 1.0 if the in-progress action has a defined end-state and the offset is in range.
- `second_person_presence`: 1.0 if the trace is present and in a natural position, 0.5 if present but in a feature position, 0.0 if absent.
- `imperfection_naturalness`: 1.0 if the imperfection is in a natural state, 0.5 if in a feature position, 0.0 if absent or over-counted.
- `personality_visibility`: 1.0 if the expression is *specific* to the character, 0.5 if generic, 0.0 if stock.
- `any_FP_match`: 1.0 if any forbidden pattern matches, 0.0 if none.

A frame with `overall < 0.6` is rejected by the engine. A frame with `0.6 ≤ overall < 0.8` is passed to the generator but flagged for review. A frame with `overall ≥ 0.8` is passed without flag.

---

## 10. Library reference resolution (cross-engine with R017)

When the engine receives a `teasing_beat_ref` (EL-XX), `behaviour_ref` (BL-XX), or `interaction_ref` (IL-XX) from R017, the engine resolves the ref and incorporates the entry's `muscle_pattern`, `action`, and `type` into the output contract.

### Resolution rules

- EL-XX must be a real entry in R017's Expression Library (EL-01 to EL-35). Unknown refs are rejected.
- BL-XX must be a real entry in R017's Behaviour Library (BL-01 to BL-40). Unknown refs are rejected.
- IL-XX must be a real entry in R017's Interaction Library (IL-01 to IL-25). Unknown refs are rejected.
- The `pairs_with` and `avoid_with` rules of the resolved entry must be respected.
- A library-mismatch (e.g., EL-15 in a "resting" beat) is flagged before scoring.

---

## 11. Interaction with sibling engines

### R012 ↔ R013 (Object Motivation)

R012 reads R013's `second_person_trace` and `in_progress_residue`. R013 reads R012's `conversation_beat` to drive object selection.

### R012 ↔ R014 (Viewer Gaze)

R012 reads R014's `gaze_mode` and `eye_state`. R012 writes `expression_state` to R014.

### R012 ↔ R015 (Luxury Intimate Fashion)

R012 reads R015's `garment_state` and `garment.beat_fit`. For intimate frames, R012 ensures the expression matches the garment beat (e.g., a `decay_smile` is appropriate for a "post-choice" beat in R015).

### R012 ↔ R016 (Swimwear Design Language)

R012 reads R016's `garment.design_signal`. For swimwear frames, R012 ensures the expression matches the design signal (e.g., a `playful_embarrassment` is appropriate for a "cutout" design signal in R016).

### R012 ↔ R017 (Female Teasing Behaviour)

R012 reads R017's `teasing_beat_ref` (EL-XX), `behaviour_ref` (BL-XX), `interaction_ref` (IL-XX). R012 writes the resolved `expression_state` back to R017.

### R012 ↔ R011 (Scene Composition)

R012 reads the scene's `conversation_beat` and the `unintentional_action` (if any).

### R012 ↔ R015 (Persona Visual Anchor)

R012 reads the persona's `expression_signature` (default lid ratio, default mouth state, default brow state) to seed the output contract.

---

## 12. Version and changelog

**v0.1.0** (2026-06-05, AContent V20 framing) — Initial engine module. Canon status: BLOCKED.

**v0.2.0** (2026-06-05, lil.troublr framing) — Rebrand to lil.troublr. 15 rules (was 12). Added 11th beat (`playful_embarrassment`). Added `playful_embarrassment`, `fake_innocence`, `resting_with_viewer` beats. Added `containment_element` to output contract. Added `library_refs` (EL/BL/IL) cross-engine resolution with R017. Added `personality_visibility` sub-score. Updated `viewer_feels_personally_noticed_checklist`. Canon status: BLOCKED.

**Planned for v0.3.0 (post-production-test):**
- Per-platform tuning of the conversation beat selection (Xiaohongshu prefers `suppressed_laugh` and `teasing`; Instagram prefers `shared_joke` and `caught_you_looking`).
- Per-character tuning of the default `micro_expression`.
- Per-time-of-day tuning of the `imperfection` selection.

---

**End R012 v2 engine spec.** Companion: `R012_DAILY_DIALOGUE_ENGINE.md` (research), `VERIFICATION_R012_DAILY_DIALOGUE.md` (verification).
