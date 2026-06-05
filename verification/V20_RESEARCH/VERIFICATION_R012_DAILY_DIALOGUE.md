# R012 — Daily Dialogue Engine
## Self-Verification Protocol (v2 — lil.troublr)

**Canon status:** BLOCKED until production testing
**File pair:** `research/V20_RESEARCH/R012_DAILY_DIALOGUE_ENGINE.md` (research), `modules/V20/ENGINE_V20_DAILY_DIALOGUE_SYSTEM.md` (engine spec)
**Scope:** Per-rule compliance evidence, red-flag set, beat-specific verification, and test prompts. This file defines how to confirm a generated image satisfies the R012-01…R012-15 rules in the research file, before the rule is unblocked.

---

## 0. How to use this file

For every rule in §14 of the research file, this file defines:
- **(a) Evidence of compliance** — what the final image MUST show.
- **(b) Red flags of failure** — what would tell you the rule is not met.
- **(c) Test prompts** — concrete prompts to run through the production pipeline to check compliance.

Canon status for the whole R012 module is **BLOCKED** until the production team runs at least **30 test prompts per rule** and the verification checklist passes at ≥ 80% of prompts.

For beat-specific verification, see §3 — each beat (settled, interrupted, playful embarrassment, shared joke, etc.) has its own per-beat checklist.

---

## 1. Verification checklist — per rule

### R012-01 — Mitsumeru-me as default gaze

- **(a) Compliance evidence:**
  - Lid ratio 50–65% (upper lid covers roughly half to two-thirds of the iris).
  - Brow neutral. Frontalis not contracted.
  - Eye engagement 0.6+ on the engine's periorbital engagement scale.
  - Catchlight in the upper-30° position.
  - Gaze within ±5° of the camera.
- **(b) Red flags:**
  - Lid ratio < 40% (alert) or > 70% (sleepy).
  - Brow raised or furrowed.
  - Catchlight absent (dead eye reading).
  - Mid-blink frame.
- **(c) Test prompts:**
  1. "Subject in mitsumeru-me, soft gaze at camera, no smile, slight head tilt"
  2. "Lid 55%, neutral brow, catchlight upper-left, gaze held"
  3. NEGATIVE: "Wide eyes, alert, scanning" — must FAIL.

### R012-02 — Return-from-away residue

- **(a) Compliance evidence:**
  - Gaze vector carries a "just returned to the camera" signature.
  - Head may still be slightly off-axis from the away-look, with the eyes now on-axis (a counter-rotation).
  - The catchlight position is consistent with the slight head angle.
- **(b) Red flags:**
  - Eyes on camera the whole time (no away-look residue, performed stare).
  - Eyes caught mid-away-look and not returning (viewer is rejected).
  - Head angle too pronounced for "just-returned" state.
- **(c) Test prompts:**
  1. "Subject's eyes just returned to camera, head still slightly turned, catchlight in the recovery position"
  2. NEGATIVE: "Subject staring directly at camera, no away-look history" — must FAIL.

### R012-03 — Suppressed or decay smile as default mouth

- **(a) Compliance evidence:**
  - Mouth in suppression, decay, or neutral-plus state.
  - Eyes match the mouth (no "smiling mouth with dead eyes").
  - The mouth is in a "containment" state, not a "performance" state.
- **(b) Red flags:**
  - Full Duchenne smile as default (performance, not conversation).
  - Closed-lip smirk (smug, not warm).
  - Perfect neutral (model face).
- **(c) Test prompts:**
  1. "Suppressed smile, mouth 8mm open, eyes crinkled"
  2. "Decay smile, peak is over, eyes still on"
  3. NEGATIVE: "Big toothy smile, default state" — must FAIL.

### R012-04 — Asymmetric posture, always

- **(a) Compliance evidence:**
  - One shoulder higher than the other (visible in a non-square crop).
  - One hip weighted (in a wider crop).
  - Head tilt off-axis (5–20° from vertical).
