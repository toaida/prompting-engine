# FEMALE_TEASING_MANIFEST

**Manifest ID:** MANIFEST-R017-V01
**Engine:** R017 Female Teasing Behaviour Engine
**Project:** lil.troublr
**Canon status:** BLOCKED (engine itself) — manifest is the *release* document, not the engine canon
**Version:** 0.1.0
**Last updated:** 2026-06-05
**Owner:** V20 production track (lil.troublr)

---

## 1. Purpose

This manifest declares the public surface of the R017 Female Teasing Behaviour Engine for downstream systems, partners, and production tooling. It specifies what the engine emits, what it consumes, and what the release criteria are.

The manifest is the *contract*; the engine is the *implementation*. The engine's core output is the three libraries (**Expression Library**, **Behaviour Library**, **Interaction Library**) that lil.troublr prompts can reference by ID.

---

## 2. Public surface

### 2.1 Engine identifier

```
engine_id: V20-ENG-017
engine_name: "Female Teasing Behaviour Engine"
project: "lil.troublr"
version: "0.1.0"
canon_status: "BLOCKED"
```

### 2.2 Engine purpose

```
purpose: |
  Give every generated frame a teasing beat that makes the viewer feel personally
  noticed. Convert posed frames (subject delivering a state to the camera) into
  teasing frames (subject responding to the viewer's presence, sharing a private
  joke, caught in a private moment).

core_output: |
  The three libraries: Expression Library (EL), Behaviour Library (BL), and
  Interaction Library (IL). These libraries are the canonical reference for
  all lil.troublr prompts.

objective: "playful interaction, viewer retention, social attraction, personality
            visibility — NOT posing."
```

### 2.3 Engine inputs (public subset)

```yaml
inputs:
  required:
    - persona_id: string
    - persona_teasing_signature: object
    - scene_id: string
    - scene_conversation_beat: enum
    - location_type: enum
    - teasing_beat: enum [settled, interrupted, playful_embarrassment, shared_joke,
                          teasing, trying_not_to_laugh, caught_you_looking,
                          fake_innocence, friend_group, resting_with_viewer]
    - expression_ref: EL-XX          # Expression Library reference
    - platform_target: enum
  optional:
    - behaviour_ref: BL-XX          # Behaviour Library reference
    - interaction_ref: IL-XX        # Interaction Library reference
```

### 2.4 Engine output (public)

The engine emits a JSON object of the form:

```json
{
  "engine_id": "V20-ENG-017",
  "version": "0.1.0",
  "timestamp": "<ISO 8601>",
  "beat": "settled | interrupted | playful_embarrassment | shared_joke | teasing | trying_not_to_laugh | caught_you_looking | fake_innocence | friend_group | resting_with_viewer",
  "expression_ref": "EL-XX",
  "behaviour_ref": "BL-XX",
  "interaction_ref": "IL-XX",
  "expression_state": {...},
  "behaviour_state": {...},
  "interaction_state": {...},
  "viewer_feels_personally_noticed_checklist": {
    "eye_contact_with_motion": true,
    "body_in_motion": true,
    "suppression_of_expression": true,
    "second_body_trace": true,
    "self_touch_or_prop_touch": true
  },
  "playfulness_score": {
    "expression_specificity": 0.0,
    "behaviour_specificity": 0.0,
    "interaction_specificity": 0.0,
    "viewer_noticed_checklist_pass": 0.0,
    "personality_visibility": 0.0,
    "any_FP_match": 0.0,
    "overall": 0.0
  }
}
```

### 2.5 Expression Library (35 entries)

The Expression Library is a curated set of named expressions. Public surface:

