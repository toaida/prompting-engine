# R014 — Viewer Gaze Engine
## Self-Verification Protocol

**Canon status:** BLOCKED until production testing
**File pair:** R014_VIEWER_GAZE_ENGINE.md (research), ENGINE_V20_VIEWER_GAZE_SYSTEM.md (engine spec)
**Scope:** Per-rule compliance evidence, red-flag set, and test prompts. This file defines how to confirm a generated image actually satisfies the R014-01…R014-12 rules in the research file, before the rule is unblocked.

---

## 0. How to use this file

For every rule in §13 of the research file, this file defines:
- **(a) Evidence of compliance** — what the final image MUST show.
- **(b) Red flags of failure** — what would tell you the rule is not met.
- **(c) Test prompts** — concrete prompts to run through the production pipeline to check compliance.

The success metric is the viewer's behaviour after the first second — specifically, the 3-second hold rate and the re-look rate. The verification protocol tests the image against the rules *and* the image against the gaze-itinerary contract (the JSON output schema in the engine spec).

Canon status for the whole R014 module is **BLOCKED** until the production team runs at least **30 test prompts per rule** and the verification checklist passes at ≥ 80% of prompts.

---

## 1. Verification checklist — per rule

### R014-01 — Mitsumeru-me default

- **(a) Compliance evidence:**
  - Lid ratio 50–65% (upper lid covers roughly half to two-thirds of the iris).
  - Brow neutral. Frontalis not contracted.
  - Eye engagement 0.6+ on the engine's periorbital engagement scale.
  - Catchlight in the upper-30° position (slightly above the iris centre, on the side consistent with the key light).
  - No blink (the eye is open and held).
- **(b) Red flags:**
  - Lid ratio < 40% = alert / scanning. Wrong mode.
  - Lid ratio > 70% = sleepy / disinterested. Wrong mode.
  - Brow up = surprised. Wrong mode.
  - Brow furrowed = hostile. Wrong mode.
  - Eye in mid-blink = "between moments", drops retention.
  - Catchlight absent = dead eye reading.
- **(c) Test prompts:**
  1. "Subject in mitsumeru-me, lid half-closed, soft gaze at camera, neutral brow, no smile"
  2. "The eye that watches you, gaze held, upper lid covering 60% of the iris, catchlight upper-left"
  3. NEGATIVE: "Wide eyes, alert, scanning" — must FAIL R014-01.

### R014-02 — Three-plane anchoring

- **(a) Compliance evidence:**
  - At least one anchor at the *foreground* depth plane (a hand, a prop, a piece of clothing, closer to the lens than the face).
  - At least one anchor at the *mid-ground* depth plane (the face itself, or a piece of furniture behind the subject).
  - At least one anchor at the *background* depth plane (a wall detail, a window, a piece of text, a small object in the distance).
  - The anchors are at *different focal sharpness* — the face is the sharpest, the mid-ground is partially soft, the background is the softest.
- **(b) Red flags:**
  - All anchors at the same depth = single-plane composition.
  - Face is not one of the anchors = face has been deprioritised.
  - Background is sharper than the face = eye lands on the background, not the face.
  - No foreground anchor = eye lands on the face and stops.
- **(c) Test prompts:**
  1. "Subject with a coffee cup in the foreground (sharp), face in the mid-ground (sharp), window in the background (soft)"
  2. "Subject with a hand on her own shoulder in the foreground, face sharp, a bookshelf in the background, soft"
  3. NEGATIVE: "Subject's face only, no foreground or background anchor" — must FAIL R014-02.

### R014-03 — Face-first hierarchy

- **(a) Compliance evidence:**
  - Face is in the upper third of the frame.
  - Face is the largest element in the frame (occupies ≥ 35% of frame area).
  - Face is the sharpest element (eyes in focus, lashes crisp).
  - Face is the brightest element (key light is on the face, or the face is the brightest mid-tone in the frame).
  - Face has no occlusion (no hand, hair, prop, or shadow crosses the face plane).
- **(b) Red flags:**
  - Face area < 25% of frame.
  - Face darker than the surroundings.
  - Background or foreground sharper than the face.
  - Anything crosses the face plane (a strand of hair, a hand, a prop).
  - Face not in the upper third (cropped at the chin, or below the eyes).
- **(c) Test prompts:**
  1. "Portrait, face in upper third, face sharp and bright, hands in the lower frame holding a prop, no occlusion of the face"
  2. NEGATIVE: "Full body, face at the centre, busy environment competing" — must FAIL R014-03.