- **(b) Red flags:**
  - Bilateral symmetry of shoulders, hips, head.
  - Both ears equally visible from a frontal head angle.
  - Spine perfectly vertical.
- **(c) Test prompts:**
  1. "Weight on left hip, right shoulder higher, head tilted 10° to her left"
  2. NEGATIVE: "Subject standing straight, symmetric shoulders" — must FAIL.

### R012-05 — Hands occupied, not posed

- **(a) Compliance evidence:**
  - At least one hand holding a real object (cup, phone, pen, own hair, own sleeve).
  - Hands NOT in classic modelling positions: not under chin, not in hair, not on neck, not on hip.
- **(b) Red flags:**
  - Hand under chin, in hair, on neck, on hip.
  - Both hands visible, both unoccupied (model-floating-hands).
- **(c) Test prompts:**
  1. "Subject holding a coffee cup, fingers around the body, relaxed grip"
  2. NEGATIVE: "Hand under chin, framing face" — must FAIL.

### R012-06 — In-progress body state

- **(a) Compliance evidence:**
  - Subject is mid-action with a clearly defined end-state.
  - The action is at a *between* beat (frame_offset_seconds between -1.0 and +1.5).
- **(b) Red flags:**
  - Fully static, no in-progress action.
  - Action has no plausible end-state.
  - Action is finished but the body is still in the action pose.
- **(c) Test prompts:**
  1. "Subject mid-sip, cup halfway to mouth, eyes at camera"
  2. "Subject mid-turn, body in motion, eyes caught the viewer"
  3. NEGATIVE: "Subject seated, hands in lap, looking at camera" — must FAIL.

### R012-07 — Second-person trace mandatory

- **(a) Compliance evidence:**
  - At least one environmental element implies a second person or the viewer's own presence.
  - Examples: second glass, second chair, half-written note, phone with message.
- **(b) Red flags:**
  - No implied second person.
  - Trace in a "feature" position (centred, in focus, isolated).
- **(c) Test prompts:**
  1. "Two coffee cups on a table, one in front, one across, both half-drunk"
  2. NEGATIVE: "Solo subject at a table for one, no second-person trace" — must FAIL.

### R012-08 — Environment in same temporal frame

- **(a) Compliance evidence:**
  - At least 2–3 environmental elements in the state of having been just used.
  - Elements are at the *time-of-day* implied by the lighting.
- **(b) Red flags:**
  - No in-progress residue anywhere.
  - In-progress residue that contradicts the time of day.
  - Uniform residue everywhere (over-acting).
- **(c) Test prompts:**
  1. "Morning room, unmade bed, half-drunk coffee, phone face-up showing recent text"
  2. NEGATIVE: "Pristine hotel room, no residue" — must FAIL.

### R012-09 — One and only one imperfection

- **(a) Compliance evidence:**
  - Exactly one imperfection visible: flyaway hair, smudged lipstick, half-buttoned shirt, tag still on, chipped nail, sock slightly down, pillow crease.
  - In a natural state, not a feature position.
- **(b) Red flags:**
  - Zero imperfections (AI-perfect read).
  - 2+ imperfections (over-acting).
  - Imperfection in a feature position.
- **(c) Test prompts:**
  1. "Subject with a single flyaway hair crossing her cheek"
  2. "Subject's cardigan half-buttoned, bottom button undone"
  3. NEGATIVE: "Flawlessly styled, no imperfection" — must FAIL.
  4. NEGATIVE: "Smudged lipstick, crooked collar, chipped nail" — must FAIL.

### R012-10 — No bilateral expression symmetry

- **(a) Compliance evidence:**
  - Mouth corners NOT at equal heights (one a few mm higher).
  - Eyebrows NOT at equal heights.
  - Scleral show asymmetric.
- **(b) Red flags:**
  - Perfectly symmetric mouth, eyebrows, eye state (AI tell).
  - Pronounced asymmetry (over-correcting).