| ID | Name | Muscle pattern | Use |
|---|---|---|---|
| EL-01 | mitsumeru_me | lid 50–65%, neutral brow, gaze held | Default dialogue gaze |
| EL-02 | miseru_me | lid 80–90%, gaze held, mouth neutral | Caught-you-looking beat |
| EL-03 | nagasu_me | gaze offset 20°+, focus in distance | Private-moment beat (forbidden for dialogue) |
| EL-04 | half_lidded_flirty | lid 40–50%, neutral-plus asymmetric | Teasing, playful embarrassment |
| EL-05 | recovered_from_away | eyes just returned, head slightly off | Caught-you-looking residue |
| EL-06 | suppressed_smile | mouth 5–10mm open, buccinator engaged | Shared joke, teasing |
| EL-07 | decay_smile | mouth corners at 60–80% of full | Post-punchline warmth |
| EL-08 | neutral_plus | mouth corners at rest-plus | Resting, listening, secret-friend |
| EL-09 | trying_not_to_laugh | mouth 5–10mm open, containment | Shared joke, teasing, playful embarrassment |
| EL-10 | post_punchline | smile in decay, eyes still on | Shared joke |
| EL-11 | you_caught_me | eyes slightly wide, head mid-turn | Caught-you-looking |
| EL-12 | shared_joke | decay smile, eyes crinkled, one brow raised | Shared joke |
| EL-13 | teasing | one corner up, eyes engaged, one brow raised | Teasing |
| EL-14 | fake_innocence | eyes wide (lid 30–40%), closed mouth, head tilt | Post-tease |
| EL-15 | playful_embarrassment | cheek blush, suppressed laugh, hand near face | Playful embarrassment |
| EL-16 | listening | eyes on speaker, head tilted, neutral-plus | Resting, daily-life |
| EL-17 | thinking | gaze offset 10–20°, head tilted | Study, daily-life |
| EL-18 | resting_with_viewer | gaze held, neutral-plus, body relaxed | Secret-friend, daily-life |
| EL-19 | surprised | eyes wide, brows up, mouth open | Caught-you-looking |
| EL-20 | delight | full Duchenne smile | Post-surprise |
| EL-21 | satisfaction | subtle smile, gaze held | Post-choice |
| EL-22 | amused | half-smile, eyes crinkled | Shared joke, teasing |
| EL-23 | anticipation | eyes slightly wide, mouth slightly open | Pre-surprise |
| EL-24 | considering | gaze held, head tilted, neutral-plus | Fitting-room |
| EL-25 | caught_you_looking | eyes just returned, head off, mouth in transit | Caught-you-looking |
| EL-26 | mid_laugh | mouth open, teeth, eyes crinkled | Post-joke |
| EL-27 | mid_tease | one corner up, eyes engaged, one brow raised | Teasing |
| EL-28 | satisfied_smile | subtle smile, eyes settled, body relaxed | Post-choice |
| EL-29 | playful_embarrassment_asymmetric | one side of mouth higher, one-cheek blush | Playful embarrassment |
| EL-30 | post_laugh | smile in decay, eyes crinkled, breath residue | Shared joke |
| EL-31 | mid_speech | mouth in vowel shape, eyes on viewer | Pre/post-speech |
| EL-32 | listening_with_smile | slight smile, eyes on speaker, head tilted | Friend-group |
| EL-33 | amused_suppressed | trying-not-to-laugh with containment | Shared joke, teasing |
| EL-34 | caught_in_progress | eyes on camera mid-action, body in motion | Caught-you-looking |
| EL-35 | post_tease | one corner up, eyes engaged, body relaxed | Teasing |

### 2.6 Behaviour Library (40 entries, abbreviated)

The Behaviour Library is a curated set of named behaviours. Highlights (full list in research file Appendix B):

| ID | Name | Use |
|---|---|---|
| BL-01 | mid_sip | Mid-sip with cup at mouth |
| BL-02 | mid_turn | Mid-turn with body in rotation |
| BL-03 | mid_reach | Mid-reach toward an object |
| BL-04 | mid_laugh | Mid-laugh with head back |
| BL-05 | mid_cardigan_on | One arm in, one arm out |
| BL-06 | mid_button | Mid-button on a garment |
| BL-07 | mid_zip | Mid-zip with body in mirror |
| BL-08 | mid_brush | Mid-brush with hand in hair |
| BL-13 | mid_chop | Mid-chop with knife in hand |
| BL-14 | mid_emerging_from_water | One shoulder out, water on skin |
| BL-15 | mid_towel_adjust | Mid-towel-adjust in bathroom |
| BL-16 | mid_robe_on | Mid-robe-on in hotel room |
| BL-19 | mid_book_turn | Mid-page-turn on a book |
| BL-23 | mid_lean | Mid-lean against a surface |
| BL-28 | mid_hand_over_mouth | Containment for trying-not-to-laugh |
| BL-29 | mid_bit_lip | Tease containment |
| BL-33 | mid_turn_to_see_who_called | Mid-turn toward a sound |
| BL-37 | mid_blow_candle | Mid-blow on a candle |
| BL-39 | mid_make_wish | Eyes closed, mouth forming wish |
| BL-40 | mid_selfie_take | Mid-selfie in a mirror |

### 2.7 Interaction Library (25 entries, abbreviated)

The Interaction Library is a curated set of named interactions. Highlights (full list in research file Appendix C):