### R014-04 — Suppressed or decay smile default

- **(a) Compliance evidence:**
  - Mouth state is one of: "suppressed", "decay", "neutral-plus", "parted".
  - The smile (if present) is not at full Duchenne.
  - The eyes match the mouth (no "smiling mouth with dead eyes").
  - The mouth is in a "containment" state, not a "performance" state.
- **(b) Red flags:**
  - Full Duchenne smile as the default = performance, not conversation.
  - Closed-lip smirk = smug, not warm.
  - Mouth at perfect neutral = "model face", no warmth.
  - Big toothy grin = over-performance.
- **(c) Test prompts:**
  1. "Subject with a suppressed smile, mouth open 5mm, eyes crinkled"
  2. "Subject with a decay smile, the peak is over, eyes still on"
  3. "Subject with a neutral-plus mouth, no smile, but the corners are at rest-plus"
  4. NEGATIVE: "Big toothy smile, default state" — must FAIL R014-04.

### R014-05 — Return-from-away residue

- **(a) Compliance evidence:**
  - The eyes have just returned to the camera from a brief away-look.
  - The head may still be slightly off-axis from the away-look, with the eyes now on-axis (a counter-rotation).
  - The catchlight position is consistent with the slight head angle.
  - The mouth is in a "settling" state, not a "performed" state.
- **(b) Red flags:**
  - The eyes have been on the camera the whole time = no away-look residue, performed stare.
  - The eyes are caught mid-away-look and not returning = the viewer is rejected.
  - The head angle is too pronounced for a "just-returned" state = the recovery is incomplete.
- **(c) Test prompts:**
  1. "Subject's eyes just returned to the camera, head still slightly turned, catchlight in the recovery position"
  2. "Subject caught in the recovery beat of an away-look, gaze re-engaging the viewer"
  3. NEGATIVE: "Subject staring directly at camera, no away-look history" — must FAIL R014-05.

### R014-06 — Personal detail density 2–3

- **(a) Compliance evidence:**
  - Exactly 2–3 *specific* personal details are visible in the frame.
  - Each detail is identifiable (a real brand, a real product, a real name, a real place, a real handwritten text, a real piece of jewelry with a specific style).
  - The details are consistent with the character (a watch she would actually wear, a notebook she would actually use).
- **(b) Red flags:**
  - 0 personal details = generic, no character.
  - 1 personal detail = under-specific.
  - 4+ personal details = over-specific, gaze fragments.
  - "Generic" personal details (a "nice" cup, a "fashionable" bag) = no specificity.
- **(c) Test prompts:**
  1. "Subject with a specific watch (e.g., a vintage Seiko), a specific notebook (Moleskine, half-written), a specific pen (Lamy Safari)"
  2. "Subject with a specific piece of jewelry, a specific mug, a specific phone case"
  3. NEGATIVE: "Subject with a generic nice cup, a generic nice notebook" — must FAIL R014-06.

### R014-07 — Second-person trace mandatory

- **(a) Compliance evidence:**
  - At least one environmental element that implies a second person or the viewer's own presence.
  - Examples: a second glass, a second chair, a half-written note, a phone with a message, a coffee cup across the table, a half-set place at a meal.
  - The trace is in a *natural* position, not a "feature" position.
- **(b) Red flags:**
  - The frame is a single-subject frame with no implied other.
  - The trace is in a "feature" position (centred, in focus, isolated).
  - The trace is so prominent that it competes with the subject.
- **(c) Test prompts:**
  1. "Subject at a table, a second coffee cup across from her, both cups half-drunk"
  2. "Subject on a couch, an empty seat next to her with a cushion still dented, a phone on the cushion showing a chat"
  3. NEGATIVE: "Solo subject, no second-person trace" — must FAIL R014-07.

### R014-08 — One incomplete pattern per frame

- **(a) Compliance evidence:**
  - Exactly one visual or narrative element in the frame is *implied* but not *fully shown*.
  - Examples: a hand entering the frame from off-screen, a face in a photo on the wall (cropped), a piece of text that is partially visible, a sound implied (the subject is listening to something), an action implied (the subject was just doing something else).
  - The incompleteness is in a *natural* state, not a "deliberately incomplete" state.
