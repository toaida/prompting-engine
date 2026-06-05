# R017 — Female Teasing Behaviour Engine
## Self-Verification Protocol

**Canon status:** BLOCKED until production testing
**File pair:** `research/V20_RESEARCH/R017_FEMALE_TEASING_BEHAVIOUR_ENGINE.md` (research), `modules/V20/ENGINE_V20_FEMALE_TEASING_BEHAVIOUR.md` (engine spec), `gpt-release/manifests/FEMALE_TEASING_MANIFEST.md` (release manifest)
**Scope:** Per-finding compliance evidence, red-flag set, beat-specific verification (settled, interrupted, playful embarrassment, etc.), library-usage verification (EL/BL/IL refs), and test prompts.

---

## 0. How to use this file

For every finding in §15 of the research file, this file defines:
- **(a) Evidence of compliance** — what the final image MUST show.
- **(b) Red flags of failure** — what would tell you the finding is not satisfied.
- **(c) Test prompts** — concrete prompts to run through the production pipeline.

Canon status for the whole R017 module is **BLOCKED** until the production team runs at least **30 test prompts per finding** and the verification checklist passes at ≥ 80% of prompts.

The engine's three libraries (Expression Library, Behaviour Library, Interaction Library) are referenced by ID (EL-XX, BL-XX, IL-XX) in the prompts. The verification checks that the library references resolve to real entries.

---

## 1. Verification — F-01 to F-20

### F-01 — Playful eye contact with micro-glance outperforms static direct gaze

- **(a) Compliance:** Mitsumeru-me + head slightly off-axis + return-from-away residue.
- **(b) Red flags:** Static direct gaze, no micro-glance.
- **(c) Test prompts:**
  1. "Subject with mitsumeru-me, head slightly off, return-from-away, micro-glance residue"
  2. NEGATIVE: "Subject staring directly at camera, no return-from-away" — must FAIL.

### F-02 — Caught-you-looking is the single highest-converting teasing beat

- **(a) Compliance:** Eyes just returned to camera, head slightly off, mouth in transit, micro-flinch overridden.
- **(b) Red flags:** Static direct gaze. Eyes averted without return.
- **(c) Test prompts:**
  1. "Subject mid-recovery from away-look, eyes just returned, head slightly off, mouth in transit"
  2. NEGATIVE: "Subject staring at camera, no recovery" — must FAIL.

### F-03 — Trying-not-to-laugh requires a containment element

- **(a) Compliance:** Mouth 5–10mm open + containment element (hand on lip, turned head, bitten lip, shoulder raised).
- **(b) Red flags:** Mouth open without containment.
- **(c) Test prompts:**
  1. "Subject with suppressed laugh, hand on lip, asymmetric mouth, mitsumeru-me"
  2. NEGATIVE: "Subject mid-laugh, no containment" — must FAIL.

### F-04 — Shared-joke expressions are the *post-punchline* state

- **(a) Compliance:** Decay smile, eyes crinkled, one brow slightly raised, micro-glance residue.
- **(b) Red flags:** Full Duchenne smile (peak, not decay).
- **(c) Test prompts:**
  1. "Subject with decay smile, eyes crinkled, one brow raised, micro-glance off-axis and back"
  2. NEGATIVE: "Subject with full Duchenne smile" — must FAIL.

### F-05 — Fake innocence is the *I don't know* beat

- **(a) Compliance:** Eyes wide (lid 30–40%), closed mouth, head tilt, palms up.
- **(b) Red flags:** Open mouth, surprise, full smile.
- **(c) Test prompts:**
  1. "Subject with eyes wide, closed mouth, head tilt, palms up"
  2. NEGATIVE: "Subject with open mouth surprise" — must FAIL.

### F-06 — Playful embarrassment is the *I just got caught* beat

- **(a) Compliance:** Three-beat gaze sequence (direct → indirect → direct), cheek blush subtle, suppressed laugh with containment, hand near face.
- **(b) Red flags:** Theatrical blush (uniform red). No containment. Eyes still averted.
- **(c) Test prompts:**
  1. "Subject in playful embarrassment, three-beat gaze, subtle cheek blush, suppressed laugh, hand near face"
  2. NEGATIVE: "Subject with uniform red cheeks, no containment, eyes still averted" — must FAIL.

