# R013 — Object Motivation Engine
## Self-Verification Protocol

**Canon status:** BLOCKED until production testing
**File pair:** R013_OBJECT_MOTIVATION_ENGINE.md (research), ENGINE_V20_OBJECT_MOTIVATION_SYSTEM.md (engine spec)
**Scope:** Per-rule compliance evidence, red-flag set, and test prompts. This file defines how to confirm a generated image actually satisfies the R013-01…R013-15 rules in the research file, before the rule is unblocked.

---

## 0. How to use this file

For every rule in §13 of the research file, this file defines:
- **(a) Evidence of compliance** — what the final image MUST show.
- **(b) Red flags of failure** — what would tell you the rule is not met.
- **(c) Test prompts** — concrete prompts to run through the production pipeline to check compliance.

Canon status for the whole R013 module is **BLOCKED** until the production team runs at least **30 test prompts per rule** and the verification checklist passes at ≥ 80% of prompts. Until that test set is run, R013 is a research document, not a production rule.

The five mandated attributes (Owner, Purpose, Last Interaction, Current Resting State, Visibility Reason) are tested per visible object. The verification protocol requires the prompt-generation system to emit an *object list* (the audit list) alongside the image, so that the rules can be checked against the actual object definitions rather than inferred from the image alone.

---

## 1. Verification checklist — the five mandated attributes

### OBJ-ATTR-01 — Owner is assigned to every visible object

- **(a) Compliance evidence:**
  - The object list (emitted by the prompt generator) names an owner for every visible object.
  - The owner is a *specific* person (her, the partner, the roommate, a child, a pet), not a category ("a person") or a default ("the subject").
  - Objects that have no specific owner (e.g., a building seen through a window) are *not* in the visible-object list; they are background and not subject to the mandate.
- **(b) Red flags:**
  - An object with no owner assignment.
  - An object with "the subject" as the owner when the subject is *implied* not present (e.g., the subject is in the kitchen, the bedroom is in the background).
  - An object with "anonymous" or "none" as the owner.
- **(c) Test prompts:**
  1. "Object list: coffee cup, owner: her; notebook, owner: her; pen, owner: her; second coffee cup, owner: partner"
  2. "Object list: towel, owner: her; toothbrush, owner: her; razor, owner: her; second toothbrush, owner: partner"
  3. NEGATIVE: object with no owner assignment — must FAIL.

### OBJ-ATTR-02 — Purpose is assigned to every visible object

- **(a) Compliance evidence:**
  - Each object has a stated purpose (drinking, writing, drying, sleeping, etc.).
  - The purpose is *plausible* for the object type and the scene.
- **(b) Red flags:**
  - An object with no purpose.
  - A purpose that is implausible (a candle "for reading", a pillow "for storing keys").