- **(c) Test prompts:**
  1. "Slight smile, one corner of the mouth 4mm higher"
  2. NEGATIVE: "Perfectly symmetric, model-still expression" — must FAIL.

### R012-11 — Phone-camera OR clean DSLR, never mixed

- **(a) Compliance evidence (if phone-camera):** Shoulder-height perspective, env lighting, catchlight consistent.
- **(a) Compliance evidence (if DSLR):** Tripod or off-camera position, controlled but consistent lighting.
- **(b) Red flags:** Phone-camera with studio catchlights. DSLR with env-only lighting.
- **(c) Test prompts:**
  1. "Phone-camera perspective, window light, slight upward angle"
  2. "DSLR portrait, Rembrandt lighting, consistent catchlight"
  3. NEGATIVE: "Phone-camera framing with ring-light catchlight" — must FAIL.

### R012-12 — Crop at an emotional joint

- **(a) Compliance evidence:**
  - Crop at chin, wrist, elbow, knee, or mid-thigh.
  - Body continues *out of frame*.
- **(b) Red flags:** Crop at the waist (stock photo). Crop implying body *ends* at frame edge.
- **(c) Test prompts:**
  1. "Portrait cropped at the chin, shoulders extending out of frame"
  2. NEGATIVE: "Full body, subject standing far from camera" — must FAIL.

### R012-13 — Frame offset between -1.0s and +1.5s

- **(a) Compliance evidence:**
  - `frame_offset_seconds` is in range.
  - Default is +0.6s (decay frame).
- **(b) Red flags:** Offset outside range. Offset = 0.0 for "after" beats.
- **(c) Test prompts:**
  1. "Frame captured at +0.6s after a shared joke"
  2. NEGATIVE: "Frame at 0.0s for a 'post-laugh' beat" — must FAIL.

### R012-14 — One personal detail in the periphery

- **(a) Compliance evidence:**
  - At least one specific personal detail visible (watch, notebook, jewelry, brand).
  - In the periphery, not in the feature position.
- **(b) Red flags:** No personal detail. Personal detail in the feature position.
- **(c) Test prompts:**
  1. "Subject with a specific watch and a specific notebook, both visible in the periphery"
  2. NEGATIVE: "No personal details visible" — must FAIL.

### R012-15 — One incomplete pattern

- **(a) Compliance evidence:**
  - Exactly one element of the frame is implied but not fully shown.
- **(b) Red flags:** Zero incomplete patterns (frame is fully resolved). 2+ (over-fragmented).
- **(c) Test prompts:**
  1. "Subject with a hand entering the frame from off-screen, holding something"
  2. NEGATIVE: "Frame with no implied element" — must FAIL.

---

## 2. Forbidden pattern verification (from research file §14)

| FP ID | Pattern | Detection |
|---|---|---|
| FP-01 | Model stare (centred iris, no orbicularis) | Visual. Reject. |
| FP-02 | Symmetric 3/4 (head turned, eyes on-axis) | Visual. Reject. |
| FP-03 | Catchlight contradiction (catchlight vs face shadow direction) | Visual. Reject. |
| FP-04 | Pure performance (bilateral symmetry) | Visual. Reject. |
| FP-05 | Cliché tease (wink, bite-lip, peace sign, peace + wink, tongue, finger-gun) | Pattern match. Reject. |
| FP-06 | Smug × smug (closed-lip smirk + closed-lip smirk) | Visual. Reject. |
| FP-07 | Dead candid (phone-camera with studio catchlights) | Visual. Reject. |
| FP-08 | Empty environment (no second-person trace, no residue) | Visual. Reject. |
| FP-09 | Tableau freeze (no in-progress action, no implied beat offset) | Visual. Reject. |
| FP-10 | Full laugh (mouth fully open, teeth bared, no suppression) | Visual. Reject. |
| FP-11 | Nagasu-me (gaze fully averted, focus in distance) | Visual. Reject. |
| FP-12 | Theatrical blush (uniform red across cheeks) | Visual. Reject. |
| FP-13 | Hair flip (signals performance) | Visual. Reject. |