### F-07 — Friend-group teasing requires a second body

- **(a) Compliance:** Second body in frame (hand on shoulder, face next to, body behind) OR strong implied second body.
- **(b) Red flags:** No second body in a "friend group" beat.
- **(c) Test prompts:**
  1. "Subject with a hand on her shoulder from a friend, mid-laugh with the friend"
  2. NEGATIVE: "Solo subject, no second body" — must FAIL (in a friend-group beat).

### F-08 — Beach teasing vocabulary

- **(a) Compliance:** Beach-specific props (towel, sunglasses pushed up, hat tilted back, sand on the body, beach bag, sun, ocean).
- **(b) Red flags:** No beach props in a beach beat.
- **(c) Test prompts:**
  1. "Subject on a beach, towel draped, sunglasses pushed up, sand on her shoulder, mitsumeru-me"
  2. NEGATIVE: "Subject on a beach, no beach props" — must FAIL.

### F-09 — Pool teasing vocabulary

- **(a) Compliance:** Pool-specific props (water on the skin, wet hair, one shoulder out, pool edge, pool reflection, sunglasses on head, wet swimwear).
- **(b) Red flags:** No pool props in a pool beat.
- **(c) Test prompts:**
  1. "Subject at a pool, one shoulder out, water on her skin, wet hair, mitsumeru-me"
  2. NEGATIVE: "Subject at a pool, dry, no water" — must FAIL.

### F-10 — Hotel teasing vocabulary

- **(a) Compliance:** Hotel-specific props (bathrobe, hotel slipper, room key, the bed, hotel art, mini-bar/room service tray, curtain, bathroom visible).
- **(b) Red flags:** No hotel props in a hotel beat.
- **(c) Test prompts:**
  1. "Subject in a hotel room, bathrobe half-off, room key on the nightstand, mitsumeru-me"
  2. NEGATIVE: "Subject in a hotel room, no hotel props" — must FAIL.

### F-11 — Mirror teasing vocabulary

- **(a) Compliance:** Mirror-specific props (phone in the mirror, one shoulder exposed, mid-adjustment, the mirror frame, the phone case).
- **(b) Red flags:** No mirror props in a mirror beat.
- **(c) Test prompts:**
  1. "Subject taking a mirror selfie, phone in the mirror, one shoulder exposed, mid-adjustment"
  2. NEGATIVE: "Subject in front of a mirror, no phone" — must FAIL.

### F-12 — Birthday teasing vocabulary

- **(a) Compliance:** Birthday-specific props (candle, party hat (ironic), cake crumbs, the "make a wish" beat, balloon, confetti, the "this many" fingers).
- **(b) Red flags:** No birthday props in a birthday beat.
- **(c) Test prompts:**
  1. "Subject blowing a candle, cake crumbs on her face, ironic party hat, mitsumeru-me"
  2. NEGATIVE: "Subject at a birthday, no birthday props" — must FAIL.

### F-13 — Daily-life teasing vocabulary

- **(a) Compliance:** Daily-life props (cooking, eating, drinking, getting ready, in transit, reading, listening to music).
- **(b) Red flags:** No daily-life props in a daily-life beat.
- **(c) Test prompts:**
  1. "Subject mid-chop in a kitchen, knife in hand, mitsumeru-me, mid-action"
  2. NEGATIVE: "Subject in a daily-life setting, no daily-life props" — must FAIL.

### F-14 — Japanese gravure interaction vocabulary

- **(a) Compliance:** Gravure-specific elements (eye that watches, towel that slips, uniform that tightens, off-shoulder state, back-view, leg-up, hair-pull, hand-on-collar, leaning-forward).
- **(b) Red flags:** No gravure elements in a gravure beat.
- **(c) Test prompts:**
  1. "Subject in a bathrobe, towel slipping, mitsumeru-me, one shoulder exposed"
  2. NEGATIVE: "Subject in a bathrobe, fully covered, no slip" — must FAIL.

### F-15 — Korean lifestyle editorial vocabulary

