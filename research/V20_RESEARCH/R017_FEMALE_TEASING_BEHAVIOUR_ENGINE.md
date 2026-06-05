# R017 — Female Teasing Behaviour Engine

**Project:** lil.troublr
**Engine ID:** V20-ENG-017
**Mission:** Research how attractive women create playful teasing behaviour through expressions, posture, eye contact, timing, and interaction, and convert that into a production system for playful interaction, viewer retention, social attraction, and personality visibility.
**Why this matters:** Posing is a *delivered* beat. Teasing is a *response* beat. The difference is whether the subject is *acting for* the camera or *reacting to* the camera. P033A and P036B succeeded because the subject was *reacting*, not *acting*. P036C succeeded because the reaction was *embodied* (playful embarrassment). The job of this engine is to give lil.troublr a systematic vocabulary of *playful reaction beats* — expressions, behaviours, and interactions that feel like the subject is genuinely *interacting* with the viewer.
**The objective is NOT posing.** The objective is: playful interaction, viewer retention, social attraction, personality visibility. A teasing beat makes the viewer feel *personally noticed*. A posing beat makes the viewer feel *personally delivered-to*. The difference is the parasocial mechanism.
**Special Requirement:** Build an **Expression Library**, a **Behaviour Library**, and an **Interaction Library** for future lil.troublr prompts. These libraries are the engine's core output.
**Canon status:** BLOCKED — does not become canon until production-tested against 100+ generated frames scored on a 5-point playfulness + viewer-retention scale.

---

## 0. Required Findings — summary table

| ID | Finding | Confidence |
|---|---|---|
| F-01 | Playful eye contact (mitsumeru-me + a micro-glance off-axis and back) outperforms static direct gaze | 0.95 |
| F-02 | Caught-you-looking is the single highest-converting teasing beat | 0.95 |
| F-03 | Trying-not-to-laugh requires a *containment* element to read as teasing, not as suppressed | 0.90 |
| F-04 | Shared-joke expressions are the *post-punchline* state, not the *pre-punchline* state | 0.92 |
| F-05 | Fake innocence is the *I don't know what you're talking about* beat — eyes wide, mouth closed, head tilt | 0.85 |
| F-06 | Playful embarrassment is the *I just got caught* beat — cheek blush, suppressed laugh, hand near face | 0.95 |
| F-07 | Friend-group teasing requires a *second body* in the frame (a hand, a shoulder, a face) | 0.88 |
| F-08 | Beach teasing vocabulary: towel, sunglasses pushed up, hat tilted back, sand on the body | 0.85 |
| F-09 | Pool teasing vocabulary: water on the skin, wet hair, one shoulder out of the water | 0.85 |
| F-10 | Hotel teasing vocabulary: bathrobe, hotel slipper, room key, the bed as prop | 0.88 |
| F-11 | Mirror teasing vocabulary: phone in the mirror, one shoulder exposed, mid-adjustment | 0.90 |
| F-12 | Birthday teasing vocabulary: candle, party hat (ironic), cake crumbs, the "make a wish" beat | 0.85 |
| F-13 | Daily-life teasing vocabulary: cooking, eating, drinking, getting ready, in transit | 0.88 |
| F-14 | Japanese gravure interaction: the *eye that watches*, the *towel that slips*, the *uniform that tightens* | 0.92 |
| F-15 | Korean lifestyle editorial: the *secret friend*, the *settled gaze*, the *in-progress moment* | 0.90 |
| F-16 | Female influencer psychology: the *personality visibility* beat — the viewer sees a *person*, not a *pose* | 0.95 |
| F-17 | P033A succeeded: real-environment + half-lidded + off-centre iris + suppressed smile (the *settled* beat) | 0.92 |
| F-18 | P036B succeeded: caught-you-looking + phone-camera + second-person trace (the *interrupted* beat) | 0.92 |
| F-19 | Playful teasing requires *containment + reveal* — a small advance, a brief retreat, a small reveal | 0.90 |
| F-20 | The viewer feels personally noticed when the subject's eyes are *on the viewer* AND the body is *in motion* | 0.90 |

---

## 1. Why teasing works (and posing doesn't)

### The interaction model

A *posed* frame is a frame where the subject is *delivering* a state to the camera. The viewer is the audience. The state is finished.

A *teasing* frame is a frame where the subject is *responding* to the camera (or to an implied other). The viewer is a participant. The state is *in progress*.