---

## 3. Beat-specific verification

### Settled beat (P033A template)

**Required elements:**
- Mitsumeru-me gaze (R012-01).
- Suppressed or decay smile (R012-03).
- Real-environment prop cluster (R012-08).
- Second-person trace (R012-07).
- Phone-camera framing (R012-11).
- Frame offset +0.6s (R012-13).

**Detection signal of success:** The viewer feels they are sitting with her, the joke was just told, she is still warm from it.

**Common failure modes:** Generic glamour shot with no environment. Bilateral symmetry. Perfect performance.

### Interrupted beat (P036B template)

**Required elements:**
- Caught-you-looking expression (eye just returned to camera, head slightly off).
- Return-from-away residue (R012-02).
- Phone-camera framing (R012-11).
- Second-person trace (R012-07).
- Asymmetric posture, body in motion (R012-04, R012-06).
- One imperfection (R012-09).

**Detection signal of success:** The viewer feels they just walked in on her, she has accepted their presence.

**Common failure modes:** Stare (eyes on camera the whole time, no recovery). Static body. No second-person trace.

### Playful embarrassment beat (P036C template)

**Required elements:**
- Three-beat gaze sequence: direct → indirect → direct (recovery).
- Cheek blush (subtle, character-dependent, sometimes ears).
- Suppressed laugh with containment (R012-03, trying-not-to-laugh).
- Hand near face (self-touch).
- One returning detail in the periphery (R012-14, R014 returning detail).
- Mid-speech or post-speech mouth state.
- Frame offset 0.0s (the recovery moment).

**Detection signal of success:** The viewer feels they made her blush.

**Common failure modes:** Theatrical blush (uniform red, looks like stage makeup). Hand on mouth without containment element. Eyes still averted (recovery not complete). Wink (cliché).

### Shared joke beat

**Required elements:**
- Decay smile (R012-03, post-punchline).
- Containment element (hand on lip, turned head, bitten lip, shoulder raised).
- Mitsumeru-me gaze (R012-01).
- One brow slightly raised.
- Second-person trace (R012-07).
- Frame offset +0.6s (decay).

**Detection signal of success:** The viewer feels the joke was just told, the warmth is on, she is the co-conspirator.

**Common failure modes:** Full Duchenne smile (peak, not decay). No containment element. Symmetric brows.

### Trying-not-to-laugh beat

**Required elements:**
- Mouth 5–10mm open, asymmetric.
- Buccinator engaged, lower lid pushed up.
- Containment element (hand on lip, turned head, bitten lip).
- Mitsumeru-me gaze (R012-01).
- Frame offset 0.0s (the suppression moment).

**Detection signal of success:** The viewer feels the laugh is being held back, they are admitted into the suppressed context.

**Common failure modes:** Full open laugh (no suppression). No containment (private, not shared). Bilateral mouth symmetry.

### Teasing beat

**Required elements:**
- Mitsumeru-me gaze with a micro-glance off-axis and back (R012-02).
- One corner of mouth higher than the other.
- One brow slightly raised.
- Self-touch or prop-touch element.
- Frame offset +0.3s.

**Detection signal of success:** The viewer feels she just said something, they are the audience for the tease.

**Common failure modes:** Static direct gaze. Bilateral symmetry. Wink (cliché). Bite-lip with eye contact (aggressive tease, not subtle).

### Caught-you-looking beat (recovery)

**Required elements:**
- Eyes just returned to camera.
- Head slightly off-axis.
- Mouth in settling state.
- Micro-flinch overridden.
- Slight cheek/ear reddening (optional, character-dependent).
- Hand in mid-gesture (the hand that was doing the private action).
- Frame offset 0.0s (the recovery moment).

**Detection signal of success:** The viewer feels they interrupted something private and have been granted access.