- **(a) Compliance:** Korean-specific elements (secret friend, settled gaze, in-progress moment, personal detail, high subject-to-frame ratio, emotional-joint crop, asymmetric environment).
- **(b) Red flags:** No Korean elements in a Korean beat.
- **(c) Test prompts:**
  1. "Subject in a high subject-to-frame ratio, settled gaze, personal detail in the periphery, mitsumeru-me"
  2. NEGATIVE: "Subject in a wide frame, no personal details" — must FAIL.

### F-16 — Personality visibility is the *meta* rule

- **(a) Compliance:** Real expression + real posture + real environment + real timing + real interaction.
- **(b) Red flags:** Stock expression, stock posture, stock environment, no personality signal.
- **(c) Test prompts:**
  1. "Subject with a *her* expression (specific to her face), *her* posture, *her* environment, mitsumeru-me"
  2. NEGATIVE: "Subject with a stock model expression" — must FAIL.

### F-17 — P033A succeeded (settled beat)

- **(a) Compliance:** Real-environment prop cluster + mitsumeru-me + suppressed smile + second-person trace + phone-camera framing.
- **(b) Red flags:** No environment, model stare, no second-person trace.
- **(c) Test prompts:**
  1. "Subject in a real study, mitsumeru-me, suppressed smile, second cup on the table, phone-camera framing"
  2. NEGATIVE: "Subject in a studio, no environment, no second-person trace" — must FAIL.

### F-18 — P036B succeeded (interrupted beat)

- **(a) Compliance:** Caught-you-looking + phone-camera + second-person trace + one imperfection + asymmetric posture.
- **(b) Red flags:** Static gaze, no return-from-away, no imperfection.
- **(c) Test prompts:**
  1. "Subject mid-recovery, phone-camera framing, second-person trace, flyaway hair, asymmetric posture"
  2. NEGATIVE: "Subject staring at camera, no recovery" — must FAIL.

### F-19 — Containment + reveal is the teasing engine

- **(a) Compliance:** Containment element + reveal element in the same frame.
- **(b) Red flags:** Containment without reveal (private) or reveal without containment (overt).
- **(c) Test prompts:**
  1. "Subject with hand on lip (containment) and one shoulder exposed (reveal)"
  2. NEGATIVE: "Subject with hand on lip but no reveal" — must FAIL.

### F-20 — Viewer feels personally noticed when eyes are on AND body is in motion

- **(a) Compliance:** Mitsumeru-me + mid-action body state.
- **(b) Red flags:** Mitsumeru-me + static body. Mid-action + averted gaze.
- **(c) Test prompts:**
  1. "Subject with mitsumeru-me + mid-turn body state"
  2. NEGATIVE: "Subject with mitsumeru-me + static body" — must FAIL.

---

## 2. Library reference verification (EL / BL / IL)

The engine's three libraries (EL, BL, IL) are referenced by ID. The verification checks:

### EL-01 to EL-35 (Expression Library)

- Each EL-XX ref in the prompt must resolve to a real entry.
- The entry's `muscle_pattern` must match the prompt's `expression_state`.
- The entry's `pairs_with` and `avoid_with` rules must be respected.

### BL-01 to BL-40 (Behaviour Library)

- Each BL-XX ref in the prompt must resolve to a real entry.
- The entry's `action` must match the prompt's `behaviour_state`.
- The entry's `pairs_with` rules must be respected.

### IL-01 to IL-25 (Interaction Library)

- Each IL-XX ref in the prompt must resolve to a real entry.
- The entry's `type` must match the prompt's `interaction_state`.
- The entry's `second_body`, `self_touch`, `prop_touch` rules must be respected.

### Library mismatch detection

If a prompt references EL-15 (playful_embarrassment) but specifies a "static body" behaviour, the library mismatch is flagged. The prompt must be rewritten to align the library refs.

---

## 3. Beat-specific verification (the four main beats)

### Settled beat (P033A template)