- **(b) Red flags:**
  - 0 incomplete patterns = the frame is fully resolved, the viewer has no question to hold.
  - 2+ incomplete patterns = over-fragmented, the viewer is confused.
  - The incompleteness is in a "feature" position (centred, in focus) = deliberately staged.
- **(c) Test prompts:**
  1. "Subject with a hand entering the frame from off-screen, holding something, the hand is the only off-frame element"
  2. "Subject with a face in a photo on the wall behind her, the face partially cropped"
  3. NEGATIVE: "Subject with a fully-resolved frame, nothing implied" — must FAIL R014-08.

### R014-09 — One returning detail per frame

- **(a) Compliance evidence:**
  - At least one detail in the frame is discoverable on the second look but not the first.
  - Examples: a small text on a notebook, a reflection in a mirror, a face in a photo on the wall, a piece of jewelry partially hidden, a number or word on a tag, a specific pattern in the wallpaper.
  - The detail is small enough to miss on the first look but visible on a careful re-examination.
- **(b) Red flags:**
  - 0 returning details = the frame is fully parsed on the first look.
  - 2+ returning details = the frame is "easter-egg heavy", looks cluttered.
  - The detail is so prominent it is visible on the first look = not a returning detail.
- **(c) Test prompts:**
  1. "Subject with a small text on her notebook in the background, visible on a second look but missed on the first"
  2. "Subject with a reflection in a mirror showing a slightly different angle, only visible on careful examination"
  3. NEGATIVE: "Subject with a frame that is fully visible on the first look, no hidden detail" — must FAIL R014-09.

### R014-10 — No face-occluding props

- **(a) Compliance evidence:**
  - Nothing crosses the face plane.
  - Hair, hands, props, and other elements are placed *around* the face, not over it.
  - Stray hair that crosses the face is in a *natural* state (one or two strands, not a curtain).
- **(b) Red flags:**
  - A hand crosses the face (e.g., a hand over the mouth, a hand brushing hair across the face).
  - Hair is positioned in front of the face.
  - A prop (a glass, a pen, a flower) is held in front of the face.
- **(c) Test prompts:**
  1. "Subject with one or two strands of hair across her cheek, the rest of the hair behind her ears"
  2. "Subject holding a prop below the chin, the prop does not cross the face plane"
  3. NEGATIVE: "Subject holding a flower in front of her face" — must FAIL R014-10.

### R014-11 — No symmetric eye state

- **(a) Compliance evidence:**
  - Lid ratio is not identical between left and right eyes (difference of at least 3–5%).
  - Catchlight position is not identical between left and right eyes (the head is slightly turned, so the catchlights fall on different parts of the irises).
  - Scleral show is asymmetric.
  - Brow is asymmetric (one slightly higher, or one shaped differently).
- **(b) Red flags:**
  - Both eyes identical in lid, catchlight, gaze, scleral show = the AI tell.
  - Asymmetry is so pronounced it looks like a medical condition (one eye drooping) = wrong mode.
- **(c) Test prompts:**
  1. "Subject with one eye's lid 5% lower than the other, catchlights in different positions, head slightly turned"
  2. "Subject with one eyebrow slightly raised, the other neutral, gaze held"
  3. NEGATIVE: "Subject with perfectly symmetric eyes" — must FAIL R014-11.

### R014-12 — Catchlight consistency

- **(a) Compliance evidence:**
  - The catchlight position is consistent with the implied key light direction.
  - If the framing is phone-camera (env-lit), the catchlight is from an env source (window, lamp, screen).
  - If the framing is DSLR (controlled), the catchlight is from a studio source.
  - The catchlight is on the same side as the implied key light (face shadow is on the opposite side from the catchlight).
- **(b) Red flags:**
  - Catchlight on the wrong side of the iris (impossible light direction).
  - Catchlight from a studio source in a candid framing = "fake candid".
  - Catchlight from an env source in a controlled framing = "fake natural".
  - No catchlight in either eye = dead eye reading.
- **(c) Test prompts:**
  1. "Subject with window light from the left, catchlight on the upper-left of the iris, face shadow on the right"
  2. "Subject with a ring light, catchlight in the upper-centre of the iris, even face shadow"
  3. NEGATIVE: "Subject with a window on the left but catchlight on the right" — must FAIL R014-12.

---

## 2. Forbidden pattern verification

### FP-01 — Single-fixation frame

**Pattern:** No peripheral anchors, gaze path ends at the face. The viewer glances, registers the face, scrolls.

**Detection:** Visual. The frame is "fully parsed" in one fixation. Reject.