**Common failure modes:** Posed smile (the subject has already recovered). Direct eye contact from the start (she's been waiting for the camera). Stare (no away-look residue).

### Resting with viewer beat

**Required elements:**
- Mitsumeru-me gaze (R012-01).
- Neutral-plus mouth (R012-03).
- Settled body (no in-progress action, OR slow in-progress).
- Asymmetric posture (R012-04).
- Frame offset 0.0s.
- Second-person trace (R012-07) optional.

**Detection signal of success:** The viewer feels they are with her, not for her.

**Common failure modes:** Model face (bilateral neutral). Held static. No second-person trace.

---

## 4. P033A, P036B, P036C verification

For the three reference frames, the verification protocol checks against the *signature* of each.

### P033A — settled

- Real-environment prop cluster (study or home office).
- Mitsumeru-me + off-centre iris.
- Suppressed smile in decay.
- Asymmetric posture.
- Second-person trace (second cup, half-written note, chair recently sat in).
- Phone-camera framing.

**Pass:** All 6 elements present.
**Fail:** Any one missing.

### P036B — interrupted

- Caught-you-looking beat (recovery from away-look).
- Phone-camera framing.
- Return-from-away residue.
- Second-person trace (phone with message, half-written note).
- One imperfection (flyaway hair).
- Asymmetric posture, body in motion.

**Pass:** All 6 elements present.
**Fail:** Any one missing.

### P036C — playful embarrassment

- Three-beat gaze sequence (direct → indirect → direct).
- Cheek blush (subtle).
- Suppressed laugh with containment.
- Hand near face.
- One returning detail in periphery.
- Mid-speech or post-speech mouth state.

**Pass:** All 6 elements present.
**Fail:** Any one missing.

---

## 5. Test prompt library (lil.troublr framing)

The following 30 prompts are the baseline test set for R012 v2. Each prompt is run through the production pipeline and the resulting image is checked against the rule set.

```
P012-01  "Subject in a coffee shop, mitsumeru-me, suppressed smile, second cup across, phone-camera framing"
P012-02  "Subject at a desk, notebook open, pen in hand, eyes on camera, decay smile, half-written note"
P012-03  "Subject in a fitting room mirror, viewer caught her mid-look, eyes recovered to camera, post-punchline warmth"
P012-04  "Subject on a bed, one shoulder higher, head tilted, mitsumeru-me, neutral-plus mouth, flyaway hair"
P012-05  "Subject on a balcony, phone-camera, one earbud in, mitsumeru-me, return-from-away, half-read book"
P012-06  "Subject holding a phone, mitsumeru-me, message visible on phone screen, second-person trace"
P012-07  "Subject mid-sip, cup halfway to mouth, mitsumeru-me, second cup on the table"
P012-08  "Subject with weight on left hip, suppressed smile, head tilt, second-person trace"
P012-09  "Subject in a study, two coffee cups, half-written note, chair recently sat in, decay smile"
P012-10  "Subject on a couch, pillow creased under her head, half-read book on lap, mitsumeru-me"
P012-11  "Subject putting on a cardigan, one arm in, one arm out, eyes at camera, caught-you-looking beat"
P012-12  "Subject with a single flyaway hair, mitsumeru-me, suppressed smile, return-from-away"
P012-13  "Subject with a half-buttoned shirt, mitsumeru-me, decay smile, head tilt"
P012-14  "Subject with one corner of the mouth 4mm higher, mitsumeru-me, gaze held"
P012-15  "Subject with one eyebrow slightly raised, the other neutral, mitsumeru-me"
P012-16  "Phone-camera framing, window light, slight upward angle, mitsumeru-me, return-from-away"
P012-17  "DSLR portrait, Rembrandt lighting, consistent catchlight, mitsumeru-me"
P012-18  "Subject cropped at the chin, shoulders extending out of frame, mitsumeru-me"
P012-19  "Subject cropped at the elbows, hands holding an object, body continuing out of frame"
P012-20  "Subject in a morning room, unmade bed, half-drunk coffee, recent text on phone, mitsumeru-me"
P012-21  "Subject with an empty chair across, half-written note, chair recently sat in"
P012-22  "Subject with a hand on her own collar, casual adjustment, mitsumeru-me"
P012-23  "Subject mid-turn toward the viewer, body in motion, mitsumeru-me recovery"
P012-24  "Subject in mitsumeru-me mode, soft gaze, no smile, slight head tilt, return-from-away"
P012-25  "Subject with suppressed laugh, mouth 8mm open, eyes crinkled, containment hand on lip"
P012-26  "Subject with post-punchline decay, eyes still on, slight head forward, second cup"
P012-27  "Subject in a fitting room, half-undressed, viewer caught her, no posed smile, containment element"
P012-28  "Subject with eyes caught the camera mid-look-away, recovery beat, cheek blush subtle"
P012-29  "Subject with a private smile, mouth closed, one corner higher, eyes warm, return-from-away"
P012-30  "Subject with all 15 R012 rules satisfied (the canonical test frame)"
```

For the v2-specific beats, additional prompts:

```
P012-31  "Subject in playful embarrassment, three-beat gaze sequence, cheek blush subtle, suppressed laugh, hand near face"
P012-32  "Subject in caught-you-looking, eyes just returned, head slightly off, mouth in transit, second-person trace"
P012-33  "Subject in shared joke, decay smile, eyes crinkled, containment element, one brow raised, +0.6s offset"
P012-34  "Subject in trying-not-to-laugh, mouth 8mm open, containment hand, asymmetric mouth, mitsumeru-me"
P012-35  "Subject in teasing, mitsumeru-me + micro-glance, one corner of mouth higher, self-touch"
P012-36  "Subject in fake innocence, eyes wide (lid 35%), closed mouth, head tilt, palms up"
P012-37  "Subject in friend-group teasing, second body in frame, mid-interaction with friend"
P012-38  "Subject in mirror teasing, phone in mirror, one shoulder exposed, mid-adjustment"
P012-39  "Subject in birthday teasing, candle, party hat, cake crumbs, make-a-wish beat"
P012-40  "Subject in daily-life teasing, cooking, mid-chop, mitsumeru-me, mid-action"
```

---

## 6. Pass/fail threshold

**Per rule:** ≥ 80% of test prompts must pass.

**Per beat:** ≥ 80% of beat-specific test prompts must pass.

**For the R012 module as a whole:** ≥ 80% of test prompts must pass the *full* R012 checklist (all 15 rules + all 13 forbidden patterns + per-beat signatures).

**For the unblock decision:** the engine is run in production for 30 days on real prompts, and the production output is rated by a panel of 3 raters (blind to the engine rules) on:
- 1–5 scale for "conversation illusion" (does the frame feel like a real exchange?)
- 1–5 scale for "viewer feels personally noticed" (does the viewer feel admitted?)
- 1–5 scale for "viewer retention" (would the viewer re-look?)

Average rating ≥ 4.0 across all raters, all frames, and all three metrics is the unblock threshold.

---

## 7. R012 v2 unblock checklist (for the production team)

- [ ] All 40 test prompts run through the production pipeline.
- [ ] Each prompt's output image checked against R012-01…R012-15.
- [ ] Each prompt's output image checked against FP-01…FP-13.
- [ ] Each beat-specific prompt checked against the beat signature.
- [ ] Pass rate ≥ 80% per rule, ≥ 80% per beat, ≥ 80% overall.
- [ ] 30-day production run completed.
- [ ] 3-rater blind panel scoring ≥ 4.0 average.
- [ ] Canon status updated to "UNBLOCKED" in the engine file.

---

**End R012 v2 verification file.** Companion: `R012_DAILY_DIALOGUE_ENGINE.md` (research), `ENGINE_V20_DAILY_DIALOGUE_SYSTEM.md` (engine spec).