- **Required library refs:** EL-01 (mitsumeru-me) or EL-08 (neutral_plus), EL-06 (suppressed_smile) or EL-07 (decay_smile), BL-XX (mid-action, optional), IL-09 (post_conversation) or IL-06 (second_person_trace).
- **Detection signal of success:** The viewer feels they are sitting with her, the joke was just told.
- **Common failure modes:** Generic glamour shot. Bilateral symmetry. Perfect performance.

### Interrupted beat (P036B template)

- **Required library refs:** EL-05 (recovered_from_away) or EL-25 (caught_you_looking), EL-08 (neutral_plus) or EL-06 (suppressed_smile), BL-02 (mid_turn) or BL-XX (other mid-action), IL-01 (caught_you_looking) or IL-02 (interrupted) or IL-06 (second_person_trace).
- **Detection signal of success:** The viewer feels they just walked in on her, she has accepted their presence.
- **Common failure modes:** Stare. Static body. No second-person trace.

### Playful embarrassment beat (P036C template)

- **Required library refs:** EL-15 (playful_embarrassment) or EL-29 (playful_embarrassment_asymmetric), EL-09 (trying_not_to_laugh) with containment, BL-28 (mid_hand_over_mouth) or BL-29 (mid_bit_lip), IL-07 (reacting_to_viewer) or IL-14 (reacting_to_compliment).
- **Detection signal of success:** The viewer feels they made her blush.
- **Common failure modes:** Theatrical blush. No containment. Eyes still averted.

### Trying-not-to-laugh beat

- **Required library refs:** EL-09 (trying_not_to_laugh) with containment, EL-01 (mitsumeru-me), BL-28 (mid_hand_over_mouth) or BL-XX (other containment behaviour), IL-16 (trying_not_to_laugh_with_other) or IL-04 (shared_joke_with_implied_other).
- **Detection signal of success:** The viewer feels the laugh is being held back, they are admitted into the suppressed context.
- **Common failure modes:** Full open laugh. No containment. Bilateral mouth symmetry.

### Teasing beat

- **Required library refs:** EL-13 (teasing) or EL-27 (mid_tease), EL-01 (mitsumeru-me), BL-XX (self-touch or prop-touch), IL-03 (teasing_viewer) or IL-17 (mid_tease_to_other).
- **Detection signal of success:** The viewer feels she just said something, they are the audience for the tease.
- **Common failure modes:** Static direct gaze. Bilateral symmetry. Wink (cliché).

### Caught-you-looking beat (recovery)

- **Required library refs:** EL-25 (caught_you_looking) or EL-34 (caught_in_progress), EL-08 (neutral_plus) or in-transit mouth, BL-02 (mid_turn) or BL-33 (mid_turn_to_see_who_called), IL-01 (caught_you_looking) or IL-22 (reacting_to_sound).
- **Detection signal of success:** The viewer feels they interrupted something private and have been granted access.
- **Common failure modes:** Stare. Static body. No second-person trace.

### Resting with viewer beat

- **Required library refs:** EL-18 (resting_with_viewer), EL-08 (neutral_plus), BL-XX (slow in-progress, optional), IL-09 (post_conversation) or IL-06 (second_person_trace).
- **Detection signal of success:** The viewer feels they are with her, not for her.
- **Common failure modes:** Model face. Held static. No second-person trace.

---

## 4. Forbidden pattern verification (R017-specific)

| FP ID | Pattern | Detection |
|---|---|---|
| FP-17-01 | Static direct gaze with no micro-glance | Visual. Reject. |
| FP-17-02 | Caught-you-looking without recovery (still averted) | Visual. Reject. |
| FP-17-03 | Trying-not-to-laugh without containment | Visual. Reject. |
| FP-17-04 | Shared-joke at peak (full Duchenne) | Visual. Reject. |
| FP-17-05 | Fake innocence with open mouth | Visual. Reject. |
| FP-17-06 | Theatrical blush (uniform red) | Visual. Reject. |
| FP-17-07 | Friend-group with no second body | Visual. Reject. |
| FP-17-08 | Beach/pool/hotel/birthday/daily-life beat with no setting-specific props | Visual. Reject. |
| FP-17-09 | Wink (cliché) | Pattern match. Reject. |
| FP-17-10 | Bite-lip with eye contact (aggressive tease) | Visual. Reject. |
| FP-17-11 | Hair flip (signals performance) | Visual. Reject. |
| FP-17-12 | Library ref doesn't resolve | Prompt analysis. Reject. |
| FP-17-13 | Library ref contradicts the beat | Prompt analysis. Reject. |