**Reject.**

### FP-02 — Single-plane composition

**Pattern:** Everything at the same depth, no foreground or background layer.

**Detection:** Visual. The frame has no layers. Reject.

**Reject.**

### FP-03 — Face competing with body

**Pattern:** Body as detailed as the face, eye is confused about where to land.

**Detection:** Visual. The face does not dominate. Reject.

**Reject.**

### FP-04 — Face in shadow

**Pattern:** Face darker than surroundings, eye lands elsewhere.

**Detection:** Visual. The face is not the brightest. Reject.

**Reject.**

### FP-05 — Closed-lip performed smile

**Pattern:** Model smile, no orbicularis engagement, mouth is informative-free.

**Detection:** Visual. The mouth is in a "stock" state. Reject.

**Reject.**

### FP-06 — Big toothy smile, no eye change

**Pattern:** Performed smile at maximum amplitude, no orbicularis engagement, social engagement drops.

**Detection:** Visual. The mouth is in a "Duchenne-without-eyes" state. Reject.

**Reject.**

### FP-07 — Static direct gaze, no away-look residue

**Pattern:** Performed stare, not flirty look.

**Detection:** Visual. The gaze has been on the camera the whole time. Reject.

**Reject.**

### FP-08 — Pure smirk

**Pattern:** Both corners up, closed lip, smug not naughty-cute.

**Detection:** Visual. Reject.

**Reject.**

### FP-09 — Fully-revealed tease

**Pattern:** Nothing withheld, no anticipatory tension.

**Detection:** Visual. The frame is fully-revealed. Reject.

**Reject.**

### FP-10 — No second-person trace

**Pattern:** Frame is a single-subject frame, no implied other.

**Detection:** Visual. The viewer is alone. Reject.

**Reject.**

### FP-11 — No personal details

**Pattern:** No specific brand, no specific name, no specific place. Generic model.

**Detection:** Visual. Reject.

**Reject.**

### FP-12 — No incomplete pattern

**Pattern:** Frame is fully resolved, no question for the viewer to hold.

**Detection:** Visual. The frame has nothing implied. Reject.

**Reject.**

### FP-13 — No returning detail

**Pattern:** All details visible on first look, no echo.

**Detection:** Visual. Reject.

**Reject.**

### FP-14 — Bilateral eye symmetry

**Pattern:** Both eyes identical in lid, catchlight, gaze — AI tell.

**Detection:** Visual. Reject.

**Reject.**

### FP-15 — Catchlight contradiction

**Pattern:** Catchlight from a different angle than the implied light source.

**Detection:** Visual. Trace the light, verify the catchlight. Reject on mismatch.

**Reject.**

### FP-16 — Face occluded

**Pattern:** Hand, hair, or prop crosses the face plane.

**Detection:** Visual. Reject.

**Reject.**

### FP-17 — Mid-blink frame

**Pattern:** Eye half-closed, frame reads as "between moments".

**Detection:** Visual. The eye is in transit. Reject.

**Reject.**

---

## 3. Test prompt library

The following 30 prompts are the *baseline test set* for R014. Each prompt is run through the production pipeline with a gaze-itinerary output, and the result is checked.

