# ENGINE_V20_FEMALE_TEASING_BEHAVIOUR

**Engine ID:** V20-ENG-017
**Engine name:** Female Teasing Behaviour Engine (R017)
**Canon status:** BLOCKED — awaiting production testing per VERIFICATION_R017
**Version:** 0.1.0
**Last updated:** 2026-06-05
**Owner:** V20 production track (lil.troublr)
**Research file:** `research/V20_RESEARCH/R017_FEMALE_TEASING_BEHAVIOUR_ENGINE.md`
**Verification file:** `verification/V20_RESEARCH/VERIFICATION_R017_FEMALE_TEASING.md`
**Release manifest:** `gpt-release/manifests/FEMALE_TEASING_MANIFEST.md`
**Companion engines:** R012 (Conversation Illusion), R013 (Object Motivation), R014 (Viewer Gaze), R015 (Luxury Intimate Fashion), R016 (Swimwear Design Language)

---

## 1. Mission

Give every generated frame in the lil.troublr pipeline a **teasing beat** that makes the viewer feel personally noticed. The engine exists to convert *posed* frames (subject delivering a state to the camera) into *teasing* frames (subject responding to the viewer's presence, sharing a private joke, caught in a private moment).

The engine's core output is the three libraries: **Expression Library (EL)**, **Behaviour Library (BL)**, and **Interaction Library (IL)**. These libraries are the canonical reference for all lil.troublr prompts.

The engine does NOT decide:
- Who the persona is (Persona Visual Anchor)
- What she is wearing (R015, R016)
- Where she is (R017 / Environment Engine — different module within same engine ID, see note)
- What her gaze anchors are (R014 / Viewer Gaze)

*Note: the engine ID V20-ENG-017 is shared between this engine (R017 Female Teasing Behaviour) and the Environment Engine. In production, these are separate modules within the same engine ID. The Environment Engine is responsible for `location_type` and `setting`; this engine is responsible for the teasing beat.*

The engine DOES decide, given the above inputs:
- The teasing beat (which of the 11 R017 beats is active).
- The expression reference (EL-XX).
- The behaviour reference (BL-XX).
- The interaction reference (IL-XX).
- The viewer-feels-personally-noticed checklist pass/fail.

---

## 2. Inputs

| Input | Type | Source | Required? |
|---|---|---|---|
| `persona_id` | string | Persona Visual Anchor | required |
| `persona_teasing_signature` | object (default beat, default expression, default behaviour) | Persona Visual Anchor | required |
| `scene_id` | string | R011 | required |
| `scene_conversation_beat` | enum { ... } | R011 or R012 | required |
| `location_type` | enum { kitchen, study, beach, pool, hotel, fitting_room, mirror, birthday, daily_life, friend_group, ... } | Environment Engine | required |
| `teasing_beat` | enum { settled, interrupted, playful_embarrassment, shared_joke, teasing, trying_not_to_laugh, caught_you_looking, fake_innocence, friend_group, resting_with_viewer } | this engine | required |
| `expression_ref` | EL-XX (Expression Library) | this engine | required |
| `behaviour_ref` | BL-XX (Behaviour Library) | this engine | optional |
| `interaction_ref` | IL-XX (Interaction Library) | this engine | optional |
| `platform_target` | enum { instagram, xiaohongshu, twitter, douyin, generic } | R018 | required |

---

## 3. Output contract

The engine emits a JSON object specifying the beat, the library refs, the expression state, the behaviour state, the interaction state, the viewer-noticed checklist, and the playfulness score.

```json
{
  "beat": "settled | interrupted | playful_embarrassment | shared_joke | teasing | trying_not_to_laugh | caught_you_looking | fake_innocence | friend_group | resting_with_viewer",
  "expression_ref": "EL-XX",
  "behaviour_ref": "BL-XX",
  "interaction_ref": "IL-XX",
  "expression_state": {
    "muscle_pattern": "mitsumeru_me | suppressed_smile | decay_smile | trying_not_to_laugh | playful_embarrassment | ...",
    "lid_ratio": 0.55,
    "brow_state": "neutral | asymmetric_raised | furrowed | neutral_plus",
    "mouth_type": "suppressed | decay | neutral_plus | trying_not_to_laugh | closed | smirk_asymmetric | open_5_10mm",
    "mouth_asymmetry_mm": 4,
    "containment_element": "hand_on_lip | turned_head | bitten_lip | pressed_lips | shoulder_raised | none"
  },
  "behaviour_state": {
    "action": "mid_sip | mid_turn | mid_reach | mid_brush | mid_button | mid_towel_adjust | mid_robe_on | mid_cardigan_on | ...",
    "body_in_motion": true,
    "in_progress_signature": "the body is mid-X with a defined end-state"
  },
  "interaction_state": {
    "type": "caught_you_looking | interrupted | teasing_viewer | shared_joke_with_other | friend_group | second_person_trace | reacting_to_viewer | mid_conversation | post_conversation | sharing_secret | ...",
    "second_body": "hand_on_shoulder | face_next_to | body_behind | none | implied",
    "self_touch": "hand_on_cheek | hand_on_ear | hand_in_hair | hand_on_collar | hand_on_lip | none",
    "prop_touch": "hand_on_cup | hand_on_phone | hand_on_pen | hand_on_book | none"
  },
  "viewer_feels_personally_noticed_checklist": {
    "eye_contact_with_motion": true,
    "body_in_motion": true,
    "suppression_of_expression": true,
    "second_body_trace": true,
    "self_touch_or_prop_touch": true
  },
  "playfulness_score": {
    "expression_specificity": 0.0..1.0,
    "behaviour_specificity": 0.0..1.0,
    "interaction_specificity": 0.0..1.0,
    "viewer_noticed_checklist_pass": 0.0..1.0,
    "personality_visibility": 0.0..1.0,
    "any_FP_match": 0.0..1.0,
    "overall": 0.0..1.0
  }
}
```

The `playfulness_score.overall` is the engine's own estimate. A score < 0.6 should not be passed to the generator without review.

---

## 4. State

The engine maintains a per-character, per-session state:

- `default_beat`: the character's default beat (e.g., a "fashion" character defaults to `settled`; a "beach" character defaults to `interrupted`).
- `default_expression_ref`: the character's default expression ref (e.g., EL-08 for "resting" characters, EL-13 for "teasing" characters).
- `recent_el_refs`: list of expression refs used in recent frames (to prevent repetition).
- `recent_bl_refs`: list of behaviour refs used.
- `recent_il_refs`: list of interaction refs used.

The state persists across frames within a session.

---

## 5. The three libraries (the core output)

The engine's core output is the three libraries defined in research file Appendices A, B, and C. The libraries are summarised here; the canonical definitions are in the research file.

### Expression Library (35 entries, EL-01 to EL-35)

The Expression Library is a curated set of named expressions with muscle patterns, visual signatures, and pairing rules. Highlights:

- **EL-01 mitsumeru-me** — the "eye that watches" (default dialogue gaze).
- **EL-04 half_lidded_flirty** — the flirty, intimate gaze.
- **EL-05 recovered_from_away** — the caught-you-looking residue.
- **EL-06 suppressed_smile** — the "I just said something" beat.
- **EL-07 decay_smile** — the post-punchline warmth.
- **EL-09 trying_not_to_laugh** — the suppressed laugh.
- **EL-15 playful_embarrassment** — the "I just got caught" beat.
- **EL-19 surprised** — the eyes-wide, brows-up beat.
- **EL-20 delight** — the full Duchenne smile.
- **EL-25 caught_you_looking** — the recovery state.
- **EL-29 playful_embarrassment_asymmetric** — the asymmetric blush.

See research file Appendix A for the full 35 entries.

### Behaviour Library (40 entries, BL-01 to BL-40)

The Behaviour Library is a curated set of named behaviours (posture, in-progress actions, gestures). Highlights:

- **BL-01 mid_sip** — cup halfway to mouth, eyes at camera.
- **BL-02 mid_turn** — body in rotation, head may be ahead or behind.
- **BL-05 mid_cardigan_on** — one arm in, one arm out.
- **BL-14 mid_emerging_from_water** — one shoulder out, water on skin.
- **BL-15 mid_towel_adjust** — towel being adjusted in a bathroom.
- **BL-28 mid_hand_over_mouth** — containment element for trying-not-to-laugh.
- **BL-29 mid_bit_lip** — the tease containment.
- **BL-37 mid_blow_candle** — the birthday beat.
- **BL-40 mid_selfie_take** — the mirror teasing beat.

See research file Appendix B for the full 40 entries.

### Interaction Library (25 entries, IL-01 to IL-25)

The Interaction Library is a curated set of named interactions. Highlights:

- **IL-01 caught_you_looking** — the subject's eyes just returned to the camera.
- **IL-02 interrupted** — the subject was mid-action, the viewer has just appeared.
- **IL-03 teasing_viewer** — the subject is engaging with the viewer playfully.
- **IL-04 shared_joke_with_implied_other** — the subject in post-punchline state, with a second body.
- **IL-05 friend_group_dynamic** — the subject in a group, mid-interaction with a friend.
- **IL-06 second_person_trace** — environmental element implies a second person.
- **IL-07 reacting_to_viewer** — the subject is responding to the viewer's presence.
- **IL-11 in_progress_with_other** — the subject mid-action with the implied other.
- **IL-19 mirror_self_interaction** — the subject in a mirror, mid-interaction with her reflection.
- **IL-24 self_touch_tease** — the subject touching herself in a self-teasing way.

See research file Appendix C for the full 25 entries.

---

## 6. Core rules (from research file §14)

The engine enforces the 20 R017 rules. Each rule is a *hard* constraint.

| Rule ID | Rule | Pass criteria |
|---|---|---|
| R017-01 | Playful eye contact | Mitsumeru-me + micro-glance off-axis and back |
| R017-02 | Caught-you-looking is the highest-converting | Eyes just returned, head slightly off, mouth in transit |
| R017-03 | Trying-not-to-laugh requires containment | Mouth 5–10mm open + containment element |
| R017-04 | Shared-joke is the *post-punchline* state | Decay smile, eyes crinkled, one brow raised |
| R017-05 | Fake innocence | Eyes wide, closed mouth, head tilt, palms up |
| R017-06 | Playful embarrassment is the highest-converting complex | Three-beat gaze, cheek blush, suppressed laugh, hand near face |
| R017-07 | Friend-group requires a second body | Second body in frame or strongly implied |
| R017-08 | Beach teasing vocabulary | Beach-specific props present |
| R017-09 | Pool teasing vocabulary | Pool-specific props present, wet elements |
| R017-10 | Hotel teasing vocabulary | Hotel-specific props present |
| R017-11 | Mirror teasing vocabulary | Mirror-specific props present |
| R017-12 | Birthday teasing vocabulary | Birthday-specific props present |
| R017-13 | Daily-life teasing vocabulary | Daily-life props present |
| R017-14 | Japanese gravure interaction | Gravure-specific elements present |
| R017-15 | Korean lifestyle editorial | Korean-specific elements present |
| R017-16 | Personality visibility (meta) | Real expression, posture, environment, timing, interaction |
| R017-17 | P033A succeeded (settled) | Real environment, mitsumeru-me, suppressed smile, second-person trace, phone-camera |
| R017-18 | P036B succeeded (interrupted) | Caught-you-looking, phone-camera, second-person trace, imperfection |
| R017-19 | Containment + reveal | Containment element + reveal element in the same frame |
| R017-20 | Eyes on + body in motion | Mitsumeru-me + mid-action body state |

---

## 7. Forbidden patterns (R017-specific, 13 patterns)

| FP ID | Pattern |
|---|---|
| FP-17-01 | Static direct gaze with no micro-glance |
| FP-17-02 | Caught-you-looking without recovery (still averted) |
| FP-17-03 | Trying-not-to-laugh without containment |
| FP-17-04 | Shared-joke at peak (full Duchenne) |
| FP-17-05 | Fake innocence with open mouth |
| FP-17-06 | Theatrical blush (uniform red) |
| FP-17-07 | Friend-group with no second body |
| FP-17-08 | Setting-specific beat with no setting-specific props |
| FP-17-09 | Wink (cliché) |
| FP-17-10 | Bite-lip with eye contact (aggressive tease) |
| FP-17-11 | Hair flip (signals performance) |
| FP-17-12 | Library ref doesn't resolve |
| FP-17-13 | Library ref contradicts the beat |

---

## 8. Beat-to-library-ref mapping (default)

| Beat | Default EL ref | Default BL ref | Default IL ref |
|---|---|---|---|
| Settled (P033A) | EL-01 + EL-07 (or EL-06) | BL-01 (mid_sip) or BL-19 (mid_book_turn) | IL-09 (post_conversation) or IL-06 (second_person_trace) |
| Interrupted (P036B) | EL-25 (caught_you_looking) or EL-34 (caught_in_progress) | BL-02 (mid_turn) or BL-33 (mid_turn_to_see_who_called) | IL-01 (caught_you_looking) or IL-02 (interrupted) |
| Playful embarrassment (P036C) | EL-15 (playful_embarrassment) or EL-29 (asymmetric) | BL-28 (mid_hand_over_mouth) or BL-29 (mid_bit_lip) | IL-07 (reacting_to_viewer) or IL-14 (reacting_to_compliment) |
| Shared joke | EL-12 (shared_joke) + EL-07 (decay_smile) | BL-19 (mid_book_turn) or BL-XX | IL-04 (shared_joke_with_implied_other) |
| Trying-not-to-laugh | EL-09 (trying_not_to_laugh) | BL-28 (mid_hand_over_mouth) | IL-16 (trying_not_to_laugh_with_other) or IL-04 |
| Teasing | EL-13 (teasing) or EL-27 (mid_tease) | BL-XX (self-touch or prop-touch) | IL-03 (teasing_viewer) or IL-17 (mid_tease_to_other) |
| Caught-you-looking (recovery) | EL-25 (caught_you_looking) | BL-02 (mid_turn) or BL-33 | IL-01 (caught_you_looking) or IL-22 (reacting_to_sound) |
| Fake innocence | EL-14 (fake_innocence) | BL-XX (palms up) | IL-12 (reacting_to_tease) |
| Friend group | EL-12 (shared_joke) | BL-XX (mid-gesture toward other) | IL-05 (friend_group_dynamic) |
| Resting with viewer | EL-18 (resting_with_viewer) + EL-08 (neutral_plus) | BL-23 (mid_lean) (optional) | IL-09 (post_conversation) or IL-06 |

For setting-specific beats, the BL ref is the setting-specific action (e.g., BL-14 for pool, BL-15 or BL-16 for hotel, BL-40 for mirror, BL-37 or BL-39 for birthday).

---

## 9. The viewer-feels-personally-noticed checklist

The engine maintains a five-point checklist for the *viewer feels personally noticed* beat:

- [ ] **Eye contact with motion** — mitsumeru-me + micro-glance off-axis and back.
- [ ] **Body in motion** — mid-action with a defined end-state.
- [ ] **Suppression of expression** — mouth in a containment state.
- [ ] **Second body trace** — environmental element implies another person.
- [ ] **Self-touch or prop-touch** — hand on collar, finger on lip, hand on cup.

A frame that fails 0–1 of the checklist is *posed* or *candid* but not *teasing*. A frame that passes 2–3 is *partially teasing*. A frame that passes 4–5 is *strongly teasing*.

---

## 10. Playfulness scoring

```
overall = 0.18 * expression_specificity
        + 0.16 * behaviour_specificity
        + 0.14 * interaction_specificity
        + 0.20 * viewer_noticed_checklist_pass
        + 0.16 * personality_visibility
        + 0.16 * (1 - any_FP_match)
```

Each sub-score is 0–1:
- `expression_specificity`: 1.0 if EL ref resolves and the expression matches the beat, 0.0 if library-mismatch.
- `behaviour_specificity`: 1.0 if BL ref resolves and the behaviour matches the beat, 0.0 if mismatch.
- `interaction_specificity`: 1.0 if IL ref resolves and the interaction matches the beat, 0.0 if mismatch.
- `viewer_noticed_checklist_pass`: 0.0–1.0 based on how many of the 5 checklist items are passed.
- `personality_visibility`: 1.0 if the expression is *specific* to the character, 0.5 if generic, 0.0 if stock.
- `any_FP_match`: 1.0 if no FP matches, 0.0 if any matches.

A frame with `overall < 0.6` is rejected. `0.6 ≤ overall < 0.8` is passed but flagged. `overall ≥ 0.8` is passed without flag.

---

## 11. Interaction with sibling engines

### R017 ↔ R012 (Conversation Illusion)

R012 reads R017's `teasing_beat_ref` (EL-XX), `behaviour_ref` (BL-XX), `interaction_ref` (IL-XX). R012 writes the resolved `expression_state` back to R017.

### R017 ↔ R013 (Object Motivation)

R017 reads R013's `second_person_trace` to determine if the IL ref can be a "second body" interaction or a "second person trace" interaction.

### R017 ↔ R014 (Viewer Gaze)

R017 reads R014's `gaze_mode` to choose the appropriate EL ref (e.g., `mitsumeru_me` for EL-01, `recovered_from_away` for EL-05).

### R017 ↔ R015 (Luxury Intimate Fashion)

R017 reads R015's `garment_state` to determine the appropriate beat (e.g., `being_considered` garment → `shared_joke` beat).

### R017 ↔ R016 (Swimwear Design Language)

R017 reads R016's `garment_state` and `cover_layer.state` to determine the appropriate beat.

---

## 12. Version and changelog

**v0.1.0** (2026-06-05) — Initial engine module. Includes 35 Expression Library entries, 40 Behaviour Library entries, 25 Interaction Library entries. Canon status: BLOCKED.

**Planned for v0.2.0 (post-production-test):**
- Per-character tuning of the `default_beat` and `default_expression_ref`.
- Per-platform tuning of the beat frequency (Xiaohongshu prefers `shared_joke` and `playful_embarrassment`; Instagram prefers `settled` and `interrupted`).
- Library expansion: add 10–15 new entries per library based on production demand.

---

**End R017 engine spec.** Companion: `R017_FEMALE_TEASING_BEHAVIOUR_ENGINE.md` (research), `VERIFICATION_R017_FEMALE_TEASING.md` (verification), `FEMALE_TEASING_MANIFEST.md` (release manifest).