---

## 5. Test prompt library (with library refs)

The following 30 prompts are the baseline test set for R017. Each prompt references library entries (EL-XX, BL-XX, IL-XX).

```
P017-01  "Subject with EL-01 + EL-06, BL-01, IL-06 (settled beat, suppressed smile, mid-sip, second-person trace)"
P017-02  "Subject with EL-05 + EL-08, BL-02, IL-01 (interrupted beat, recovered from away, mid-turn, caught-you-looking)"
P017-03  "Subject with EL-15 + EL-09, BL-28, IL-07 (playful embarrassment, suppressed laugh with containment, mid-hand-over-mouth, reacting to viewer)"
P017-04  "Subject with EL-09 + EL-01, BL-28, IL-16 (trying-not-to-laugh, mitsumeru-me, mid-hand-over-mouth, with implied other)"
P017-05  "Subject with EL-07 + EL-12, BL-19, IL-04 (shared joke decay, eyes crinkled, mid-book-turn, shared joke with other)"
P017-06  "Subject with EL-13 + EL-01, BL-24, IL-03 (teasing, mitsumeru-me, mid-stretch, teasing viewer)"
P017-07  "Subject with EL-14 + BL-XX, IL-12 (fake innocence, palms up, reacting to tease)"
P017-08  "Subject with EL-25 + EL-08, BL-33, IL-22 (caught-you-looking, neutral-plus, mid-turn-to-see, reacting to sound)"
P017-09  "Subject with EL-18 + EL-08, BL-23, IL-09 (resting with viewer, neutral-plus, mid-lean, post-conversation)"
P017-10  "Subject with EL-29 + EL-09, BL-29, IL-14 (playful embarrassment asymmetric, mid-bit-lip, reacting to compliment)"
P017-11  "Subject with EL-11 + EL-08, BL-XX, IL-07 (you-caught-me, neutral-plus, mid-action, reacting to viewer)"
P017-12  "Subject with EL-04 + EL-13, BL-XX, IL-03 (half-lidded flirty, teasing, mid-touch, teasing viewer)"
P017-13  "Subject with EL-21 + EL-08, BL-XX, IL-XX (satisfaction, neutral-plus, mid-pose, after-choice)"
P017-14  "Subject with EL-22 + EL-01, BL-XX, IL-04 (amused, mitsumeru-me, mid-pose, shared joke with other)"
P017-15  "Subject with EL-25 + EL-29, BL-29, IL-14 (caught-you-looking, playful-embarrassment-asymmetric, mid-bit-lip, reacting to compliment)"
P017-16  "Subject with EL-30 + EL-07, BL-XX, IL-04 (post-laugh, decay smile, mid-pose, shared joke with other)"
P017-17  "Subject with EL-31 + EL-01, BL-XX, IL-08 (mid-speech, mitsumeru-me, mid-pose, mid-conversation)"
P017-18  "Subject with EL-32 + EL-01, BL-XX, IL-13 (listening-with-smile, mitsumeru-me, mid-pose, reacting to surprise)"
P017-19  "Subject with EL-33 + EL-09, BL-28, IL-04 (amused-suppressed, trying-not-to-laugh, mid-hand-over-mouth, shared joke with other)"
P017-20  "Subject with EL-34 + EL-08, BL-02, IL-22 (caught-in-progress, neutral-plus, mid-turn, reacting to sound)"
P017-21  "Subject with EL-35 + EL-13, BL-XX, IL-03 (post-tease, teasing, mid-pose, teasing viewer)"
P017-22  "Subject with EL-12 + EL-07, BL-XX, IL-04 (shared joke, decay smile, mid-pose, shared joke with other)"
P017-23  "Subject with EL-15 + EL-09, BL-29, IL-14 (playful embarrassment, trying-not-to-laugh, mid-bit-lip, reacting to compliment)"
P017-24  "Subject with EL-29 + EL-08, BL-29, IL-12 (playful-embarrassment-asymmetric, neutral-plus, mid-bit-lip, reacting to tease)"
P017-25  "Subject with EL-25 + EL-06, BL-XX, IL-01 (caught-you-looking, suppressed smile, mid-pose, caught-you-looking)"
P017-26  "Subject with EL-04 + EL-13, BL-XX, IL-03 (half-lidded-flirty, teasing, mid-pose, teasing viewer)"
P017-27  "Subject with EL-18 + EL-08, BL-XX, IL-06 (resting with viewer, neutral-plus, mid-pose, second-person trace)"
P017-28  "Subject with EL-12 + EL-09, BL-28, IL-04 (shared joke, trying-not-to-laugh, mid-hand-over-mouth, shared joke with other)"
P017-29  "Subject with EL-29 + EL-15, BL-XX, IL-07 (playful-embarrassment-asymmetric, playful embarrassment, mid-pose, reacting to viewer)"
P017-30  "Subject with all R017 rules satisfied (the canonical test frame)"
```