| ID | Name | Use |
|---|---|---|
| IL-01 | caught_you_looking | Subject's eyes just returned to the camera |
| IL-02 | interrupted | Subject was mid-action, viewer has appeared |
| IL-03 | teasing_viewer | Subject engaging with viewer playfully |
| IL-04 | shared_joke_with_implied_other | Subject in post-punchline state, with second body |
| IL-05 | friend_group_dynamic | Subject in a group, mid-interaction with friend |
| IL-06 | second_person_trace | Environmental element implies a second person |
| IL-07 | reacting_to_viewer | Subject responding to viewer's presence |
| IL-08 | mid_conversation | Subject in the middle of a conversation |
| IL-09 | post_conversation | Subject in the post-conversation state |
| IL-11 | in_progress_with_other | Subject mid-action with implied other |
| IL-12 | reacting_to_tease | Subject responding to a tease |
| IL-14 | reacting_to_compliment | Subject responding to a compliment |
| IL-16 | trying_not_to_laugh_with_other | Subject suppressing a laugh caused by the other |
| IL-17 | mid_tease_to_other | Subject teasing the implied other |
| IL-19 | mirror_self_interaction | Subject in a mirror, mid-interaction with her reflection |
| IL-20 | phone_self_interaction | Subject interacting with her phone |
| IL-22 | reacting_to_sound | Subject mid-turn toward a sound |
| IL-24 | self_touch_tease | Subject touching herself in a self-teasing way |

---

## 3. Public rules

The engine enforces 20 R017 rules. Downstream systems can validate outputs against these rules.

### Forbidden patterns (R017-specific, 13 patterns)

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

## 4. The three reference templates

### P033A — Settled

- **Beat:** `settled`
- **EL ref:** EL-01 (mitsumeru_me) + EL-07 (decay_smile)
- **BL ref:** BL-01 (mid_sip) or BL-19 (mid_book_turn)
- **IL ref:** IL-09 (post_conversation) or IL-06 (second_person_trace)

### P036B — Interrupted

- **Beat:** `interrupted`
- **EL ref:** EL-25 (caught_you_looking) or EL-34 (caught_in_progress)
- **BL ref:** BL-02 (mid_turn) or BL-33 (mid_turn_to_see_who_called)
- **IL ref:** IL-01 (caught_you_looking) or IL-02 (interrupted)

### P036C — Playful embarrassment

- **Beat:** `playful_embarrassment`
- **EL ref:** EL-15 (playful_embarrassment) or EL-29 (asymmetric)
- **BL ref:** BL-28 (mid_hand_over_mouth) or BL-29 (mid_bit_lip)
- **IL ref:** IL-07 (reacting_to_viewer) or IL-14 (reacting_to_compliment)

---

## 5. The viewer-feels-personally-noticed checklist (public)

A frame passes the "viewer feels personally noticed" checklist if all five are present:

- [ ] Eye contact with motion (mitsumeru-me + micro-glance off-axis and back).
- [ ] Body in motion (mid-action with a defined end-state).
- [ ] Suppression of expression (mouth in a containment state).
- [ ] Second body trace (environmental element implies another person).
- [ ] Self-touch or prop-touch (hand on collar, finger on lip, hand on cup).

A frame that fails 0–1 is *posed* or *candid* but not *teasing*. A frame that passes 4–5 is *strongly teasing*.

---

## 6. Release criteria

The engine can be released (canon status updated from BLOCKED to UNBLOCKED) when:

- [ ] All 40 verification test prompts pass at ≥ 80%.
- [ ] 30-day production run completed.
- [ ] 3-rater blind panel scoring ≥ 4.0 average on playfulness, viewer retention, personality visibility.
- [ ] Library refs (EL/BL/IL) resolve to real entries and match the beat.
- [ ] Documentation complete: research, verification, engine, manifest all present.
- [ ] All public surface (this manifest) is consistent with the engine implementation.

---

## 7. Compatibility

### Compatible with

- R012 (Conversation Illusion Engine) — bidirectional library-ref resolution.
- R013 (Object Motivation) — reads `second_person_trace` for IL-06 matching.
- R014 (Viewer Gaze) — reads `gaze_mode` for EL ref selection.
- R015 (Luxury Intimate Fashion) — reads `garment_state` for beat selection.
- R016 (Swimwear Design Language) — reads `garment_state` and `cover_layer.state` for beat selection.
- Persona Visual Anchor — reads `persona_teasing_signature`.
- Environment Engine — reads `location_type`.
- R011 (Scene Composition) — reads `scene_conversation_beat`.
- R018 (Platform Targeting) — reads `platform_target`.

### Incompatible with

- Engines not in the lil.troublr V20 stack.
- Production runs without the verification protocol.
- Outputs with `playfulness_score.overall < 0.6`.
- Library refs that don't resolve to real entries.

---

## 8. Versioning

| Version | Date | Changes | Canon status |
|---|---|---|---|
| 0.1.0 | 2026-06-05 | Initial manifest. 35 EL entries, 40 BL entries, 25 IL entries. 11 beats. 20 rules, 13 forbidden patterns. | BLOCKED |

Future versions will expand the libraries, add per-platform tuning, and add per-character defaults.

---

**End FEMALE_TEASING_MANIFEST.**