```
P014-01  "Subject in mitsumeru-me, soft gaze at camera, no smile, slight head tilt, 3-plane composition"
P014-02  "Subject with a coffee cup in foreground, face sharp mid-ground, window soft background"
P014-03  "Subject with hand on her own shoulder, face sharp, bookshelf soft, second-person trace"
P014-04  "Subject with a suppressed smile, mouth open 5mm, eyes crinkled, return-from-away gaze"
P014-05  "Subject with a decay smile, peak over, eyes still on, second coffee cup on the table"
P014-06  "Subject with a specific watch, a Moleskine notebook, a Lamy pen, all visible"
P014-07  "Subject at a table, second cup across, both half-drunk, suppressed smile, gaze held"
P014-08  "Subject on a couch, empty seat next to her with a dented cushion, a phone showing a chat"
P014-09  "Subject with a hand entering the frame from off-screen, holding a small object"
P014-10  "Subject with a face in a photo on the wall behind her, partially cropped"
P014-11  "Subject with a small text on her notebook in the background, visible on second look"
P014-12  "Subject with a reflection in a mirror showing a slightly different angle"
P014-13  "Subject with one or two strands of hair across her cheek, the rest behind her ears"
P014-14  "Subject holding a prop below the chin, the prop does not cross the face plane"
P014-15  "Subject with one eye's lid 5% lower than the other, catchlights in different positions"
P014-16  "Subject with one eyebrow slightly raised, the other neutral, gaze held"
P014-17  "Window light from the left, catchlight upper-left of the iris, face shadow on the right"
P014-18  "Ring light, catchlight upper-centre of the iris, even face shadow"
P014-19  "Subject with a flirty look, half-lidded, slight smile, head tilt, gaze at camera"
P014-20  "Subject in naughty-cute mode, suppressed smile, one eyebrow raised, gaze held"
P019-21  "Subject with the 'shared joke' expression, eyes crinkled, mouth asymmetric"
P014-22  "Subject with a 'you caught me' beat, mid-action, eyes recovered to camera"
P014-23  "Subject with strategic occlusion: a finger over the lip, the rest of the face in view"
P014-24  "Subject with the 'off-frame hand' tease, hand at the edge of the frame, holding something"
P014-25  "Subject with the 'almost-turn' tease, body mid-turn, the next moment will be fuller"
P014-26  "Subject with the 'half-laugh' tease, mouth opening into a smile, not yet complete"
P014-27  "Subject with Xiaohongshu signature: loose hair, light makeup, real-env light, specific personal details"
P014-28  "Subject with the 'office-worker' beat: professional but slightly-loosened attire, real-looking desk"
P014-29  "Subject with the 'early-morning' beat: home in the early morning, hair not done, low-effort activity"
P014-30  "Frame satisfying all 12 R014 rules (the canonical test frame)"
```

---

## 4. Gaze-itinerary output verification

In addition to the image-only checks, the engine's *output contract* (the JSON gaze-itinerary schema in ENGINE_V20_VIEWER_GAZE_SYSTEM.md) must be emitted and verified.

For each rendered frame, the emitted JSON must:
- Specify `primary_anchor` and `secondary_anchor`.
- Specify `gaze_vector` with `direction`, `return_from_away`, and `hold_intensity`.
- Specify `eye_state` with `mode`, `lid_ratio`, `brow_state`, `periorbital_engagement`, and `catchlight_position`.
- Specify `mouth_state` with `type` and `asymmetry`.
- Specify `micro_expression` from the allowed enum.
- Specify all five `face_first_hierarchy` booleans.
- Specify all three `attention_anchors` (foreground, midground, background).
- Specify at least 2 and at most 3 `personal_details`.
- Specify at least 1 `second_person_trace`.
- Specify at least 1 `incomplete_pattern`.
- Specify at least 1 `returning_detail_echo`.
- Specify `retention_estimate.three_second_hold` between 0 and 1.
- Specify `retention_estimate.return_fixation_probability` between 0 and 1.

Any field that is missing, null, or out-of-range is a verification failure for the gaze-itinerary output.

---

## 5. Pass/fail threshold

**Per rule:** ≥ 80% of test prompts must pass.

**For the R014 module as a whole:** ≥ 80% of test prompts must pass the *full* R014 checklist (all 12 rules + all 17 forbidden patterns + the gaze-itinerary output).

**For the unblock decision:** the engine is run in production for 30 days on real prompts, and the production output is rated by a panel of 3 raters (blind to the engine rules) on:
- 1–5 scale for "3-second hold" (does the image hold past 3 seconds?)
- 1–5 scale for "re-look rate" (does the viewer's eye return?)
- 1–5 scale for "parasocial connection" (does the viewer feel the subject is real?)

Average rating ≥ 4.0 across all raters, all frames, and all three metrics is the unblock threshold.

---

## 6. R014 unblock checklist (for the production team)

- [ ] All 30 test prompts run through the production pipeline.
- [ ] Each prompt emits a gaze-itinerary JSON.
- [ ] Each output image checked against R014-01…R014-12.
- [ ] Each output image checked against FP-01…FP-17.
- [ ] Each gaze-itinerary checked against the output contract.
- [ ] Pass rate ≥ 80% per rule, ≥ 80% overall.
- [ ] 30-day production run completed.
- [ ] 3-rater blind panel scoring ≥ 4.0 average on hold + re-look + parasocial.
- [ ] Canon status updated to "UNBLOCKED" in the engine file.

---

**End R014 verification file.** Companion: R014_VIEWER_GAZE_ENGINE.md (research), ENGINE_V20_VIEWER_GAZE_SYSTEM.md (engine spec).