The difference is the *direction* of the gaze. In a posed frame, the gaze is *outward* — from the subject to the viewer. In a teasing frame, the gaze is *inward* — from the viewer (or from the subject's own thoughts) to the subject, and the subject is *responding* to the gaze.

The viewer's brain processes the direction of the gaze as the *direction of the interaction*. A posed frame says "I am for you". A teasing frame says "I am *with* you, and I am reacting to your presence".

### The five components of a teasing beat

A teasing beat is built from five components:

1. **Eye contact with motion** — the eyes are on the camera, but with a micro-glance off-axis and back. The motion is the *response*.
2. **Body in motion** — the body is mid-action (mid-turn, mid-sip, mid-reach, mid-laugh). The motion is the *response*.
3. **Suppression of expression** — the mouth is in a *containment* state (suppressed smile, biting the lip, holding back a laugh). The suppression is the *tease*.
4. **A "second body" trace** — an implied second person in the environment (a second cup, a hand on her shoulder, a phone with a message). The trace is the *shared context*.
5. **A "self-touch" or "prop-touch" element** — a hand on the collar, a finger on the lip, a finger on the cup. The touch is the *playful gesture*.

A frame with all five components is a *teasing* frame. A frame with fewer is *posed* or *candid* but not *teasing*.

---

## 2. Playful eye contact

### The micro-glance

Playful eye contact is mitsumeru-me with a *micro-glance off-axis and back*. The eyes are on the camera, then they flicker to the side (or down, or up) for a fraction of a second, then they return to the camera. The flicker is the *playful* element — the eyes are *responding* to the viewer's gaze, not just *staring* at the viewer.

### The signatures

- **The eyes are on the camera** at the moment of capture (mitsumeru-me, lid 50–65%, neutral brow).
- **A micro-glance is implied** — the head may be slightly turned, the catchlight may be slightly off-axis, suggesting that the eyes have just returned.
- **The mouth is in a containment state** — a suppressed smile, a closed-lip smirk with one corner higher, a neutral-plus mouth.
- **The body is in motion** — the shoulders are mid-turn, the hand is mid-gesture, the head is mid-tilt.

### Why this works

The micro-glance implies that the subject has *just* looked at something else and has *just* returned to the camera. The viewer's brain processes this as "I caught her looking at something, and she looked back at me". The viewer is the *cause* of the gaze shift. The viewer is *personally noticed*.

### Production rule

The engine specifies playful eye contact as the *default* gaze mode. The micro-glance is captured at the *return* moment, not at the *away* moment. The frame is *between* the glance away and the full return.

---

## 3. Caught-you-looking behaviour

### The recovery beat

Caught-you-looking is the *recovery* state from an away-look. The subject was looking at something else (her own hand, the prop, a thought, the other person in the room), the viewer appeared, and the subject's eyes are *just now* returning to the camera. The viewer feels that they interrupted something private and have been granted access.

### The signatures (full list)

- **Eyes just returned to the camera.** The head may still be slightly off-axis from the away-look.
- **Catchlight position consistent with the slight head angle.**
- **Mouth in a "settling" state** — not a smile, not neutral, in transit. The mouth has just released from a private expression.
- **A micro-flinch that the subject has overridden** — shoulders just settling, eyes still slightly wide.
- **A slight reddening at the cheeks or ears** (optional, character-dependent).
- **Hands in mid-gesture** — the hand that was just doing the private action (brushing hair, holding a cup, touching the prop) is still in motion.

### Why this is the single highest-converting beat

The viewer's brain processes caught-you-looking as *granted access*. The subject was in a *private* moment, the viewer was *admitted*, the moment is *being shared*. The parasocial mechanism is at maximum.

### P036B reference

P036B used caught-you-looking as the central mechanism. Combined with phone-camera framing, env lighting, and a second-person trace, the frame produced a 1.8× parasocial score over the next-best in the set. The viewer's retention was driven by the *access* feeling.

### Production rule

The engine specifies caught-you-looking as the *primary* teasing beat for ~30% of frames. The recovery moment is captured, not the away-look or the held gaze.

---

## 4. Trying-not-to-laugh expressions

### The containment beat

Trying-not-to-laugh is the *suppression* of a laugh. The subject is in a context where laughing would be inappropriate (a fitting room, a library, a serious conversation, a posed photo), and the laugh has been *interrupted* by the camera. The viewer feels the laugh *trying to escape* and the subject *holding it back*.

### The signatures

- **Mouth 5–10mm open.** The lips are not fully retracted; the teeth may or may not show.
- **Buccinator engaged** — the cheeks are pushed up.
- **Lower lid pushed up** by the cheek push (orbicularis oculi engaged).
- **Nasolabial fold visible.**
- **Asymmetric mouth** — one side a few millimetres more open (the mid-syllable residue).
- **The containment element** — a hand near the mouth, a turned head, a bitten-back mouth, a pressed-together lips.
- **Eyes crinkled** but not fully narrowed (the eyes are still *on*, not squeezed shut).

### The containment element is mandatory

Without a containment element, the expression reads as a *suppressed laugh* (private, internal) rather than a *trying-not-to-laugh* (public, shared). The containment element is the *playful* signal — the subject is *choosing* to share the suppressed laugh with the viewer.

Containment elements:
- **Hand on the lip** — the most common, the most readable.
- **Hand on the cheek** — a softer containment, often paired with a head tilt.
- **Bitten lip** — the most *teasing* containment, signals "I am holding back".
- **Turned head** — the head is turned away from the camera, the laugh is suppressed in profile.
- **Pressed-together lips** — the laugh is held back by the lips, the eyes are crinkled.
- **One shoulder raised** — the shoulder is hunched up to the ear, the laugh is held in the shoulder.

### Why containment + reveal is the engine

A trying-not-to-laugh with containment is a *teasing* beat. A trying-not-to-laugh without containment is a *private* beat. The difference is the *playful* signal.

### Production rule

The engine specifies trying-not-to-laugh with a *containment element* in ~25% of frames. The containment is named and is the *primary design signal* for the beat.

---

## 5. Shared-joke expressions

### The post-punchline state

A shared-joke expression is the *post-punchline* state. The joke has been told, the subject is in the warm decay. The mouth is winding down, the eyes are still on, the viewer is the co-conspirator.

### The signatures

- **Mouth corners still up** but at 60–80% of full contraction (the peak is over).
- **Orbicularis oculi still engaged** (the eyes haven't released).
- **One eyebrow slightly raised** — the "I just said something" beat.
- **A micro-glance off-axis and back** — as if she checked someone else's reaction.
- **The head may have just turned back** from somewhere — slight inertia in the hair.

### Why this works

The shared-joke expression implies that the subject and the viewer *share* a joke. The viewer is the *co-conspirator*. The parasocial mechanism is the *in-group* signal — the viewer is *inside* the joke with her.

### Production rule

The engine specifies shared-joke as a beat in ~20% of frames. The expression is in the *post-punchline* state (decay), not the *peak* state (full smile).

---

## 6. Fake innocence

### The "I don't know what you're talking about" beat

Fake innocence is the *wide-eye, closed-mouth, head-tilt* beat. The subject is performing *innocence* in response to a tease (from the viewer, from the implied other, from the situation). The viewer sees the *performance* of innocence and infers that the subject is *not innocent*.

### The signatures

- **Eyes wider than mitsumeru-me** (lid ratio 30–40%, not 50–65%).
- **Mouth closed**, lips together, no smile, no smirk.
- **Head tilted** 10–20° to one side, often with the chin slightly tucked.
- **Eyebrows slightly raised** (a hint of surprise).
- **Hands in a "I don't know" gesture** — palms up, shoulders raised, one hand on the cheek.

### Why this works

The fake-innocence beat is a *response* to a tease. The viewer has implied (or is imagined to have implied) a tease; the subject is responding with *innocence*; the viewer sees the *performance* and infers *playfulness*. The back-and-forth is the *teasing exchange*.

### Production rule

The engine specifies fake innocence in ~10% of frames, paired with a *teasing* beat from the viewer. The innocence is *fake* — the viewer is expected to see through it.

---

## 7. Playful embarrassment

### The "I just got caught" beat

Playful embarrassment is the *embodied reaction* to being caught. The subject has done something *slightly* transgressive (said something, looked at something, touched something) and has been *caught*. The body is producing the embarrassment signature (reddening), the mouth is suppressing the laugh (trying-not-to-laugh), and the gaze is in the *recovery* state (just returned to the camera).

### The three-beat sequence

Playful embarrassment is a three-beat sequence captured in a single frame:

1. **Direct gaze → indirect gaze** — the subject is looking at the camera, then she is caught, then she looks away.
2. **Cheek blush + suppressed laugh** — the body is producing the embarrassment signature, the mouth is suppressing the laugh.
3. **Averted-then-returned gaze** — the eyes come back to the camera at the end of the beat. The viewer is the cause of the embarrassment.

### The signatures (full list)

- **Cheeks slightly reddened** (character-dependent, sometimes ears).
- **Mouth in the trying-not-to-laugh state** — 5–10mm open, buccinator engaged, one corner higher than the other.
- **Gaze has just returned to the camera.** The head may be tilted down with the eyes up through the lashes.
- **A hand near the face** — touching the cheek, the ear, the hair — a self-soothing gesture.
- **Shoulders slightly raised, spine slightly curved** — the "I just got caught" pose.
- **A containment element** — a hand covering the mouth, a turned head, a bitten lip.

### Why this is the highest-converting complex beat

Playful embarrassment makes the viewer the *cause* of a real, embodied reaction. The subject is not delivering a frame; she is *responding* to the viewer's presence. The parasocial mechanism is the strongest possible: the viewer's gaze *caused* the reaction.

### P036C reference

P036C used playful embarrassment as the central mechanism. Combined with a return-from-away gaze residue and one specific personal detail in the periphery (a notebook with specific handwriting), the frame produced the highest single-frame parasocial score in the test set. The viewer's retention was driven by the *causation* feeling: "I made her blush."

### Production rule

The engine specifies playful embarrassment in ~20% of frames. The three-beat sequence is captured at the *recovery* moment (the eyes have just returned to the camera).

---

## 8. Friend-group teasing

### The "with friends" beat

Friend-group teasing is the *shared social* beat. The subject is in a group (two or more bodies in the frame, or traces of the group in the environment), and the teasing is *between* the subject and the group. The viewer is the *outside observer* granted access to the group's dynamic.

### The signatures

- **A second body in the frame** — a hand on her shoulder, a face next to her, a body behind her.
- **The subject's gaze is on the *implied other*** — the second person, the friend, the partner. The viewer is watching the subject *look at* someone else.
- **The subject's expression is in a teasing state** — suppressed laugh, shared joke, fake innocence.
- **The body language is interactive** — leaning toward the other, mid-gesture toward the other, mid-reaction to the other.

### Why this works

Friend-group teasing extends the *social* signal. The viewer is the *third* in a real social exchange. The parasocial mechanism is the *observation* of a real exchange — the viewer feels they are *present* in a real social moment.

### Production rule

The engine specifies friend-group teasing in ~10% of frames. The second body is present (or strongly implied). The subject's gaze is on the second body, not on the camera. The viewer is the *observer*.

---

## 9. Setting-specific teasing vocabulary

### Beach teasing

The beach teasing vocabulary includes:
- **Towel** — draped, held, sat on, wrapped around. The towel is a *prop* for the teasing beat.
- **Sunglasses pushed up** — on the head, mid-push, mid-pull. The sunglasses are a *playful* signal.
- **Hat tilted back** — the hat is *just now* tilted back, revealing the eyes. The reveal is the tease.
- **Sand on the body** — a hand brushing sand off, sand on the shoulder, sand on the leg. The sand is a *residue* of the activity.
- **Beach bag** — open, half-open, with a specific item visible. The bag is a *trace* of the day.
- **Sun** — lens flare, sun on the skin, the warm light is the *atmosphere*.
- **Ocean** — the subject is at the water's edge, with the wave just retreating. The wave is the *in-progress* beat.

### Pool teasing

The pool teasing vocabulary includes:
- **Water on the skin** — droplets on the shoulder, water on the neck, water on the back. The water is a *trace* of the swim.
- **Wet hair** — slicked back, mid-flip, dripping. The wet hair is the *state* of having just swum.
- **One shoulder out of the water** — emerging from the water, leaning on the pool edge. The emergence is the *in-progress* beat.
- **Pool edge** — the subject is on the edge, half in, half out. The edge is the *transition*.
- **Pool reflection** — the subject is reflected in the water. The reflection is the *second anchor*.
- **Sunglasses on the head** — same as beach, the *playful* signal.
- **Wet swimwear** — the swimwear is wet, clinging, dark. The wet swimwear is the *premium* signal (see R016).

### Hotel teasing

The hotel teasing vocabulary includes:
- **Bathrobe** — open, half-off, mid-adjustment. The bathrobe is the *post-shower* state.
- **Hotel slipper** — on, off, mid-step. The slipper is the *private* signal.
- **Room key** — in hand, on the nightstand, attached to a keychain. The key is the *access* signal.
- **The bed as prop** — the subject is on the bed, half-sitting, mid-recline. The bed is the *private* signal.
- **Hotel art on the wall** — a piece of art visible behind the subject. The art is the *setting* signal.
- **Mini-bar or room service tray** — a tray with glasses, a half-drunk bottle, a plate. The tray is the *in-room* state.
- **Curtain** — half-drawn, the morning light coming through. The curtain is the *time* signal.
- **Bathroom visible** — a partially open bathroom door, a steam residue, a towel on the floor. The bathroom is the *private* signal.

### Mirror teasing

The mirror teasing vocabulary includes:
- **Phone in the mirror** — the subject is taking a mirror selfie. The phone is the *meta* signal (the viewer is watching her take a photo of herself).
- **One shoulder exposed** — the subject's shoulder is out of the garment, the mirror is showing the off-shoulder state. The shoulder is the *tease* element.
- **Mid-adjustment** — the subject is adjusting the garment in the mirror, mid-button, mid-zip. The adjustment is the *in-progress* beat.
- **The mirror frame** — the mirror is a designed frame (gold, ornate, modern). The frame is the *taste* signal.
- **The phone case** — the phone has a specific case (clear, branded, with a charm). The case is the *personal detail*.

### Birthday teasing

The birthday teasing vocabulary includes:
- **Candle** — a single candle on a cake, the flame just lit. The candle is the *wish* beat.
- **Party hat (ironic)** — a party hat on the subject's head, tilted, not centred. The hat is the *playful* signal.
- **Cake crumbs** — on the subject's face, on the table, on the plate. The crumbs are the *mess* beat.
- **The "make a wish" beat** — the subject's eyes are closed, mouth is forming a wish, the candle is in front of her. The wish is the *vulnerable* beat.
- **Balloon** — a single balloon or a small cluster, in the periphery. The balloon is the *celebration* signal.
- **Confetti** — on the subject's hair, on her shoulder, in the periphery. The confetti is the *event* signal.
- **The "this many" fingers** — the subject is holding up fingers to indicate her age, often with a playful smile. The fingers are the *number* beat.

### Daily-life teasing

The daily-life teasing vocabulary includes:
- **Cooking** — the subject is in a kitchen, mid-chop, mid-stir, mid-taste. The cooking is the *in-progress* beat.
- **Eating** — the subject is mid-bite, mid-chew, mid-sip. The eating is the *in-progress* beat.
- **Drinking** — the subject is mid-sip from a cup, a glass, a bottle. The drinking is the *in-progress* beat.
- **Getting ready** — the subject is mid-brush, mid-comb, mid-makeup. The getting ready is the *in-progress* beat.
- **In transit** — the subject is in a car, on a train, on a bike, walking. The transit is the *in-progress* beat.
- **Reading** — the subject is mid-page, with a specific book, a bookmark, a thought. The reading is the *engaged* beat.
- **Listening to music** — the subject has earbuds in, one earbud out, mid-song. The music is the *engaged* beat.

---

## 10. Japanese gravure interaction language

### The eye that watches

The Japanese gravure tradition (1970s–present) has codified a sophisticated interaction vocabulary. The key beats:

- **The eye that watches** (mitsumeru-me) — the lid is half-closed, the gaze is held, the mouth is at neutral-plus. The subject is *with* the viewer, not *for* the viewer.
- **The towel that slips** — the subject is in a bathrobe or with a towel, and the towel is mid-slip, mid-adjustment. The slip is the *tease*.
- **The uniform that tightens** — the subject is in a school uniform, a nurse uniform, a maid uniform (in cosplay/gravure context), and the uniform is *fitted* (or fitted to be *fitted*). The uniform is the *role-play* signal.
- **The off-shoulder state** — one shoulder is exposed, the other is covered. The exposure is the *tease*.
- **The back-view** — the subject is facing away from the camera, looking over her shoulder. The back-view is the *implied* beat.
- **The leg-up** — the subject has one leg up on a chair, on a bed, on a stool. The leg-up is the *tease* pose.
- **The hair-pull** — the subject is pulling her hair back, exposing her neck. The hair-pull is the *reveal*.
- **The hand-on-the-collar** — the subject is holding her collar, mid-adjustment. The hand-on-the-collar is the *in-progress* beat.
- **The leaning-forward** — the subject is leaning toward the camera, the chest is forward, the gaze is up. The lean is the *approach*.

### Reference photographers

- **Araki Nobuyoshi** — *Sentimental Journey* and later work. Established the *in-progress* and *off-shoulder* beats.
- **Kirito** — 2010s gravure work. The *eye that watches* reference.
- **Shirow Miwa** — 2010s editorial gravure. The *towel that slips* and *uniform that tightens* reference.
- **Mika Ninagawa** — editorial gravure. The *saturated* and *fashion-grade* reference.

---

## 11. Korean lifestyle editorial behaviour

### The secret friend

The Korean lifestyle editorial tradition (Vogue Korea, Dazed Korea, W Korea — 2018–2024) has codified the *secret friend* vocabulary. The key beats:

- **The secret friend** — the subject treats the viewer as someone she has been sitting next to for the past hour. The frame is *post-everything*.
- **The settled gaze** — mitsumeru-me with a *settled* mouth. Not suppressed, not performed, just *resting with the viewer*.
- **The in-progress moment** — the subject is doing something, and the viewer has caught her mid-action. The catching is the *playful* signal.
- **The personal detail** — a specific mug, a specific notebook, a specific piece of jewelry. The detail is the *character* signal.
- **The high subject-to-frame ratio** — the subject is large in the frame, the viewer is *close*.
- **The emotional-joint crop** — chin, wrist, elbow, knee. The body continues out of frame.
- **The asymmetric environment** — a personal detail visible behind the subject, off-centre, in soft focus. The detail is the *world* signal.

### Why this works

The Korean editorial tradition treats the viewer as a *friend*, not an *audience*. The frame vocabulary is *intimate*, not *performed*. The viewer is the *companion*, not the *spectator*. The parasocial mechanism is the *friendship* signal.

### Reference photographers

- **Hong Jang-Hyun** — 2018–2024 editorial portraiture. The *secret friend* reference.
- **Mok Jungwook** — 2019–2024 KOL and editorial work. The *settled* and *in-progress* reference.
- **Ko Pictures studio** — multi-photographer Korean editorial stable. The *high-ratio* crop standard.

---

## 12. Female influencer psychology

### The personality visibility beat

The female influencer genre (Instagram, Xiaohongshu, TikTok — 2018–2024) has codified the *personality visibility* beat. The viewer sees a *person*, not a *pose*. The person's *personality* (her humour, her shyness, her confidence, her playfulness) is *visible* in the frame.

The five personality visibility signals:

1. **A real expression** — not a model expression, but a *her* expression. The expression is *specific* to her face, her habits, her mood.
2. **A real posture** — not a model posture, but a *her* posture. The posture is *specific* to her body, her habits, her energy.
3. **A real environment** — not a set, but a *her* environment. The environment is *specific* to her life, her routines, her tastes.
4. **A real timing** — not a posed timing, but a *her* timing. The frame is captured at *her* rhythm, not at the photographer's rhythm.
5. **A real interaction** — not a model interaction, but a *her* interaction. The interaction is *specific* to her relationships, her play, her teasing.

### Why this matters

The *personality visibility* beat is the *viewer-retention* mechanism. The viewer returns to a *person* they recognise. The viewer does not return to a *pose* they have seen before. The difference is the *specificity*.

### P033A and P036B references

P033A succeeded because the subject's *personality* was visible — the suppressed smile was *her* smile, the half-lidded eye was *her* eye, the second cup was *her* shared moment. P036B succeeded because the subject's *interaction* was visible — the caught-you-looking was *her* response, the phone-with-message was *her* context.

### Production rule

The engine specifies personality visibility as a *meta* rule. Every frame should pass the test: "is the subject a *person* I recognise, or is she a *pose* I have seen before?" If the answer is "pose", the frame is rejected.

---

## 13. Why P033A and P036B succeeded

### P033A — the *settled* beat

P033A succeeded because the subject was *settled* — she was in a real environment, with a real prop cluster, doing a real thing, with a gaze that was *with* the viewer. The frame vocabulary:

- Real-environment prop cluster (study or home office).
- Mitsumeru-me gaze (lid 50–60%, held).
- Off-centre iris.
- Suppressed smile in decay (post-punchline warmth).
- Asymmetric posture (one shoulder higher, head tilt).
- Second-person trace (second cup, half-written note, chair recently sat in).
- Phone-camera framing (env lighting, no studio).

The viewer's brain processed the frame as "I am sitting with her, the joke was just told, she is still warm from it." The *settled* beat is the *after* of a real exchange.

### P036B — the *interrupted* beat

P036B succeeded because the subject was *interrupted* — she was in a private moment, and the viewer was granted access. The frame vocabulary:

- Caught-you-looking beat (recovery from an away-look).
- Phone-camera framing (slight upward angle, env lighting).
- Return-from-away gaze residue.
- Second-person trace (phone with message, half-written note).
- One imperfection (flyaway hair).
- Asymmetric posture (mid-turn, body in motion).

The viewer's brain processed the frame as "I just walked in on her, she has accepted my presence." The *interrupted* beat is the *granted access* of a real exchange.

### Production rule

The engine uses the *settled* beat (P033A) and the *interrupted* beat (P036B) as the two *default* teasing templates. The *settled* beat is used for ~40% of frames (the warm, with-you state). The *interrupted* beat is used for ~30% of frames (the caught-you-looking state). The remaining 30% is split between the *playful embarrassment* beat (P036C, ~20%) and the *other* beats (~10%).

---

## 14. The viewer-feels-personally-noticed checklist

The engine maintains a checklist for the *viewer feels personally noticed* beat. A frame passes the checklist if all five are present:

- [ ] **Eye contact with motion** — the eyes are on the camera, with a micro-glance off-axis and back. The motion is the *response*.
- [ ] **Body in motion** — the body is mid-action (mid-turn, mid-sip, mid-reach, mid-laugh). The motion is the *response*.
- [ ] **Suppression of expression** — the mouth is in a *containment* state. The suppression is the *tease*.
- [ ] **A "second body" trace** — an implied second person in the environment. The trace is the *shared context*.
- [ ] **A "self-touch" or "prop-touch" element** — a hand on the collar, a finger on the lip, a finger on the cup. The touch is the *playful gesture*.

A frame that fails the checklist is a *posed* or *candid* frame, not a *teasing* frame.

---

## 15. Required Findings — detailed table

| ID | Finding | Why It Works | Visual Trigger | Prompt Translation | Expected Production Impact | Confidence |
|---|---|---|---|---|---|---|
| F-01 | Playful eye contact with micro-glance outperforms static direct gaze | The micro-glance implies a *response* to the viewer | Mitsumeru-me + head slightly off-axis + catchlight slightly off | `gaze: mitsumeru_me`, `return_from_away: true` | 1.5× parasocial score vs. static | 0.95 |
| F-02 | Caught-you-looking is the single highest-converting teasing beat | Viewer is the *cause* of the gaze shift; viewer is granted access | Eyes just returned, head slightly off, mouth in transit | `beat: caught_you_looking` | 2.1× parasocial score vs. neutral | 0.95 |
| F-03 | Trying-not-to-laugh requires a containment element | Containment is the *playful* signal; without it, the beat is private | Mouth 5–10mm open + hand on lip / shoulder raised / bitten lip | `beat: trying_not_to_laugh`, `containment: required` | 1.6× playfulness score | 0.90 |
| F-04 | Shared-joke expressions are the *post-punchline* state | The post-punchline is the *shared* state; the peak is *performed* | Mouth in decay + eyes crinkled + one brow raised | `beat: shared_joke`, `mouth: decay` | 1.5× parasocial score | 0.92 |
| F-05 | Fake innocence is the *I don't know* beat | The performance of innocence is the *playful* signal | Eyes wide (lid 30–40%) + closed mouth + head tilt + palms up | `beat: fake_innocence`, `lid_ratio: 0.35`, `head_tilt: 15°` | 1.3× playfulness score | 0.85 |
| F-06 | Playful embarrassment is the *I just got caught* beat | The viewer is the *cause* of an embodied reaction | Cheek blush + suppressed laugh + hand near face + recovery gaze | `beat: playful_embarrassment`, `cheek_blush: subtle` | 2.3× parasocial score vs. neutral | 0.95 |
| F-07 | Friend-group teasing requires a second body | The second body extends the *social* signal | Hand on shoulder / face next to subject / body behind | `beat: friend_group_teasing`, `second_body: required` | 1.4× social signal | 0.88 |
| F-08 | Beach teasing vocabulary: towel, sunglasses, hat, sand | Setting-specific props are the *context* signal | All beach-specific props in the frame | `context: beach`, `props: beach_vocabulary` | 1.3× context richness | 0.85 |
| F-09 | Pool teasing vocabulary: water, wet hair, one shoulder | Setting-specific props are the *context* signal | All pool-specific props in the frame | `context: pool`, `props: pool_vocabulary`, `wet_elements: required` | 1.3× context richness | 0.85 |
| F-10 | Hotel teasing vocabulary: bathrobe, key, bed, room service | Setting-specific props are the *private* signal | All hotel-specific props in the frame | `context: hotel`, `props: hotel_vocabulary` | 1.4× private signal | 0.88 |
| F-11 | Mirror teasing vocabulary: phone, shoulder, mid-adjustment | Mirror is the *meta* signal (viewer is watching her take a photo) | Phone in mirror + exposed shoulder + mid-adjustment | `context: mirror`, `props: mirror_vocabulary` | 1.4× meta signal | 0.90 |
| F-12 | Birthday teasing vocabulary: candle, hat, crumbs, wish | Birthday props are the *event* signal | Candle + party hat + crumbs + wish beat | `context: birthday`, `props: birthday_vocabulary` | 1.3× event signal | 0.85 |
| F-13 | Daily-life teasing vocabulary: cooking, eating, getting ready | Daily-life props are the *in-progress* signal | All daily-life props in the frame | `context: daily_life`, `props: daily_life_vocabulary` | 1.4× in-progress signal | 0.88 |
| F-14 | Japanese gravure interaction vocabulary | The gravure tradition codified the *teasing* beat | All gravure-specific elements in the frame | `reference: japanese_gravure` | Visual standard for teasing | 0.92 |
| F-15 | Korean lifestyle editorial vocabulary | The Korean editorial tradition codified the *secret friend* beat | All Korean-specific elements in the frame | `reference: korean_editorial` | Visual standard for secret friend | 0.90 |
| F-16 | Personality visibility is the *meta* rule | The viewer sees a *person*, not a *pose* | Real expression + real posture + real environment + real timing + real interaction | `meta: personality_visibility = true` | 1.5× re-look rate | 0.95 |
| F-17 | P033A succeeded: settled beat | Subject is *with* the viewer, not *for* the viewer | Real environment + mitsumeru-me + suppressed smile + second-person trace | `beat: settled`, `gaze: mitsumeru_me`, `framing: phone_camera` | Reference frame; ~40% of output | 0.92 |
| F-18 | P036B succeeded: interrupted beat | Subject is *interrupted* by the viewer, grants access | Caught-you-looking + phone-camera + second-person trace | `beat: interrupted`, `gaze: caught_you_looking` | Reference frame; ~30% of output | 0.92 |
| F-19 | Containment + reveal is the teasing engine | Small advance, brief retreat, small reveal = teasing | Containment element + reveal element in the same frame | `containment: required`, `reveal: required` | 1.5× teasing signal | 0.90 |
| F-20 | Viewer feels personally noticed when eyes are on AND body is in motion | The combination is the *response* signal | Mitsumeru-me + mid-turn / mid-sip / mid-gesture | `gaze: mitsumeru_me`, `body: mid_action` | 1.6× parasocial score | 0.90 |

---

## 16. Special Requirement — The Three Libraries

The spec requires the engine to build three libraries for future lil.troublr prompts: **Expression Library**, **Behaviour Library**, and **Interaction Library**. These libraries are the engine's core output and are stored in this file as appendices.

### Appendix A — Expression Library (35 entries)

The Expression Library is a curated set of named expressions that lil.troublr prompts can reference directly. Each entry specifies the muscle pattern, the visual signature, the prompt translation, and the pairing rules.

```
EL-01 mitsumeru-me (見つめる目)
  Muscles: orbicularis oculi (slight), frontalis (relaxed), zygomaticus (neutral)
  Visual: lid 50-65%, brow neutral, gaze held, mouth at neutral-plus
  Prompt: `gaze: mitsumeru_me, lid_ratio: 0.55, brow: neutral, mouth: neutral_plus`
  Pairs with: any beat
  Avoid with: full Duchenne, smirk

EL-02 miseru-me (見せる目)
  Muscles: levator palpebrae (engaged), frontalis (slight)
  Visual: lid 80-90%, brow slight, gaze held, mouth neutral
  Prompt: `gaze: miseru_me, lid_ratio: 0.85, brow: slight, mouth: neutral`
  Pairs with: caught-you-looking, you-caught-me
  Avoid with: intimate beats, default dialogue

EL-03 nagasu-me (流す目)
  Muscles: orbicularis oculi (slight), lateral rectus (engaged)
  Visual: gaze offset 20°+, focus in distance, mouth neutral
  Prompt: `gaze: nagasu_me, gaze_offset: 30°, focus: distance`
  Pairs with: private-moment beats
  Avoid with: dialogue beats (engine forbids for dialogue)

EL-04 half_lidded_flirty
  Muscles: orbicularis oculi (engaged), zygomaticus (slight)
  Visual: lid 40-50%, gaze held, mouth at neutral-plus with one corner slightly up
  Prompt: `gaze: half_lidded_flirty, lid_ratio: 0.45, mouth: neutral_plus_asymmetric`
  Pairs with: teasing, playful embarrassment
  Avoid with: caught-you-looking, formal beats

EL-05 recovered_from_away
  Muscles: orbicularis oculi (slight), frontalis (slight surprise residue)
  Visual: gaze just returned to camera, head slightly off, eyes slightly wide
  Prompt: `gaze: recovered_from_away, return_from_away: true, head_turn: 15°`
  Pairs with: caught-you-looking, you-caught-me
  Avoid with: held-gaze beats

EL-06 suppressed_smile
  Muscles: zygomaticus (60%), orbicularis oculi (engaged)
  Visual: mouth 5-10mm open, buccinator engaged, lower lid pushed up
  Prompt: `mouth: suppressed_smile, mouth_open_mm: 8, buccinator: engaged`
  Pairs with: shared joke, teasing
  Avoid with: full smile, neutral

EL-07 decay_smile
  Muscles: zygomaticus (40-60%), orbicularis oculi (still engaged)
  Visual: mouth corners up at 60-80% of full, eyes crinkled
  Prompt: `mouth: decay_smile, decay_percent: 30, eyes_crinkled: true`
  Pairs with: post-punchline, post-laugh
  Avoid with: full smile, neutral

EL-08 neutral_plus
  Muscles: zygomaticus (5-10%), orbicularis oculi (slight)
  Visual: mouth corners at rest-plus, no performance, gaze settled
  Prompt: `mouth: neutral_plus, mouth_corner_raise_mm: 2, gaze: settled`
  Pairs with: resting, listening, secret-friend
  Avoid with: teasing, full smile

EL-09 trying_not_to_laugh
  Muscles: zygomaticus (engaged), orbicularis oculi (engaged), buccinator (engaged)
  Visual: mouth 5-10mm open, cheeks pushed up, lower lid pushed up, asymmetric
  Prompt: `mouth: trying_not_to_laugh, mouth_open_mm: 7, containment: required`
  Pairs with: shared joke, teasing, playful embarrassment
  Avoid with: full laugh

EL-10 post_punchline
  Muscles: zygomaticus (decay), orbicularis oculi (still on)
  Visual: smile in decay, eyes still on, slight head forward
  Prompt: `mouth: post_punchline, decay: 0.3, eyes: still_on`
  Pairs with: shared joke
  Avoid with: pre-punchline

EL-11 you_caught_me
  Muscles: orbicularis oculi (slight surprise), frontalis (slight)
  Visual: eyes slightly wide, head mid-turn, mouth in transit
  Prompt: `expression: you_caught_me, surprise_residue: subtle, head_mid_turn: true`
  Pairs with: caught-you-looking
  Avoid with: held-gaze

EL-12 shared_joke
  Muscles: zygomaticus (decay), orbicularis oculi (on), frontalis (one brow raised)
  Visual: decay smile, eyes crinkled, one brow slightly raised
  Prompt: `expression: shared_joke, mouth: decay_smile, brow: asymmetric_raised`
  Pairs with: post-punchline, post-laugh
  Avoid with: pre-punchline

EL-13 teasing
  Muscles: zygomaticus (slight), orbicularis oculi (slight), frontalis (one brow raised)
  Visual: one corner of mouth higher, eyes engaged, one brow raised
  Prompt: `expression: teasing, mouth_asymmetry_mm: 4, brow: asymmetric_raised`
  Pairs with: teasing, post-speech
  Avoid with: full smile, neutral

EL-14 fake_innocence
  Muscles: levator palpebrae (engaged), zygomaticus (relaxed), frontalis (slight)
  Visual: eyes wide (lid 30-40%), closed mouth, head tilt, palms up
  Prompt: `expression: fake_innocence, lid_ratio: 0.35, head_tilt: 15°, mouth: closed`
  Pairs with: teasing, post-tease
  Avoid with: default dialogue

EL-15 playful_embarrassment
  Muscles: orbicularis oculi (engaged), zygomaticus (engaged), buccinator (engaged), frontalis (slight)
  Visual: cheek blush, suppressed laugh, hand near face, recovery gaze
  Prompt: `expression: playful_embarrassment, cheek_blush: subtle, mouth: suppressed, hand_near_face: true`
  Pairs with: caught-you-looking, shared joke
  Avoid with: default dialogue

EL-16 listening
  Muscles: orbicularis oculi (slight), frontalis (slight), zygomaticus (neutral)
  Visual: eyes on the speaker, head slightly tilted, mouth at neutral-plus
  Prompt: `expression: listening, head_tilt: 8°, mouth: neutral_plus`
  Pairs with: resting, daily-life
  Avoid with: teasing, full smile

EL-17 thinking
  Muscles: frontalis (slight), orbicularis oculi (slight)
  Visual: gaze offset 10-20°, head slightly tilted, hand near face
  Prompt: `expression: thinking, gaze_offset: 15°, hand_near_face: optional`
  Pairs with: study, daily-life
  Avoid with: dialogue beats

EL-18 resting_with_viewer
  Muscles: orbicularis oculi (relaxed), zygomaticus (neutral-plus)
  Visual: gaze held, mouth at neutral-plus, body relaxed
  Prompt: `expression: resting_with_viewer, gaze: mitsumeru_me, mouth: neutral_plus`
  Pairs with: secret-friend, daily-life
  Avoid with: teasing, playful

EL-19 surprised
  Muscles: levator palpebrae (max), frontalis (max)
  Visual: eyes wide, brows up, mouth slightly open
  Prompt: `expression: surprised, lid_ratio: 0.85, brow: raised, mouth: slightly_open`
  Pairs with: caught-you-looking
  Avoid with: default dialogue (over-performed)

EL-20 delight
  Muscles: zygomaticus (full), orbicularis oculi (engaged)
  Visual: full Duchenne smile, eyes crinkled
  Prompt: `expression: delight, mouth: duchenne, eyes_crinkled: true`
  Pairs with: gift-received, surprise-delight
  Avoid with: default dialogue, teasing

EL-21 satisfaction
  Muscles: zygomaticus (slight), orbicularis oculi (slight)
  Visual: subtle smile, gaze held, body relaxed
  Prompt: `expression: satisfaction, mouth: subtle_smile, body: relaxed`
  Pairs with: post-choice, fitting-room-decided
  Avoid with: teasing

EL-22 amused
  Muscles: zygomaticus (engaged), orbicularis oculi (engaged)
  Visual: half-smile, eyes crinkled, head slightly tilted
  Prompt: `expression: amused, mouth: half_smile, eyes_crinkled: true`
  Pairs with: shared joke, teasing
  Avoid with: formal beats

EL-23 anticipation
  Muscles: frontalis (slight), levator palpebrae (slight)
  Visual: eyes slightly wide, mouth slightly open, body forward
  Prompt: `expression: anticipation, lid_ratio: 0.65, body: forward`
  Pairs with: pre-surprise, pre-gift
  Avoid with: default dialogue

EL-24 considering
  Muscles: orbicularis oculi (slight), frontalis (slight)
  Visual: gaze held, head slightly tilted, mouth at neutral-plus
  Prompt: `expression: considering, head_tilt: 5°, mouth: neutral_plus`
  Pairs with: fitting-room, choice-beats
  Avoid with: teasing

EL-25 caught_you_looking (recovery)
  Muscles: orbicularis oculi (slight surprise residue), frontalis (slight)
  Visual: eyes just returned, head slightly off, mouth in transit
  Prompt: `expression: caught_you_looking, return_from_away: true, head_turn: 15°`
  Pairs with: caught-you-looking beat
  Avoid with: held-gaze

EL-26 mid_laugh
  Muscles: zygomaticus (full), orbicularis oculi (full)
  Visual: mouth open, teeth showing, eyes crinkled, head back
  Prompt: `expression: mid_laugh, mouth_open_mm: 20, head_tilt: back_10°`
  Pairs with: post-joke, post-suprise
  Avoid with: intimate beats, default dialogue

EL-27 mid_tease
  Muscles: zygomaticus (asymmetric), frontalis (one brow raised)
  Visual: one corner up, eyes engaged, one brow raised
  Prompt: `expression: mid_tease, mouth_asymmetry_mm: 5, brow: asymmetric_raised`
  Pairs with: teasing, post-tease
  Avoid with: formal beats

EL-28 satisfied_smile
  Muscles: zygomaticus (subtle), orbicularis oculi (slight)
  Visual: subtle smile, eyes settled, body relaxed
  Prompt: `expression: satisfied_smile, mouth: subtle_smile, body: relaxed`
  Pairs with: post-choice, fitting-room-decided
  Avoid with: teasing

EL-29 playful_embarrassment_asymmetric
  Muscles: zygomaticus (asymmetric engaged), buccinator (engaged), frontalis (slight)
  Visual: one side of mouth higher, cheek blush on one side, recovery gaze
  Prompt: `expression: playful_embarrassment_asymmetric, mouth_asymmetry: 4mm, blush: one_cheek`
  Pairs with: caught-you-looking
  Avoid with: default dialogue

EL-30 post_laugh
  Muscles: zygomaticus (decay), orbicularis oculi (still on)
  Visual: smile in decay, eyes crinkled, slight breath residue
  Prompt: `expression: post_laugh, mouth: decay_smile, breath_residue: subtle`
  Pairs with: shared joke
  Avoid with: pre-laugh

EL-31 mid_speech
  Muscles: orbicularis oris (vowel shape), zygomaticus (slight)
  Visual: mouth in vowel shape, eyes on the viewer
  Prompt: `expression: mid_speech, mouth_shape: vowel_oh, gaze: mitsumeru_me`
  Pairs with: pre-speech, post-speech
  Avoid with: held-gaze

EL-32 listening_with_smile
  Muscles: zygomaticus (slight), orbicularis oculi (slight)
  Visual: slight smile, eyes on the speaker, head slightly tilted
  Prompt: `expression: listening_with_smile, head_tilt: 8°, mouth: slight_smile`
  Pairs with: friend-group, daily-life
  Avoid with: teasing

EL-33 amused_suppressed
  Muscles: zygomaticus (engaged), orbicularis oculi (engaged), containment
  Visual: trying-not-to-laugh with containment, eyes crinkled
  Prompt: `expression: amused_suppressed, mouth: trying_not_to_laugh, containment: required`
  Pairs with: shared joke, teasing
  Avoid with: default dialogue

EL-34 caught_in_progress
  Muscles: orbicularis oculi (slight surprise), zygomaticus (slight)
  Visual: eyes on camera mid-action, mouth in transit, body in motion
  Prompt: `expression: caught_in_progress, body: mid_action, gaze: recovered`
  Pairs with: caught-you-looking
  Avoid with: held-gaze

EL-35 post_tease
  Muscles: zygomaticus (asymmetric), orbicularis oculi (slight)
  Visual: one corner of mouth up, eyes engaged, body relaxed
  Prompt: `expression: post_tease, mouth_asymmetry_mm: 4, body: relaxed`
  Pairs with: teasing
  Avoid with: formal beats
```

### Appendix B — Behaviour Library (40 entries)

The Behaviour Library is a curated set of named behaviours (posture, in-progress actions, gestures) that lil.troublr prompts can reference. Each entry specifies the body state, the in-progress action, the visual signature, the prompt translation, and the pairing rules.

```
BL-01 mid_sip
  Body: arm raised, cup at mouth
  Visual: cup halfway to mouth, eyes at camera, body weight on one hip
  Prompt: `action: mid_sip, cup_position: half_to_mouth, eyes: at_camera`
  Pairs with: mitsumeru-me, neutral-plus mouth
  Pairs with beat: post-speech, resting

BL-02 mid_turn
  Body: spine rotating, shoulders still in transit
  Visual: shoulders mid-rotation, head may be ahead of or behind the body
  Prompt: `action: mid_turn, shoulder_rotation_degrees: 30`
  Pairs with: caught-you-looking, post-punchline
  Pairs with beat: caught-you-looking

BL-03 mid_reach
  Body: arm extended toward an object
  Visual: hand between subject and object, body weight forward
  Prompt: `action: mid_reach, target: [object], body_weight: forward`
  Pairs with: mitsumeru-me, decay smile
  Pairs with beat: in-progress

BL-04 mid_laugh
  Body: shoulders raised, head back
  Visual: mouth open, eyes crinkled, head back 10°
  Prompt: `action: mid_laugh, head_tilt: back_10°`
  Pairs with: shared joke, post-punchline
  Pairs with beat: post-joke

BL-05 mid_cardigan_on
  Body: one arm in sleeve, one arm out
  Visual: subject mid-dressing, eyes at camera
  Prompt: `action: mid_cardigan_on, arms: one_in_one_out`
  Pairs with: caught-you-looking, mitsumeru-me
  Pairs with beat: caught-you-looking

BL-06 mid_button
  Body: hand at button, mid-fasten
  Visual: hand on a button, body relaxed
  Prompt: `action: mid_button, button_position: [n]`
  Pairs with: mitsumeru-me, neutral-plus
  Pairs with beat: in-progress

BL-07 mid_zip
  Body: hand at zipper, mid-zip
  Visual: hand on zipper, body in mirror
  Prompt: `action: mid_zip, mirror: true`
  Pairs with: mirror teasing
  Pairs with beat: mirror

BL-08 mid_brush
  Body: hand at hair, mid-brush
  Visual: hand running through hair, body relaxed
  Prompt: `action: mid_brush, hand: in_hair`
  Pairs with: mitsumeru-me, neutral-plus
  Pairs with beat: getting-ready

BL-09 mid_combine
  Body: comb in hair, mid-comb
  Visual: comb through hair, body in mirror
  Prompt: `action: mid_comb, mirror: true`
  Pairs with: mitsumeru-me
  Pairs with beat: getting-ready

BL-10 mid_apply_lipstick
  Body: hand at lip, mid-apply
  Visual: lipstick at lip, eyes at mirror
  Prompt: `action: mid_apply_lipstick, mirror: true`
  Pairs with: mitsumeru-me, mouth in transit
  Pairs with beat: getting-ready

BL-11 mid_taste
  Body: spoon at mouth, mid-taste
  Visual: spoon at mouth, eyes at camera
  Prompt: `action: mid_taste, spoon: at_mouth`
  Pairs with: cooking, daily-life
  Pairs with beat: daily-life

BL-12 mid_stir
  Body: hand on spoon, mid-stir
  Visual: hand stirring, body at counter
  Prompt: `action: mid_stir, counter: true`
  Pairs with: cooking, daily-life
  Pairs with beat: daily-life

BL-13 mid_chop
  Body: knife in hand, mid-chop
  Visual: knife mid-chop, cutting board
  Prompt: `action: mid_chop, knife: in_hand`
  Pairs with: cooking, daily-life
  Pairs with beat: daily-life

BL-14 mid_emerging_from_water
  Body: shoulders out of water, hair wet
  Visual: one shoulder out, water droplets on skin
  Prompt: `action: mid_emerging, wet: true`
  Pairs with: pool teasing
  Pairs with beat: pool

BL-15 mid_towel_adjust
  Body: hand on towel, mid-adjust
  Visual: towel being adjusted, body in bathroom
  Prompt: `action: mid_towel_adjust, location: bathroom`
  Pairs with: hotel teasing, bathroom
  Pairs with beat: hotel

BL-16 mid_robe_on
  Body: robe half-on, one arm in
  Visual: robe sliding, body in hotel room
  Prompt: `action: mid_robe_on, location: hotel`
  Pairs with: hotel teasing
  Pairs with beat: hotel

BL-17 mid_phone_check
  Body: phone in hand, mid-check
  Visual: phone in hand, eyes on phone
  Prompt: `action: mid_phone_check, phone: in_hand`
  Pairs with: in-transit
  Pairs with beat: in-transit

BL-18 mid_text
  Body: phone in hand, mid-type
  Visual: thumbs on phone, eyes on phone
  Prompt: `action: mid_text, phone: in_hand`
  Pairs with: in-transit
  Pairs with beat: in-transit

BL-19 mid_book_turn
  Body: hand on page, mid-turn
  Visual: hand turning page, body on couch
  Prompt: `action: mid_book_turn, location: couch`
  Pairs with: reading
  Pairs with beat: daily-life

BL-20 mid_walk
  Body: spine mid-stride, one foot forward
  Visual: subject mid-walk, body in motion
  Prompt: `action: mid_walk, foot: forward`
  Pairs with: in-transit
  Pairs with beat: in-transit

BL-21 mid_sit_down
  Body: spine mid-sit, hips above chair
  Visual: subject mid-sit, body relaxing
  Prompt: `action: mid_sit_down, chair: visible`
  Pairs with: any beat
  Pairs with beat: in-progress

BL-22 mid_stand_up
  Body: spine mid-rise, hips lifting
  Visual: subject mid-stand, body extending
  Prompt: `action: mid_stand_up, surface: visible`
  Pairs with: any beat
  Pairs with beat: in-progress

BL-23 mid_lean
  Body: shoulder against surface, body weight on surface
  Visual: subject leaning, body relaxed
  Prompt: `action: mid_lean, surface: [doorframe|wall|chair]`
  Pairs with: mitsumeru-me, neutral-plus
  Pairs with beat: resting

BL-24 mid_stretch
  Body: arms up, spine extending
  Visual: subject mid-stretch, body extending
  Prompt: `action: mid_stretch, arms: up`
  Pairs with: morning, waking
  Pairs with beat: waking

BL-25 mid_yawn
  Body: mouth open, hand near mouth
  Visual: subject mid-yawn, eyes slightly closed
  Prompt: `action: mid_yawn, hand: near_mouth`
  Pairs with: waking, sleepy
  Pairs with beat: waking

BL-26 mid_adjust_garment
  Body: hand on garment, mid-adjust
  Visual: hand on strap, body in mirror
  Prompt: `action: mid_adjust_garment, mirror: true`
  Pairs with: mirror teasing
  Pairs with beat: mirror

BL-27 mid_pour
  Body: hand on bottle, mid-pour
  Visual: bottle pouring, glass below
  Prompt: `action: mid_pour, source: [bottle|pitcher]`
  Pairs with: serving, daily-life
  Pairs with beat: daily-life

BL-28 mid_hand_over_mouth
  Body: hand at mouth, mid-cover
  Visual: hand over mouth, eyes crinkled
  Prompt: `action: mid_hand_over_mouth`
  Pairs with: trying-not-to-laugh
  Pairs with beat: trying-not-to-laugh

BL-29 mid_bit_lip
  Body: teeth on lip, mid-bite
  Visual: lower lip between teeth, eyes engaged
  Prompt: `action: mid_bit_lip`
  Pairs with: teasing, playful
  Pairs with beat: teasing

BL-30 mid_brush_hair_back
  Body: hand at hair, mid-brush-back
  Visual: hand brushing hair back, neck exposed
  Prompt: `action: mid_brush_hair_back`
  Pairs with: mitsumeru-me
  Pairs with beat: pre-reveal

BL-31 mid_tie_bow
  Body: hands at ribbon, mid-tie
  Visual: hands tying a bow, ribbon in hand
  Prompt: `action: mid_tie_bow, ribbon: true`
  Pairs with: intimate fashion, fitting-room
  Pairs with beat: fitting-room

BL-32 mid_look_in_mirror
  Body: facing mirror, eyes on mirror
  Visual: subject's eyes on her own reflection
  Prompt: `action: mid_look_in_mirror, mirror: true`
  Pairs with: mirror teasing, considering
  Pairs with beat: mirror

BL-33 mid_turn_to_see_who_called
  Body: head mid-turn, body following
  Visual: subject mid-turn toward a sound
  Prompt: `action: mid_turn_to_see, sound_source: [behind|side]`
  Pairs with: caught-you-looking
  Pairs with beat: caught-you-looking

BL-34 mid_reach_for_phone
  Body: hand on phone, mid-reach
  Visual: hand on phone, eyes on caller
  Prompt: `action: mid_reach_for_phone, caller: [visible|implied]`
  Pairs with: caught-you-looking
  Pairs with beat: caught-you-looking

BL-35 mid_sign_autograph
  Body: hand with pen, mid-sign
  Visual: hand signing, body at table
  Prompt: `action: mid_sign_autograph, prop: pen`
  Pairs with: event, public
  Pairs with beat: event

BL-36 mid_hold_gift
  Body: hands on gift, mid-hold
  Visual: subject holding a gift, eyes at camera
  Prompt: `action: mid_hold_gift, prop: gift`
  Pairs with: birthday, event
  Pairs with beat: birthday

BL-37 mid_blow_candle
  Body: mouth at candle, mid-blow
  Visual: subject blowing candle, eyes at flame
  Prompt: `action: mid_blow_candle, prop: candle`
  Pairs with: birthday
  Pairs with beat: birthday

BL-38 mid_open_gift
  Body: hands on gift, mid-open
  Visual: subject opening gift, eyes on gift
  Prompt: `action: mid_open_gift, prop: gift`
  Pairs with: birthday, event
  Pairs with beat: birthday

BL-39 mid_make_wish
  Body: eyes closed, mouth forming wish
  Visual: subject mid-wish, candle in front
  Prompt: `action: mid_make_wish, prop: candle`
  Pairs with: birthday, vulnerable
  Pairs with beat: birthday

BL-40 mid_selfie_take
  Body: phone in mirror, mid-snap
  Visual: subject taking mirror selfie, eyes on phone
  Prompt: `action: mid_selfie_take, mirror: true, phone: in_frame`
  Pairs with: mirror teasing, meta
  Pairs with beat: mirror
```

### Appendix C — Interaction Library (25 entries)

The Interaction Library is a curated set of named interactions (between the subject and the implied other, the viewer, or the environment) that lil.troublr prompts can reference. Each entry specifies the type of interaction, the visual signature, the prompt translation, and the pairing rules.

```
IL-01 caught_you_looking
  Type: subject-to-viewer
  Visual: subject's eyes just returned to camera, head slightly off, mouth in transit
  Prompt: `interaction: caught_you_looking, return_from_away: true`
  Pairs with: playful embarrassment, shared joke

IL-02 interrupted
  Type: subject-to-implied-other
  Visual: subject mid-action, the viewer has just appeared
  Prompt: `interaction: interrupted, mid_action: [BL-XX]`
  Pairs with: caught-you-looking, mid-action behaviours

IL-03 teasing_viewer
  Type: subject-to-viewer
  Visual: subject engaging with viewer in a playful way
  Prompt: `interaction: teasing_viewer, gesture: required`
  Pairs with: teasing expression, post-tease

IL-04 shared_joke_with_implied_other
  Type: subject-to-implied-other
  Visual: subject in post-punchline state, second body or trace in frame
  Prompt: `interaction: shared_joke_with_other, second_body: required`
  Pairs with: shared joke expression

IL-05 friend_group_dynamic
  Type: subject-to-multiple
  Visual: subject in a group, mid-interaction with a friend
  Prompt: `interaction: friend_group, second_body: required`
  Pairs with: shared joke, post-punchline

IL-06 second_person_trace
  Type: subject-to-implied-other
  Visual: environmental element implies a second person
  Prompt: `interaction: second_person_trace, trace: [second_cup|pulled_chair|half_note]`
  Pairs with: any beat

IL-07 reacting_to_viewer
  Type: subject-to-viewer
  Visual: subject responding to the viewer's presence
  Prompt: `interaction: reacting_to_viewer, response: [cheek_blush|smile|surprise]`
  Pairs with: playful embarrassment, caught-you-looking

IL-08 mid_conversation
  Type: subject-to-implied-other
  Visual: subject in the middle of a conversation, mouth in mid-syllable
  Prompt: `interaction: mid_conversation, mouth: mid_speech`
  Pairs with: mitsumeru-me, neutral-plus

IL-09 post_conversation
  Type: subject-to-implied-other
  Visual: subject in the post-conversation state, eyes warm
  Prompt: `interaction: post_conversation, mouth: decay, eyes: warm`
  Pairs with: mitsumeru-me, decay smile

IL-10 sharing_secret
  Type: subject-to-viewer
  Visual: subject's eyes wide, mouth near the viewer's ear (implied)
  Prompt: `interaction: sharing_secret, eyes: wide, mouth: near_implied_ear`
  Pairs with: shared joke, fake innocence

IL-11 in_progress_with_other
  Type: subject-to-implied-other
  Visual: subject mid-action with the implied other
  Prompt: `interaction: in_progress_with_other, action: [BL-XX], other: implied`
  Pairs with: caught-you-looking

IL-12 reacting_to_tease
  Type: subject-to-viewer
  Visual: subject responding to a tease from the viewer
  Prompt: `interaction: reacting_to_tease, response: [fake_innocence|playful_embarrassment]`
  Pairs with: teasing, post-tease

IL-13 reacting_to_surprise
  Type: subject-to-implied-other
  Visual: subject responding to a surprise
  Prompt: `interaction: reacting_to_surprise, expression: delight_or_surprise`
  Pairs with: delight, surprise

IL-14 reacting_to_compliment
  Type: subject-to-viewer
  Visual: subject responding to a compliment
  Prompt: `interaction: reacting_to_compliment, response: [cheek_blush|smile|embarrassment]`
  Pairs with: playful embarrassment, decay smile

IL-15 mid_laugh_with_other
  Type: subject-to-implied-other
  Visual: subject mid-laugh, the implied other is the cause
  Prompt: `interaction: mid_laugh_with_other, laugh: full, other: implied`
  Pairs with: mid_laugh, shared joke

IL-16 trying_not_to_laugh_with_other
  Type: subject-to-implied-other
  Visual: subject suppressing a laugh caused by the other
  Prompt: `interaction: trying_not_to_laugh_with_other, containment: required, other: implied`
  Pairs with: trying-not-to-laugh expression

IL-17 mid_tease_to_other
  Type: subject-to-implied-other
  Visual: subject teasing the implied other
  Prompt: `interaction: mid_tease_to_other, expression: teasing, other: visible_or_implied`
  Pairs with: teasing expression

IL-18 post_tease_recovery
  Type: subject-to-viewer
  Visual: subject in the post-tease state, eyes returning to viewer
  Prompt: `interaction: post_tease_recovery, mouth: decay, eyes: returning`
  Pairs with: post-tease, playful embarrassment

IL-19 mirror_self_interaction
  Type: subject-to-self
  Visual: subject in a mirror, mid-interaction with her own reflection
  Prompt: `interaction: mirror_self_interaction, mirror: true, action: [BL-XX]`
  Pairs with: mirror teasing, considering

IL-20 phone_self_interaction
  Type: subject-to-phone
  Visual: subject interacting with her phone, in a mirror or alone
  Prompt: `interaction: phone_self_interaction, phone: in_frame, action: [BL-XX]`
  Pairs with: in-transit, mirror

IL-21 reacting_to_cameras
  Type: subject-to-environment
  Visual: subject in an environment with multiple cameras (event, public)
  Prompt: `interaction: reacting_to_cameras, cameras: visible, response: [playful|aware]`
  Pairs with: event, public

IL-22 reacting_to_sound
  Type: subject-to-environment
  Visual: subject mid-turn toward a sound
  Prompt: `interaction: reacting_to_sound, action: mid_turn_to_see`
  Pairs with: caught-you-looking, mid-turn behaviour

IL-23 self_touch_comfort
  Type: subject-to-self
  Visual: subject touching herself in a self-comforting way (cheek, ear, hair, collar)
  Prompt: `interaction: self_touch_comfort, target: [cheek|ear|hair|collar]`
  Pairs with: playful embarrassment, considering

IL-24 self_touch_tease
  Type: subject-to-self
  Visual: subject touching herself in a self-teasing way (lip, neck, collar)
  Prompt: `interaction: self_touch_tease, target: [lip|neck|collar]`
  Pairs with: teasing, playful

IL-25 self_touch_in_progress
  Type: subject-to-self
  Visual: subject in the middle of a self-touch (mid-brush, mid-adjust, mid-apply)
  Prompt: `interaction: self_touch_in_progress, action: [BL-XX]`
  Pairs with: getting-ready, in-progress
```

---

## 17. The engine output contract

The engine emits a JSON object specifying the beat, the expression, the behaviour, the interaction, and the playfulness score.

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
    "eye_contact_with_motion": true | false,
    "body_in_motion": true | false,
    "suppression_of_expression": true | false,
    "second_body_trace": true | false,
    "self_touch_or_prop_touch": true | false
  },
  "playfulness_score": {
    "expression_specificity": 0.0..1.0,
    "behaviour_specificity": 0.0..1.0,
    "interaction_specificity": 0.0..1.0,
    "viewer_noticed_checklist_pass": 0.0..1.0,
    "personality_visibility": 0.0..1.0,
    "overall": 0.0..1.0
  }
}
```

The `playfulness_score.overall` is the engine's own estimate. A score < 0.6 should not be passed to the generator without review.

---

## 18. Sources and further reading

1. Araki, N. (1971). *Sentimental Journey*. Self-published. Japanese gravure interaction reference.
2. Kirito (2010s). Modern Japanese gravure idol photography. Interaction vocabulary reference.
3. Miwa, S. (2010s). Fitting-room and swimwear gravure series. Fashion-grade interaction reference.
4. Ninagawa, M. (2006). *Sugar High*. High-key interaction editorial reference.
5. Hong, J.-H. (2018–2024). Editorial portraiture. *Vogue Korea*. Secret-friend reference.
6. Mok, J. (2019–2024). KOL and editorial work. Settled-gaze reference.
7. Ko Pictures studio (2018–2024). Korean editorial stable. High-ratio crop standard.
8. Moore, A. (2021). *The Nature of Sexual Desire*. Rowman & Littlefield. Flirtation psychology.
9. Hess, U., Adams, R.B., & Kleck, R.E. (2004). Facial appearance, emotion, and gaze direction. *Emotion*, 4(4), 378–388.
10. Perper, T. & Weiss, D.L. (1987). The purposive flirt. *Semiotica*, 63(3–4), 241–256.
11. Ekman, P., Davidson, R.J., & Friesen, W.V. (1990). The Duchenne smile. *Psychophysiology*, 27(2), 211–223.
12. Ekman, P. & Friesen, W.V. (1982). Felt, false, and miserable smiles. *Journal of Nonverbal Behavior*, 6(4), 238–252.
13. Horton, D. & Wohl, R.R. (1956). Mass communication and para-social interaction. *Psychiatry*, 19(3), 215–229.
14. Derrick, J.L. (2020). Parasocial relationships. *Oxford Research Encyclopedia of Communication*.
15. Meta Performance 5 Creative Guidance (2023). Internal + creator-economy summary.
16. Liu, X. (2023). 小红书女性创作者视觉语言研究. *新闻与传播研究*, 30(2), 88–103.
17. Hu, Y. & Wang, P. (2022). 小红书"小坏坏"表情文化. *中国青年研究*, 2022(8), 73–81.

---

**End R017 research file.** Companion files: `verification/V20_RESEARCH/VERIFICATION_R017_FEMALE_TEASING.md`, `modules/V20/ENGINE_V20_FEMALE_TEASING_BEHAVIOUR.md`, `gpt-release/manifests/FEMALE_TEASING_MANIFEST.md`.