- **(c) Test prompts:**
  1. "Object list: coffee cup, purpose: drinking morning coffee"
  2. "Object list: notebook, purpose: journaling"
  3. NEGATIVE: an object with "decoration" as its only purpose and no functional role in the scene — must FAIL (unless the scene is explicitly a styled interior, which is outside R013's scope).

### OBJ-ATTR-03 — Last Interaction is assigned to every visible object

- **(a) Compliance evidence:**
  - Each object has a "last used" timestamp (e.g., 5 minutes ago, 1 hour ago, yesterday).
  - The timestamp is *plausible* for the time-of-day implied by the lighting and the object's purpose (a half-drunk morning coffee at noon is implausible; a half-drunk morning coffee at 9am is plausible).
  - The state of the object is *consistent* with the last interaction (a warm cup was used 5 minutes ago; a cold cup was used 1 hour ago).
- **(b) Red flags:**
  - An object with no last-interaction timestamp.
  - A timestamp that contradicts the lighting (evening lamp with a "morning coffee" timestamp).
  - A state that contradicts the timestamp (a "5 minutes ago" coffee that is cold).
- **(c) Test prompts:**
  1. "Object list: coffee cup, last interaction: 5 minutes ago, current state: warm, half-full"
  2. "Object list: book, last interaction: 2 hours ago, current state: open to page 84, face-down on couch"
  3. NEGATIVE: an object with a timestamp that contradicts the lighting or the state — must FAIL.

### OBJ-ATTR-04 — Current Resting State is assigned to every visible object

- **(a) Compliance evidence:**
  - Each object has a *state description* (wet, dry, open, closed, full, empty, on, off, warm, cold, etc.).
  - The state is the *result* of the last interaction, not a "default" or "stock" state.
  - The state is *consistent* with the object's purpose and the last interaction.
- **(b) Red flags:**
  - An object with a generic state (just "there") and no specifics.
  - A state that contradicts the last interaction (a "used 5 minutes ago" towel that is dry and folded).
  - A state that is impossible (a book that is both face-down and open to a specific page).
- **(c) Test prompts:**
  1. "Object list: pen, current state: uncapped, mid-table, ink still wet at the tip"
  2. "Object list: towel, current state: damp, crumpled on the bathroom floor, not on the rack"
  3. NEGATIVE: an object with a "stock" state that is the same as a product-listing photo — must FAIL.

### OBJ-ATTR-05 — Visibility Reason is assigned to every visible object

- **(a) Compliance evidence:**
  - Each object has a stated reason for being visible from the camera angle (e.g., "on the foreground table", "at eye level in the background", "in the path of the subject's hand").
  - The reason is *spatial* (about position) or *narrative* (about the subject's action), not "because it looks nice".
- **(b) Red flags:**
  - An object with no visibility reason.
  - A reason that is "because it is photogenic" or "to fill the frame".
  - A reason that contradicts the camera angle (an object claimed to be in the foreground that is actually in the deep background).
- **(c) Test prompts:**
  1. "Object list: coffee cup, visibility: on the bedside table, in the foreground depth, near the subject's hand"
  2. "Object list: laptop, visibility: open on the desk, in the mid-ground depth, screen facing the subject"
  3. NEGATIVE: an object with "to add visual interest" as the visibility reason — must FAIL.

---

## 2. Verification checklist — per rule

### R013-01 — Object list audit

- **(a) Compliance evidence:** Every visible object in the final image has all five attributes assigned in the prompt-generator's object list.
- **(b) Red flags:** Any visible object missing one or more attributes.
- **(c) Test prompts:**
  1. Render the same scene with and without the object list. Without-list should fail or produce a generic scene; with-list should produce a specific scene.
  2. Manually count visible objects in the rendered image and verify each appears in the object list with all five attributes.

### R013-02 — Last-interaction timestamp

- **(a) Compliance evidence:** Each object's timestamp is plausible for the lighting and the state.
- **(b) Red flags:** Timestamp-state mismatch, timestamp-lighting mismatch.
- **(c) Test prompts:**
  1. "Morning scene, 9am lighting, half-drunk coffee = plausible"
  2. "Evening scene, 8pm lamp, full ashtray with a still-warm cigarette = plausible"
  3. NEGATIVE: "Morning scene, half-drunk red wine = implausible" — must FAIL.

### R013-03 — Default closed

- **(a) Compliance evidence:** Drawers, cabinets, wardrobes, bags, boxes, and other storage are closed by default. Open storage implies an in-progress activity stated in the prompt.
- **(b) Red flags:** An open cabinet with no in-progress activity specified. An open wardrobe showing a curated interior. A "peek into the bag" beat with the contents arranged.
- **(c) Test prompts:**
  1. "Closed kitchen cabinets, one open drawer that the subject is actively looking through"
  2. "Closed wardrobe, a single outfit on the bed that the subject is mid-deciding"
  3. NEGATIVE: "Open cabinet revealing a perfectly arranged interior" — must FAIL.

### R013-04 — Active cluster mandate

- **(a) Compliance evidence:** Exactly one *cluster* of objects in the frame is in the "active" (in-progress) state. The rest of the frame is at baseline.
- **(b) Red flags:** Multiple active clusters. No active cluster (every surface at baseline). Uniform clutter (every surface equally in-progress).
- **(c) Test prompts:**
  1. "Desk with active cluster (notebook, pen, coffee cup, phone), rest of the room at baseline (bed made, closet closed, floor clear)"
  2. "Kitchen counter with active cluster (cutting board, knife, half-chopped vegetables), rest of the kitchen clean"
  3. NEGATIVE: "Every surface in the room equally cluttered" — must FAIL.

### R013-05 — Use-signature props

- **(a) Compliance evidence:** Every visible prop has a use-signature (the state that results from the last person who used it). The prop is not in a "feature" or "mood" position.
- **(b) Red flags:** A prop that is centred, in focus, against a clean background. A "mood prop pile" (candle + flower + journal in soft light). A prop that is in its "stock" state (a book with the dust jacket pristine, a candle never lit).
- **(c) Test prompts:**
  1. "Notebook open to a half-written page, pen uncapped, in the periphery of the frame"
  2. "Book face-down on the couch, a thumb in the page, in the periphery"
  3. NEGATIVE: "Single candle, centred, in focus, against a clean background" — must FAIL.

### R013-06 — Owner signature

- **(a) Compliance evidence:** All objects owned by the same person share a consistent signature (dominant hand, sleep side, morning routine). The signature is consistent across the frame.
- **(b) Red flags:** A cup with the handle to the right (right-handed) in one frame and to the left (left-handed) in another for the same character. A pillow on the wrong side of the bed for the character's sleep side.
- **(c) Test prompts:**
  1. "Right-handed character: coffee cup handle to the right, pen in the right hand, phone on the right side of the desk"
  2. "Sleep-on-left character: pillow on the left, book on the left nightstand, glass of water on the left"
  3. NEGATIVE: "Same character, handle to the right in one frame and the left in another" — must FAIL.

### R013-07 — Path of motion

- **(a) Compliance evidence:** Objects in motion are mid-motion. Objects at rest are at rest. No object is in a state that contradicts its motion path (a hand reaching for a cup with the cup already in the hand).
- **(b) Red flags:** An object claimed to be "in motion" but in a still state. An object claimed to be "at rest" but in an in-progress state.
- **(c) Test prompts:**
  1. "Subject mid-reaching for a cup, the cup is on the table, the hand is between the subject and the cup"
  2. "Subject mid-placing a book on a shelf, the book is in the hand, the shelf has space for it"
  3. NEGATIVE: "Subject's hand already on the cup with the cup still claimed to be 'on the table'" — must FAIL.

### R013-08 — Visibility justification

- **(a) Compliance evidence:** Every visible object has a stated visibility reason. The reason is not "because it looks nice".
- **(b) Red flags:** Objects with no visibility reason, or with "to fill the frame" as the reason.
- **(c) Test prompts:**
  1. "Object list with a visibility column populated for every object"
  2. NEGATIVE: an object list with "to add visual interest" in the visibility column — must FAIL.

### R013-09 — Time-of-day coherence

- **(a) Compliance evidence:** All objects, residue, and lighting are consistent with the same time of day.
- **(b) Red flags:** Morning light with evening residue. Evening lamp with morning objects. A scene with no consistent time signature.
- **(c) Test prompts:**
  1. "Morning: bright window light, unmade bed, half-drunk coffee, unopened mail, light breakfast residue"
  2. "Evening: warm lamp light, partial undress, half-full wine, lit candle, phone face-down on the couch"
  3. "Late night: dark room, single screen glow, one subject, no other lights, sleepwear"
  4. NEGATIVE: "Morning light with a full ashtray and an evening lamp" — must FAIL.

### R013-10 — Casual entropy default

- **(a) Compliance evidence:** The default entropy is "no event in 24+ hours". The small drifts are from normal use, not from any specific event.
- **(b) Red flags:** The room looks post-party, post-argument, or post-move without the event being specified. The "deliberately messy" look.
- **(c) Test prompts:**
  1. "Default bedroom: bed slightly unmade from the morning, two pillows with their normal dent, phone on the nightstand, book on the duvet"
  2. "Default kitchen: one dish in the sink, one cup on the counter, a half-read newspaper on the table"
  3. NEGATIVE: "Room with confetti, empty bottles, multiple glasses" — must FAIL (unless the prompt specifies a party, which is out of R013's default scope).

### R013-11 — No real-estate angles

- **(a) Compliance evidence:** No open-cabinet reveals, no open-wardrobe reveals, no "peek into the bag" beats, no "show the curated interior" frames.
- **(b) Red flags:** An open cabinet shot with a clean, well-lit interior. A wardrobe open to a colour-coded clothing rail. A bag opened to display the contents.
- **(c) Test prompts:**
  1. "Cabinet closed, the subject reaching for the handle"
  2. "Wardrobe closed, the subject's outfit on the bed"
  3. NEGATIVE: "Cabinet open, contents perfectly arranged and lit" — must FAIL.

### R013-12 — No catalogue composition

- **(a) Compliance evidence:** The objects in the frame include at least one *slightly worn* or *imperfect* object. The "best of" only composition is avoided.
- **(b) Red flags:** Every object pristine, every product at its catalogue best, no wear, no personal damage.
- **(c) Test prompts:**
  1. "Coffee cup with a chip on the rim, otherwise normal"
  2. "Book with a folded corner, a pen with a chewed cap, a notebook with a water-stain"
  3. NEGATIVE: "Every object pristine, all products at their best" — must FAIL.

### R013-13 — No bilaterally symmetric arrangement

- **(a) Compliance evidence:** No two-of-each symmetric arrangement. The placement reflects use, not composition.
- **(b) Red flags:** Two candles flanking a centred object. Two pillows symmetrically placed. A symmetric "tablescape".
- **(c) Test prompts:**
  1. "Three candles on a mantel, all at different heights, none symmetrically placed"
  2. "Coffee table with one book, one cup, one remote, no symmetry"
  3. NEGATIVE: "Two identical candles on either side of a centred vase" — must FAIL.

### R013-14 — Hotel-room guest traces / bathroom post-shower state

- **(a) Compliance evidence (hotel-room):** At least one guest trace per room (a half-unmade bed, a single item of clothing, an open suitcase, the TV on).
- **(a) Compliance evidence (bathroom):** At least one post-shower state marker (a damp towel, an open product, a mirror with a slight steam residue, a toothbrush at a used angle).
- **(b) Red flags:** A hotel room that looks like a stock listing. A bathroom that looks like a beauty counter.
- **(c) Test prompts:**
  1. "Hotel room, night 2: bed unmade, single shoe by the bed, TV on, curtains half-drawn, glass of water half-empty on the nightstand"
  2. "Bathroom, post-shower: damp towel on the floor (not on the rack), open toothpaste, toothbrush at a used angle, mirror slightly fogged, a hair tie on the sink"
  3. NEGATIVE: "Hotel room: bed made, lamps symmetric, no personal items" — must FAIL.

### R013-15 — Shopping bag lean rule

- **(a) Compliance evidence:** Shopping bags lean against objects, sit on floors, are held, or are stacked. They do not stand free in the centre of the frame.
- **(b) Red flags:** A shopping bag standing free in the centre of a frame, fully visible, contents peeking out.
- **(c) Test prompts:**
  1. "Shopping bag leaning against the kitchen counter, partially open, receipt visible on the floor next to it"
  2. "Two shopping bags on the floor by the door, leaning against each other, not standing"
  3. NEGATIVE: "Shopping bag standing free in the centre of a clean table" — must FAIL.

---

## 3. Forbidden pattern verification

### FP-01 — Feature-object syndrome

**Pattern:** One of each category, well-composed, filling the frame. The "tablescape" look.

**Detection:** Visual. If the frame is a "still life" with one of each type, the engine has fallen into feature-object mode.

**Reject.**

### FP-02 — Real-estate open storage

**Pattern:** Open cabinet, open wardrobe, open drawer, showing a curated interior.

**Detection:** Visual. If storage is open and the interior is curated, reject.

**Reject.**

### FP-03 — Catalogue composition

**Pattern:** All objects at their "best", no wear, no personal damage.

**Detection:** Visual. The frame looks like a product catalogue. Reject.

**Reject.**

### FP-04 — Bilateral symmetry

**Pattern:** Two of each, equally weighted, centred.

**Detection:** Visual. Mirror-symmetric arrangement = reject.

**Reject.**

### FP-05 — Mood-prop pile-up

**Pattern:** Candle + flower + journal + soft light = the "wellness aesthetic".

**Detection:** Pattern match. Reject.

**Reject.**

### FP-06 — Time-of-day incoherence

**Pattern:** Lighting and objects from different times of day.

**Detection:** Visual. Compare the lighting to the residue. Reject on mismatch.

**Reject.**

### FP-07 — Uniform clutter

**Pattern:** Every surface equally cluttered.

**Detection:** Visual. The room has no "active cluster". Reject.

**Reject.**

### FP-08 — Empty personal space

**Pattern:** No photos, no magnets, no personal items in a private space.

**Detection:** Visual. The space is "model home", not "lived in". Reject.

**Reject.**

### FP-09 — Upright shopping bag

**Pattern:** Shopping bag standing free in the centre of a frame.

**Detection:** Visual. The bag is the subject, not the user. Reject.

**Reject.**

### FP-10 — Hanger-ready clothes

**Pattern:** Wardrobe or fitting room with clothes on hangers, perfectly arranged, fully visible.

**Detection:** Visual. The "ootd wardrobe" or "curated fitting room". Reject.

**Reject.**

### FP-11 — Stock fitting room

**Pattern:** Empty fitting room, single hook, no try-on residue.

**Detection:** Visual. Reject.

**Reject.**

### FP-12 — OOTD fitting room

**Pattern:** Full outfit, mirror angled for camera, no "no" pile on the floor.

**Detection:** Visual. Reject.

**Reject.**

### FP-13 — Hotel-room stock

**Pattern:** Made bed, symmetric lamps, no guest traces, curtains drawn.

**Detection:** Visual. Reject.

**Reject.**

### FP-14 — Beauty counter bathroom

**Pattern:** All products visible, mirror clean, towel folded, no used state.

**Detection:** Visual. Reject.

**Reject.**

### FP-15 — Event entropy without event

**Pattern:** Room looks post-party, post-argument, post-move with no event specified.

**Detection:** Visual. Reject.

**Reject.**

---

## 4. Test prompt library

The following 30 prompts are the *baseline test set* for R013. Each prompt is run through the production pipeline with an emitted object list, and the result is checked.

```
P013-01  "Kitchen scene, morning, half-drunk coffee, toast crumbs, open newspaper on the table, one dirty plate in the sink"
P013-02  "Bedroom scene, evening, bed slightly unmade from the morning, phone on the nightstand, half-read book on the duvet, lamp on"
P013-03  "Bathroom scene, post-shower, damp towel on the floor, open toothpaste, toothbrush at a used angle, hair tie on the sink"
P013-04  "Hotel room, night 2, bed unmade, single shoe by the bed, TV on, curtains half-drawn"
P013-05  "Fitting room, mid-decision, half-undressed, 'no' pile on the floor, 'maybe' item with tag still on"
P013-06  "Two shopping bags on the floor by the door, leaning against each other, receipts visible"
P013-07  "Subject at a desk, notebook open, pen uncapped, coffee cup, phone face-up, lamp on"
P013-08  "Subject in a study, two coffee cups, half-written note, chair recently sat in"
P013-09  "Default kitchen: one dish in the sink, one cup on the counter, half-read newspaper on the table"
P013-10  "Default bedroom: bed slightly unmade, two pillows with their normal dent, phone on the nightstand"
P013-11  "Subject in a kitchen, cutting board, knife, half-chopped vegetables, rest of kitchen clean"
P013-12  "Three candles on a mantel, all at different heights, no symmetry"
P013-13  "Coffee table with one book, one cup, one remote, no symmetry"
P013-14  "Cabinet closed, the subject reaching for the handle"
P013-15  "Wardrobe closed, the subject's outfit on the bed"
P013-16  "Coffee cup with a chip on the rim, otherwise normal"
P013-17  "Book with a folded corner, pen with a chewed cap, notebook with a water-stain"
P013-18  "Subject mid-reaching for a cup, the cup on the table, the hand between the subject and the cup"
P013-19  "Subject mid-placing a book on a shelf, the book in the hand, the shelf has space"
P013-20  "Morning scene: bright window light, unmade bed, half-drunk coffee, unopened mail"
P013-21  "Evening scene: warm lamp light, partial undress, half-full wine, lit candle, phone face-down"
P013-22  "Late night scene: dark room, single screen glow, one subject, sleepwear"
P013-23  "Default bedroom with active cluster on the nightstand (phone, book, glass of water), bed at baseline"
P013-24  "Default kitchen with active cluster on the counter (cutting board, vegetables, knife), rest at baseline"
P013-25  "Right-handed character: coffee cup handle to the right, pen in right hand, phone on right of desk"
P013-26  "Sleep-on-left character: pillow on the left, book on the left nightstand, glass on the left"
P013-27  "Subject in a fitting room, the viewer caught her, 'no' pile on the floor"
P013-28  "Subject with a notebook open to a half-written page, pen uncapped, in the periphery of the frame"
P013-29  "Subject with a book face-down on the couch, a thumb in the page, in the periphery"
P013-30  "Scene with all 15 R013 rules satisfied (the canonical test frame)"
```

---

## 5. Pass/fail threshold

**Per rule:** ≥ 80% of test prompts must pass.

**For the R013 module as a whole:** ≥ 80% of test prompts must pass the *full* R013 checklist (all 15 rules + all 5 attributes + all 15 forbidden patterns).

**For the unblock decision:** the engine is run in production for 30 days on real prompts, and the production output is rated by a panel of 3 raters (blind to the engine rules) on a 1–5 scale for "realism" and "object believability". Average rating ≥ 4.0 across all raters and all frames is the unblock threshold.

---

## 6. R013 unblock checklist (for the production team)

- [ ] All 30 test prompts run through the production pipeline.
- [ ] Each prompt emits an object list with all five attributes per object.
- [ ] Each output image checked against R013-01…R013-15.
- [ ] Each output image checked against FP-01…FP-15.
- [ ] Pass rate ≥ 80% per rule, ≥ 80% overall.
- [ ] 30-day production run completed.
- [ ] 3-rater blind panel scoring ≥ 4.0 average.
- [ ] Canon status updated to "UNBLOCKED" in the engine file.

---

**End R013 verification file.** Companion: R013_OBJECT_MOTIVATION_ENGINE.md (research), ENGINE_V20_OBJECT_MOTIVATION_SYSTEM.md (engine spec).