For setting-specific beats, additional prompts:

```
P017-31  "Subject in a beach beat, BL-XX (towel/sunglasses/hat), IL-06, EL-01"
P017-32  "Subject in a pool beat, BL-14 (mid_emerging_from_water), IL-06, EL-01"
P017-33  "Subject in a hotel beat, BL-15 (mid_towel_adjust) or BL-16 (mid_robe_on), IL-06, EL-01"
P017-34  "Subject in a mirror beat, BL-40 (mid_selfie_take) or BL-32 (mid_look_in_mirror), IL-19, EL-01"
P017-35  "Subject in a birthday beat, BL-37 (mid_blow_candle) or BL-39 (mid_make_wish), IL-13, EL-13"
P017-36  "Subject in a daily-life beat, BL-11 (mid_taste) or BL-12 (mid_stir) or BL-13 (mid_chop), IL-08, EL-01"
P017-37  "Subject in a friend-group beat, IL-05, EL-12, BL-XX"
P017-38  "Subject in a Japanese gravure beat, BL-XX (off-shoulder / back-view), IL-XX, EL-01"
P017-39  "Subject in a Korean editorial beat, EL-18, IL-09, BL-XX"
P017-40  "Subject in P033A template (settled), IL-06, EL-01 + EL-06, BL-01"
```

---

## 6. Pass/fail threshold

**Per finding:** ≥ 80% of test prompts must pass.

**Per beat:** ≥ 80% of beat-specific test prompts must pass.

**Per library ref:** 100% of EL/BL/IL refs must resolve to real entries. Library-mismatch prompts are rejected before scoring.

**For the R017 module as a whole:** ≥ 80% of test prompts must pass the *full* R017 checklist.

**For the unblock decision:** the engine is run in production for 30 days on real prompts, and the production output is rated by a panel of 3 raters (blind to the engine rules) on:
- 1–5 scale for "playfulness" (does the frame feel teasing?).
- 1–5 scale for "viewer retention" (would the viewer re-look?).
- 1–5 scale for "personality visibility" (does the viewer see a *person*?).

Average rating ≥ 4.0 across all raters, all frames, and all three metrics is the unblock threshold.

---

## 7. R017 unblock checklist

- [ ] All 40 test prompts run through the production pipeline.
- [ ] Each output image checked against F-01…F-20.
- [ ] Each output image checked against FP-17-01…FP-17-13.
- [ ] Each beat-specific prompt checked against the beat signature.
- [ ] Each library ref (EL/BL/IL) resolves and matches the beat.
- [ ] Pass rate ≥ 80% per finding, ≥ 80% per beat, ≥ 80% overall.
- [ ] 30-day production run completed.
- [ ] 3-rater blind panel scoring ≥ 4.0 average.
- [ ] Canon status updated to "UNBLOCKED" in the engine file.

---

**End R017 verification file.** Companion: `R017_FEMALE_TEASING_BEHAVIOUR_ENGINE.md` (research), `ENGINE_V20_FEMALE_TEASING_BEHAVIOUR.md` (engine spec), `FEMALE_TEASING_MANIFEST.md` (release manifest).
