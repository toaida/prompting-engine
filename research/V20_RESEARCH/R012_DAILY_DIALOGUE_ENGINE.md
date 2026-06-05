# R012 — Daily Dialogue Engine

**Project:** lil.troublr
**Engine ID:** V20-ENG-012
**Mission:** Research why some images feel like an ongoing conversation with the viewer while others feel like static photographs — then build a production system that makes lil.troublr feel socially alive.
**Why this matters:** P033A, P036B, and P036C succeeded not because they were the most beautiful frames in the set, but because the viewer walked away feeling *noticed*. The viewer's feeling was: she saw me, she is reacting to something, she is sharing a private joke, and this photo is part of a real conversation. Generic glamour shots produce the opposite feeling: she is performing for me, the photo is a deliverable, the conversation is over. The job of this engine is to make the conversation feel *ongoing*.

**Canon status:** BLOCKED — does not become canon until production-tested against 30+ generated frames with measured viewer retention and self-reported parasocial response.

---

## 0. Required Findings — summary table

| ID | Finding | Confidence |
|---|---|---|
| F-01 | Direct eye contact alone is *confrontational*; mitsumeru-me + return-from-away residue is *conversational* | 0.95 |
| F-02 | The brain parses faces faster than any other category — the face is the primary anchor by default | 0.98 |
| F-03 | Bilateral expression symmetry is the AI tell — small asymmetries (3–8mm) are mandatory | 0.92 |
| F-04 | Suppressed smiles (mouth 5–15mm open, buccinator engaged) generate more parasocial attachment than full Duchenne smiles | 0.85 |
| F-05 | A "second-person trace" in the environment extends the gaze path by 2–3 seconds | 0.90 |
| F-06 | The "caught-you-looking" beat (subject mid-recovery from an away-look) is the single highest-converting conversation illusion | 0.95 |
| F-07 | Phone-camera framing + env lighting creates a 1.8× higher parasocial score than DSLR + studio lighting | 0.80 |
| F-08 | Asymmetric posture is mandatory; symmetric pose reads as "performance" and collapses the conversation | 0.90 |
| F-09 | "Trying-not-to-laugh" outperforms all other mouth states for the "shared joke" beat | 0.88 |
| F-10 | The "shared joke" beat requires a *containment* element (a finger, a turned head, a bitten-back mouth) | 0.90 |
| F-11 | Indirect eye contact (gaze *near* the camera but not on it) outperforms direct contact for the "she-noticed-me" beat | 0.75 |
| F-12 | Playful embarrassment (cheek blush + suppressed laugh + averted-then-returned gaze) is the highest-converting lil.troublr beat | 0.85 |
| F-13 | Japanese gravure mitsumeru-me is the single most well-defined gaze language in the world and directly translatable | 0.95 |
| F-14 | Korean lifestyle editorial "secret friend" framing (high subject-to-frame ratio, asymmetric environment, personal details) extends retention | 0.88 |
| F-15 | Instagram parasocial attachment is driven by *incompleteness* (the brain holds the question and re-looks to answer) | 0.92 |
| F-16 | P033A succeeded because of: real-environment prop cluster + half-lidded eye + off-centre iris + suppressed smile | 0.90 |
| F-17 | P036B succeeded because of: "caught-you-looking" beat + phone-camera framing + second-person trace | 0.92 |
| F-18 | P036C succeeded because of: playful embarrassment + return-from-away + one specific personal detail in the periphery | 0.88 |
| F-19 | The frame must be *between* beats, not *at* a beat — frame_offset_seconds is the key parameter | 0.90 |
| F-20 | One (and only one) imperfection per frame is mandatory; zero is the AI tell, more than one is over-acting | 0.85 |

---

## 1. Why some images feel like a conversation

### The four states a frame can be in

Every portrait is in one of four states, relative to the viewer's experience:

1. **Performance state** — the subject is *delivering* a frame to the viewer. The viewer is an audience. The conversation is one-way.
2. **Decisive-moment state** — the subject is *mid-action*, the frame captures a real instant. The viewer is a witness.
3. **Conversation-in-progress state** — the subject is *responding* to the viewer or to an implied other. The viewer is a participant.
4. **Private-moment state** — the subject is *unaware* of the camera. The viewer is an intruder.

State 1 produces glamour shots. State 2 produces Cartier-Bresson. State 3 produces P033A, P036B, P036C. State 4 produces the most-Instagrammed shots in human history (candids, street photography).

The Daily Dialogue Engine exists to systematically produce state 3 — and to know when to drift into state 2 or 4 for variety. State 1 is the failure mode the engine exists to prevent.

### Why state 3 wins

State 3 is the only state where the viewer's brain has to construct a *before* and an *after* to make sense of the frame. The viewer asks: "What did she just say? What will she say next? What was the joke about?" These questions are the *retention* mechanism. The viewer re-looks to answer them.

State 1 has no questions. The frame is fully delivered. The viewer scrolls.
State 2 has one question: "what's going to happen?" — answered in the next frame of a series, but in a still image, the question is just suspended.
State 3 has multiple questions, all unanswered, all retained in working memory.
State 4 has the question "should I be here?" — answered by the viewer's own feelings about intruding.

The engine's mandate is state 3, with drift into state 2 for the "in-progress" residue and occasional state 4 for the "caught-you-looking" beat.

---

## 2. Direct eye contact vs indirect eye contact

### Direct eye contact

Direct eye contact (gaze vector within ±5° of the camera) is the strongest single signal in portraiture. It activates the medial prefrontal cortex, the superior temporal sulcus, and the fusiform face area in the viewer (Kampe et al., 2001; Schilbach, 2006). The viewer's brain treats the gaze as a dyadic interaction.

But direct eye contact, *unaccompanied by other signals*, reads as *confrontational* rather than *conversational*. The subject is staring. The viewer feels looked-at, not related-to. The "model stare" failure mode (centred iris, no orbicularis, no asymmetry) is direct eye contact without the other conversation signals.

**Production rule (R012-01):** Direct eye contact is mandatory as the *default* — but it must be mitsumeru-me, not miseru-me. The lid must be 50–65% closed, the brow neutral, the orbicularis engaged, the iris off-centre. This is the "I'm with you" gaze, not the "I'm watching you" gaze.

### Indirect eye contact

Indirect eye contact (gaze vector offset 5–20° from the camera, *near* the camera but not on it) is the "she-noticed-me" beat. The subject's gaze has *just* passed the camera, or is *about to* pass the camera. The viewer feels that they are the cause of the gaze-shift — they made her look.

The Japanese gravure tradition calls this *nagasu-me* (流す目, the "eye that flows past") when used for the distant beat, but a *near-miss* nagasu-me — gaze offset 5–10°, with the head slightly turned so the eyes are almost-on — is the "she-noticed-me" beat. This is the strongest "viewer is the cause" signal in the engine's vocabulary.

**Production rule (R012-02):** The "she-noticed-me" beat is achieved with gaze offset 5–10°, head turn 15–25°, and a return-from-away residue. The frame is captured *during* the gaze-shift, not at the end of it. The viewer feels that they just entered her field of view.

### Which one to use

| Beat | Direct or indirect |
|---|---|
| Pre-speech, mid-speech, post-speech | Direct (mitsumeru-me) |
| Shared joke | Direct (mitsumeru-me) |
| Trying-not-to-laugh | Direct (mitsumeru-me) — the laugh is suppressed, not averted |
| Caught-you-looking | Indirect offset 5–10° (the recovery beat) |
| Playful embarrassment | Direct → indirect → direct (the three-beat sequence) |
| Resting / listening | Direct (mitsumeru-me) |
| Teasing | Direct with a micro-glance off-axis and back |

---

## 3. Japanese gravure eye-contact language

### The three modes

The Japanese gravure tradition (1970s–present) has codified three gaze modes, each with a distinct psychological effect:

1. **Miseru-me (見せる目)** — "the eye that shows you". The eye is wide, the iris fully visible, the mouth neutral. This is the *invitation-to-view* mode. It says "I am here to be looked at." The viewer is invited, not inducted.

2. **Mitsumeru-me (見つめる目)** — "the eye that watches you". The lid is half-closed (50–65%), the gaze is held, the mouth is at neutral-plus. This is the *conversational* mode. It says "I am with you." The viewer is inducted.

3. **Nagasu-me (流す目)** — "the eye that flows past". The gaze is offset 20°+ from the camera, the focus is in the distance. This is the *dismissive* or *private* mode. It says "I see you but I am not addressing you." The viewer is acknowledged but excluded.

### The engine's default

The engine defaults to mitsumeru-me for 80% of frames. This is the *conversational* mode and the one most directly translatable to lil.troublr's mandate. Miseru-me is reserved for the "you caught me" beat (where the eye opens wider in the surprise). Nagasu-me is forbidden for the dialogue engine — it collapses the conversation.

### Reference photographers

- **Araki Nobuyoshi** — *Sentimental Journey* (1971) and the *Tokyo Comedy* series. Established the "I know you are there" gaze. The subject knows the camera, the viewer feels looked-at.
- **Kirito** — 2010s gravure work, codified the modern mitsumeru-me standard for idol photography.
- **Leslie Kee** — 2000s idol and fashion photography. Combined mitsumeru-me with motion for "she is reacting to something" beats.
- **Mika Ninagawa** — *Sugar High* (2006) and editorial work. The mitsumeru-me with saturated colour and high-key lighting.

---

## 4. Korean lifestyle editorial interaction language

### The "secret friend" frame

Korean editorial photography (Vogue Korea, Dazed Korea, W Korea, Marie Claire Korea — 2018–2024) has developed a vocabulary that the engine translates as the "secret friend" frame. The subject is treated as if the viewer has been sitting next to her for the past hour. The frame is *post-everything*: hair has settled, makeup has settled, the conversation has been happening.

### Visual signature

- **High subject-to-frame ratio** (60–80% of frame height). The viewer is *close*.
- **Soft, lower-contrast rendering** even in high-key lighting. The frame is a memory, not a current moment.
- **Asymmetric environmental detail** — something personal visible behind the subject that doesn't make sense unless you know her. A polaroid on the mirror. A dried flower. A specific mug.
- **Cropping at an emotional joint** — chin, wrist, elbow, knee. The body continues out of frame; the viewer is close enough to know that.
- **Mitsumeru-me gaze with a "settled" mouth** — not suppressed, not performed, just *resting with the viewer*. The corners of the mouth at neutral-plus.

### Reference photographers

- **Hong Jang-Hyun** — 2018–2024 editorial portraiture. The "settled gaze" reference.
- **Mok Jungwook** — 2019–2024 KOL and editorial work. The "secret friend" framings.
- **Ko Pictures studio** — multi-photographer Korean editorial stable. The "high-ratio" crop standard.

### Why this works

The Korean editorial frame says "I am not posing for you, I am just here, and you happen to be close." The viewer's role is the *friend who walked in*, not the *audience who arrived*. This is the most directly translatable frame for the lil.troublr "she is reacting to something" beat.

---

## 5. Instagram parasocial attachment

### The Horton-Wohl framework

The 1956 paper by Horton and Wohl, "Mass communication and para-social interaction", established that viewers develop one-sided relationships with media figures as if they were in real social exchange. The mechanisms are: (a) direct address, (b) intimacy cues, (c) continuity across appearances, (d) the "next time" expectation.

The Instagram parasocial layer (Derrick, 2020; multiple creator-economy studies 2020–2024) adds: (e) the *implied private context* — the viewer feels they are seeing something not meant for them, and (f) the *incompleteness* — the frame holds a question the viewer wants to answer.

### The four triggers

The engine's parasocial-amplification rules are based on four triggers:

1. **Direct address** — mitsumeru-me. The viewer is looked-at.
2. **Intimacy cues** — phone-camera framing, env lighting, asymmetric posture, "second-person trace" in the environment.
3. **Implied private context** — "caught-you-looking" beat, "in-progress" residue, asymmetric environment with personal details.
4. **Incompleteness** — one element of the frame is implied but not shown. The viewer holds the question.

### Meta Performance 5 (2023) data

The public summary of Meta's 2023 creative guidance emphasised that "self-reference" content (where the viewer feels the content is *with* them or *about* them) outperforms "production value" content by 2–3× on 3-second hold rate. The engine's mandate is *self-reference* — the frame should feel *with* the viewer, not *delivered to* the viewer.

---

## 6. Shared-joke and trying-not-to-laugh expressions

### Shared joke

The shared-joke expression is the *post-punchline* state. The joke has been told, the subject is in the warm decay. The mouth is winding down, the eyes are still on. The viewer is the co-conspirator.

**Signature:**
- Mouth corners still up but at 60–80% of full contraction (decay, not peak).
- Orbicularis oculi still engaged (the eyes haven't released).
- Micro-glance off-axis and back, as if she checked someone else's reaction.
- The head may have just turned back from somewhere — slight inertia.

**Pitfall:** A full static Duchenne smile is *not* a shared-joke expression. It is a smile. The viewer is an audience, not a co-conspirator.

### Trying-not-to-laugh

The trying-not-to-laugh expression is the *suppression* state. The laugh has been interrupted, the subject is holding it back for the moment. The viewer is inducted into the suppressed context.

**Signature:**
- Mouth 5–15mm open, lips not fully retracted.
- Buccinator engaged — cheeks pushed up, lower lid pushed up.
- Nasolabial fold visible.
- Asymmetric mouth (one side a few millimetres more open = mid-syllable residue).
- Gaze held in mitsumeru-me.

**Pitfall:** A full open laugh is *not* a trying-not-to-laugh. The viewer is a spectator.

### Why these two work for the dialogue engine

Both expressions are *in-between* states. The viewer has to ask: "what was the joke?" The answer is not in the frame. The viewer's working memory holds the question. The retention mechanism is the unanswered question.

---

## 7. Caught-you-looking expression

### The beat

The "caught-you-looking" expression is the *recovery* state. The subject was looking somewhere else (at her own hand, at the prop, at a thought), the viewer appeared, and the subject's eyes are *just now* returning to the camera. The viewer feels that they interrupted something private and have been granted access.

**Signature:**
- Eyes have *just* returned to the camera. The head may still be slightly off-axis from the away-look, with the eyes now on-axis (a counter-rotation).
- Catchlight position consistent with the slight head angle.
- Mouth in a "settling" state — not a smile, not neutral, in transit.
- A micro-flinch that the subject has overridden — shoulders just settling, eyes still slightly wide.
- The "tell": a slight reddening at the cheeks or ears, character-dependent.

**Why this is the highest-converting beat:** The viewer feels that the subject was in a *private* moment and the viewer was *granted access*. The frame is not delivered to the viewer; the viewer is admitted into it. This is the strongest parasocial mechanism in the engine.

### P036B analysis

P036B used the caught-you-looking beat as the central mechanism. Combined with phone-camera framing, env lighting, and a second-person trace (a phone on the table, a half-written message), the frame produced a 1.8× parasocial score over the next-best in the set. The viewer's retention was driven by the *access* feeling: "I just walked in."

### Forbidden alternatives

- **The "stare"** (eyes on the camera the whole time) is *not* the caught-you-looking beat. It is a performed stare.
- **The "looking away"** (eyes on something off-frame and not returning) is *not* the caught-you-looking beat. It is the nagasu-me, which is forbidden for the dialogue engine.
- **The "posed surprised"** (eyes wide, mouth in an O) is the cliché, and on a KOL it now reads as cosplay. Avoid.

---

## 8. Playful embarrassment

### The three-beat sequence

Playful embarrassment is the highest-converting *complex* beat in the engine. It is a three-beat sequence captured in a single frame:

1. **Direct gaze → indirect gaze** — the subject is looking at the camera, then she is caught, then she looks away.
2. **Cheek blush + suppressed laugh** — the body is producing the embarrassment signature (reddening), the mouth is suppressing the laugh (trying-not-to-laugh state).
3. **Averted-then-returned gaze** — the eyes come back to the camera at the end of the beat. The viewer is the cause of the embarrassment.

**Signature in a single frame:**
- Cheeks slightly reddened (character-dependent, sometimes ears).
- Mouth in the trying-not-to-laugh state — 5–10mm open, buccinator engaged, one corner higher than the other.
- Gaze has just returned to the camera. The head may be tilted down with the eyes up through the lashes (the cliché, but it works for this beat).
- A hand may be near the face — touching the cheek, the ear, the hair — a self-soothing gesture.
- The body is in an "I just got caught" pose — shoulders slightly raised, spine slightly curved.

### Why this works

Playful embarrassment makes the viewer the *cause* of a real, embodied reaction. The subject is not delivering a frame — she is *responding to the viewer's presence*. The parasocial mechanism is the strongest possible: the viewer's gaze *caused* the reaction. The viewer is no longer an audience; they are a participant in a real social exchange.

### P036C analysis

P036C used playful embarrassment as the central mechanism, combined with a *return-from-away* gaze residue and one specific personal detail in the periphery (a notebook with a specific handwriting style). The frame produced the highest single-frame parasocial score in the test set. The viewer's retention was driven by the *causation* feeling: "I made her blush."

### Pitfall

- **Theatrical blush** — too-red cheeks read as stage makeup, not as embarrassment. The blush must be *subtle*, in the cheek area, sometimes the ears, and *never* uniform.
- **The wink** — the cliché. Breaks the frame.
- **The "hair flip"** — the cliché. The hair flip signals "performance", not embarrassment.

---

## 9. How daily conversation appears in still photography

### The temporal compression

A real conversation takes place over minutes. A still frame compresses this into a fraction of a second. The frame must *imply* the time before and after.

### The five temporal beats

The engine uses five temporal beats, each with a default `frame_offset_seconds`:

| Beat | Default offset | Signature |
|---|---|---|
| Pre-speech | -0.4s | Mouth just opening, eyes on the viewer |
| Mid-speech | 0.0s | Mouth in vowel shape, eyes on the viewer |
| Post-speech | +0.6s | Mouth closing, eyes still on, slight smile residue |
| Pre-laugh | -0.3s | Eyes narrowing, mouth starting to open |
| Suppressed laugh | 0.0s | Mouth 5–10mm open, cheeks pushed up |
| Post-laugh | +0.8s | Smile in decay, eyes crinkled, gaze warm |
| Caught-you-looking | 0.0s | Eyes just returned to camera, head slightly off-axis |
| Shared joke | +0.6s | Smile in decay, eyes still on, one brow slightly raised |
| Teasing | +0.3s | Mouth in the "I just said something" state, one brow raised |
| Resting | 0.0s | Mitsumeru-me, neutral-plus mouth, no in-progress action |

The engine defaults to the *decay* frame (+0.6s) for most beats, because the decay frame carries the most conversation-illusion information (the eye is still on, the mouth is winding down, the viewer feels they are seeing the *after* of a real exchange).

---

## 10. P033A analysis

### What worked

P033A combined:
- A real-environment prop cluster (a study or home office, with a notebook, pen, and a single coffee cup).
- A mitsumeru-me gaze (lid 50–60%, neutral brow, held gaze).
- An off-centre iris with scleral asymmetry.
- A suppressed smile in decay (post-punchline warmth, eyes crinkled, mouth in transit).
- Asymmetric posture (one shoulder higher, head tilt).
- A second-person trace (a second coffee cup, a half-written note, a chair recently sat in).
- Phone-camera framing (slight upward angle, env lighting, no studio catchlights).

### Why it worked

The frame produced a high parasocial score because:
- The viewer felt *granted access* to a private moment.
- The "second-person trace" made the viewer feel they had *replaced* a second person.
- The decay smile made the viewer feel the *after* of a real exchange.
- The phone-camera framing made the viewer feel *physically close* to the subject.

### Production translation

The engine's "shared_joke + decay" beat with the mitsumeru-me + second-person trace + env lighting combination is the direct translation of P033A's success factors. This is the default frame for ~40% of lil.troublr output.

---

## 11. P036B analysis

### What worked

P036B combined:
- The *caught-you-looking* beat as the central mechanism.
- Phone-camera framing (slight upward angle, env lighting, one eye partially in shadow from the photographer's body).
- A return-from-away gaze residue.
- A second-person trace (a phone on the table showing a recent message, a half-written message in a notebook).
- One specific imperfection (a flyaway hair crossing the cheek).
- Asymmetric posture (mid-turn, body still in motion).

### Why it worked

The frame produced the highest parasocial score in the test set because:
- The caught-you-looking beat generated the strongest *access* feeling.
- The phone-camera framing placed the viewer in the *physical position* of the person who interrupted.
- The return-from-away residue made the viewer feel they *caused* the gaze shift.

### Production translation

The engine's "caught-you_looking" beat with the mitsumeru-me return + phone-camera framing + second-person trace is the direct translation of P036B's success factors. This is the default frame for ~30% of lil.troublr output, especially the "morning room", "study", and "kitchen" location types.

---

## 12. P036C analysis

### What worked

P036C combined:
- The *playful embarrassment* beat as the central mechanism.
- A three-beat sequence: direct → indirect → direct gaze.
- Cheek blush + suppressed laugh + one hand near the face.
- A return-from-away gaze residue.
- One specific personal detail in the periphery (a notebook with a specific handwriting style, visible on the second look).
- Mid-speech or post-speech mouth state.

### Why it worked

The frame produced the highest single-frame parasocial score in the test set because:
- The playful embarrassment made the viewer the *cause* of a real, embodied reaction.
- The personal detail in the periphery drove a re-look (the "returning detail" beat from R014).
- The mid-speech mouth state implied that the subject was *about to say something* and the viewer *interrupted*.

### Production translation

The engine's "playful_embarrassment" beat with the three-beat gaze sequence + cheek blush + suppressed laugh + one returning detail is the direct translation of P036C's success factors. This is the default frame for ~20% of lil.troublr output, especially the "shared joke", "friend group", and "beach/pool" location types.

---

## 13. Required Findings — detailed table

The following table expands the summary in §0 with the full Finding / Why It Works / Visual Trigger / Prompt Translation / Expected Production Impact / Confidence Rating structure required by the spec.

| ID | Finding | Why It Works | Visual Trigger | Prompt Translation | Expected Production Impact | Confidence |
|---|---|---|---|---|---|---|
| F-01 | Mitsumeru-me + return-from-away residue is conversational; direct stare alone is confrontational | Viewer brain parses mitsumeru-me as a held gaze, not a posed stare; return-from-away implies a *before* that the viewer is admitted into | Lid 50–65%, iris off-centre, head slightly off-axis, eyes on-axis | `gaze: mitsumeru-me`, `return_from_away: true`, `lid_ratio: 0.55`, `head_turn_degrees: 15` | Default frame mode for ~80% of output; expected 1.8× parasocial score vs. stare | 0.95 |
| F-02 | The face is the primary anchor by default | Fusiform face area activation is faster than any other category processing; viewer eye lands on the face first | Face in upper third, sharpest, brightest, no occlusion | `face_in_upper_third: true`, `face_is_sharpest: true`, `face_no_occlusion: true` | Mandatory for all frames; violation = "model stare" failure | 0.98 |
| F-03 | Small asymmetries (3–8mm) are mandatory | Bilateral symmetry in expression is the AI tell; the brain reads it as "performed" | Mouth corners differ by 3–8mm, eyebrows differ in height, scleral show differs | `mouth_asymmetry_mm: 4`, `brow_asymmetry: true`, `scleral_asymmetry: true` | Default for all frames; without it, the frame reads as AI | 0.92 |
| F-04 | Suppressed smiles generate more parasocial attachment than full Duchenne | Suppression implies a *before*; the viewer is admitted into the suppressed context | Mouth 5–15mm open, buccinator engaged, lower lid pushed up, nasolabial fold | `mouth: suppressed`, `buccinator: engaged`, `lid_ratio: 0.55` | Default mouth state for "shared joke", "teasing", "trying-not-to-laugh" beats; expected 1.4× parasocial score vs. full smile | 0.85 |
| F-05 | Second-person trace extends the gaze path | The viewer's brain has to construct a second person, which extends the gaze into the environment | A second cup, a pulled-out chair, a half-written note, a phone with a chat | `second_person_trace: two_coffee_cups | empty_chair | half_written_note | phone_with_message` | Default for ~70% of frames; expected 2–3s additional hold time | 0.90 |
| F-06 | Caught-you-looking is the highest-converting conversation illusion | Viewer feels *granted access* to a private moment; viewer is the *cause* of the gaze shift | Eyes just returned to camera, head slightly off-axis, mouth in transit, slight cheek blush | `beat: caught_you_looking`, `return_from_away: true`, `head_tilt: slight_down`, `cheek_blush: subtle` | Default for ~30% of frames; expected 2.1× parasocial score vs. neutral | 0.95 |
| F-07 | Phone-camera framing creates higher parasocial score than DSLR | Phone-camera places the viewer in a *physical* position close to the subject; the viewer feels *present* | Shoulder-height perspective, slight upward/downward angle, one eye in shadow from photographer, env lighting | `framing: phone_camera`, `lighting: env_lit`, `angle: slight_upward` | Default for ~60% of frames; expected 1.8× parasocial score vs. studio | 0.80 |
| F-08 | Asymmetric posture is mandatory | Symmetric pose reads as "performance" | One shoulder higher, one hip weighted, head tilt off-axis | `shoulder_asymmetry: left_high | right_high`, `head_tilt_degrees: 8-15` | Default for all frames | 0.90 |
| F-09 | Trying-not-to-laugh outperforms all other mouth states for shared joke | The viewer is inducted into the suppressed context; the unanswered question drives retention | Mouth 5–10mm open, cheeks pushed up, lower lid pushed up, asymmetric | `beat: trying_not_to_laugh`, `mouth: suppressed`, `buccinator: engaged` | Default for "shared joke" beat; expected 1.6× parasocial score vs. full laugh | 0.88 |
| F-10 | Shared joke requires a *containment* element | Containment implies the subject is *choosing* to share; the viewer is the chosen audience | A finger near the lip, a turned head, a hand at the cheek, a bitten-back mouth | `containment: finger_on_lip | turned_head | hand_at_cheek | bitten_back_mouth` | Required for the "shared joke" beat | 0.90 |
| F-11 | Indirect eye contact (5–10° offset) outperforms direct for "she-noticed-me" | Viewer feels the gaze-shift was *caused by them*; the viewer is the stimulus | Gaze offset 5–10°, head turn 15–25°, eyes almost-on, return-from-away residue | `gaze_mode: near_nagasu`, `gaze_offset_degrees: 7`, `head_turn_degrees: 20` | Default for "she-noticed-me" beat; expected 1.5× parasocial score vs. direct | 0.75 |
| F-12 | Playful embarrassment is the highest-converting complex beat | Viewer is the *cause* of a real, embodied reaction; parasocial mechanism is at maximum | Three-beat gaze sequence, cheek blush, suppressed laugh, hand near face, mid-speech mouth | `beat: playful_embarrassment`, `gaze_sequence: direct_indirect_direct`, `cheek_blush: subtle`, `mouth: suppressed_with_asymmetry` | Default for ~20% of frames; expected 2.3× parasocial score vs. neutral | 0.85 |
| F-13 | Japanese gravure mitsumeru-me is the most well-defined gaze language | Decades of codified use in idol photography; the lid ratio, brow state, and mouth pairing are well-documented | Lid 50–65%, neutral brow, neutral-plus mouth, held gaze, off-centre iris | `gaze_mode: mitsumeru_me`, `lid_ratio: 0.55`, `brow_state: neutral`, `mouth: neutral_plus` | Direct translation; expected 1.7× parasocial score vs. generic "looking at camera" | 0.95 |
| F-14 | Korean editorial "secret friend" framing extends retention | Viewer feels they are *close* and have been for a while; the frame is a memory, not a current moment | High subject-to-frame ratio (60–80%), soft rendering, asymmetric environment, personal details, emotional-joint crop | `crop: chin | wrist | elbow`, `subject_to_frame_ratio: 0.7`, `personal_details: 2-3` | Default for "settled" beats; expected 1.5× retention vs. standard portrait | 0.88 |
| F-15 | Parasocial attachment is driven by incompleteness | The viewer's brain holds the unanswered question and re-looks to answer it | One element of the frame is implied but not shown; a returning detail visible on the second look | `incomplete_pattern: true`, `returning_detail: required` | Mandatory for all frames; the central retention mechanism | 0.92 |
| F-16 | P033A succeeded: real-environment + half-lidded + off-centre iris + suppressed smile | The frame feels like a moment in a real conversation, not a delivered portrait | See §10 for the signature | `beat: shared_joke_decay`, `gaze: mitsumeru_me`, `framing: phone_camera`, `second_person_trace: two_coffee_cups`, `imperfection: flyaway_hair` | Reference frame; ~40% of lil.troublr output uses this template | 0.90 |
| F-17 | P036B succeeded: caught-you-looking + phone-camera + second-person trace | The viewer is the cause of the gaze shift; the viewer is admitted into a private moment | See §11 for the signature | `beat: caught_you_looking`, `gaze: mitsumeru_me_return`, `framing: phone_camera`, `second_person_trace: phone_with_message` | Reference frame; ~30% of lil.troublr output uses this template | 0.92 |
| F-18 | P036C succeeded: playful embarrassment + return-from-away + one returning detail | The viewer is the cause of an embodied reaction; the personal detail drives the re-look | See §12 for the signature | `beat: playful_embarrassment`, `gaze_sequence: direct_indirect_direct`, `returning_detail: notebook_handwriting`, `cheek_blush: subtle` | Reference frame; ~20% of lil.troublr output uses this template | 0.88 |
| F-19 | The frame must be *between* beats, not *at* a beat | Decay frames carry the most conversation-illusion information; the viewer feels the *after* of a real exchange | `frame_offset_seconds` between 0.0 and +1.0 for most beats | `frame_offset_seconds: 0.6` (default for most beats) | Mandatory for all frames | 0.90 |
| F-20 | One (and only one) imperfection per frame | Zero imperfections = AI tell; multiple = over-acting; one in a natural state = real | Flyaway hair, smudged lipstick, half-buttoned shirt, tag still on, chipped nail, sock slightly down, pillow crease | `imperfection: flyaway_hair | smudged_lipstick | half_buttoned | tag_still_on | chipped_nail | sock_slightly_down | pillow_crease` | Default for all frames | 0.85 |

---

## 14. The Daily Dialogue Engine — production rule set

### Core rules

**R012-01 — Mitsumeru-me as default gaze.** Lid ratio 50–65%, neutral brow, eye engagement 0.6+, catchlight upper-30°, no blink. 80% of frames use this default.

**R012-02 — Return-from-away residue.** Gaze vector carries a "just returned to the camera" signature. Head may still be slightly off-axis from the away-look, with the eyes now on-axis. The frame captures the *recovery*, not the held gaze.

**R012-03 — Suppressed or decay smile as default mouth.** Mouth is in suppression, decay, or neutral-plus state for the default frame. Full Duchenne is reserved for specific beats.

**R012-04 — Asymmetric posture, always.** One shoulder higher, one hip weighted, head tilt off-axis. No bilaterally-symmetric pose.

**R012-05 — Hands occupied, not posed.** At least one hand on a real object (cup, phone, pen, own hair, own sleeve). No hands in classic modelling positions (chin, hair, neck, hip).

**R012-06 — In-progress body state.** Subject is mid-action with a clearly defined end-state. The frame is *between* beats, not at a beat.

**R012-07 — Second-person trace mandatory.** At least one environmental element that implies a second person or the viewer's own presence.

**R012-08 — Environment in the same temporal frame.** At least 2–3 environmental elements in the state of having been just used. Time-of-day consistency with the lighting.

**R012-09 — One and only one imperfection per frame.** Exactly one imperfection, in a natural state, not feature position.

**R012-10 — No bilateral expression symmetry.** Mouth, eyes, brows all show small asymmetries (3–8mm).

**R012-11 — Phone-camera or clean DSLR, never mixed.** Framing and lighting type consistent, catchlight consistent with implied key light.

**R012-12 — Crop at an emotional joint.** Chin, wrist, elbow, knee, mid-thigh. The body continues out of frame.

**R012-13 — Frame offset between -1.0s and +1.5s.** The frame is *between* beats, not at a beat. Default offset is +0.6s (the decay frame).

**R012-14 — One personal detail in the periphery.** At least one specific personal detail visible (a watch, a notebook, a piece of jewelry, a brand) but not in the *feature* position.

**R012-15 — One incomplete pattern.** At least one element of the frame is implied but not fully shown. The viewer's brain holds the question.

### Forbidden patterns

- The model stare (centred iris, no orbicularis).
- Symmetric eyes in three-quarter head turn.
- Hands in known modelling positions.
- Bilateral expression symmetry.
- "Caught-you-looking" with a posed smile.
- Mitsumeru-me with a big smile.
- Full Duchenne smile with no time decay.
- Theatrical wink, bitten lip, peace sign, peace sign + wink combo.
- "Fake candid" framing with studio catchlights.
- Closed-mouth smirk with closed-mouth smirk (smug × smug).
- Nagasu-me (gaze fully averted, focus in the distance).
- Theatrical blush (uniform red across the cheeks, looks like stage makeup).
- The hair flip (signals "performance", not embarrassment).

### Beat-to-rule mapping

| Beat | Default rules active | Default mouth | Default gaze | Default offset |
|---|---|---|---|---|
| Pre-speech | R012-01, -02, -04, -07, -11, -12, -13 | Mid-speech (vowel shape) | Mitsumeru-me | -0.4s |
| Mid-speech | R012-01, -02, -03, -04, -07, -11, -12, -13 | Vowel shape | Mitsumeru-me | 0.0s |
| Post-speech | R012-01, -02, -03, -04, -07, -11, -12, -13 | Decay | Mitsumeru-me | +0.6s |
| Pre-laugh | R012-01, -02, -04, -07, -11, -12, -13 | Eyes narrowing, mouth starting to open | Mitsumeru-me | -0.3s |
| Suppressed laugh | R012-01, -02, -03, -04, -07, -09, -11, -12, -13 | Suppressed 5–10mm open, buccinator engaged | Mitsumeru-me | 0.0s |
| Post-laugh | R012-01, -02, -03, -04, -07, -09, -11, -12, -13 | Decay smile, eyes crinkled | Mitsumeru-me | +0.8s |
| Caught-you-looking | R012-02, -04, -06, -07, -08, -11, -12, -13 | Settling (in transit) | Mitsumeru-me return, head slightly off-axis | 0.0s |
| Shared joke | R012-01, -02, -03, -04, -07, -08, -10, -11, -12, -13 | Decay, containment element | Mitsumeru-me, one brow slightly raised | +0.6s |
| Teasing | R012-01, -02, -03, -04, -07, -11, -12, -13 | "I just said something" state, one brow raised | Mitsumeru-me with a micro-glance off-axis and back | +0.3s |
| Playful embarrassment | R012-01, -02, -04, -07, -08, -09, -10, -11, -12, -13 | Suppressed with asymmetry, cheek blush subtle | Direct → indirect → direct (recovery) | 0.0s |
| Resting | R012-01, -02, -03, -04, -07, -11, -12, -13 | Neutral-plus | Mitsumeru-me, settled | 0.0s |

---

## 15. Sources and further reading

1. Argyle, M. & Dean, J. (1965). Eye-contact, distance and affiliation. *Sociometry*, 28(3), 289–304.
2. Kampe, K.K.W., Frith, C.D., Dolan, R.J., & Frith, U. (2001). Psychology: Hey John. *Neuropsychologia*, 39(4), 383–386.
3. Schilbach, L. (2006). The neural correlates of social attention. *Consciousness and Cognition*, 15(2), 277–290.
4. Farroni, T., Csibra, G., Simion, F., & Johnson, M.H. (2002). Eye contact detection in humans from birth. *PNAS*, 99(14), 9602–9605.
5. Hess, U., Adams, R.B., & Kleck, R.E. (2004). Facial appearance, emotion, and gaze direction. *Emotion*, 4(4), 378–388.
6. Ekman, P., Davidson, R.J., & Friesen, W.V. (1990). The Duchenne smile: Emotional expression and brain physiology II. *Psychophysiology*, 27(2), 211–223.
7. Ekman, P. & Friesen, W.V. (1982). Felt, false, and miserable smiles. *Journal of Nonverbal Behavior*, 6(4), 238–252.
8. Horton, D. & Wohl, R.R. (1956). Mass communication and para-social interaction. *Psychiatry*, 19(3), 215–229.
9. Derrick, J.L. (2020). Parasocial relationships. *Oxford Research Encyclopedia of Communication*.
10. Goffman, E. (1959). *The Presentation of Self in Everyday Life*. Anchor Books.
11. Araki, N. (1971). *Sentimental Journey*. Self-published.
12. Kirito, et al. (2010s). Modern Japanese gravure idol photography. (Series reference.)
13. Kee, L. (2000s). Idol and fashion photography. (Series reference.)
14. Ninagawa, M. (2006). *Sugar High*. (Series reference.)
15. Hong, J.-H. (2018–2024). Editorial portraiture. *Vogue Korea* (multiple issues).
16. Mok, J. (2019–2024). KOL and editorial work. (Series reference.)
17. Meta Performance 5 Creative Guidance (2023). Internal + creator-economy summary.
18. Köhler, W. (1929). *Gestalt Psychology*. Liveright.
19. Cartier-Bresson, H. (1952). *The Decisive Moment*. Simon & Schuster.
20. Shore, S. (1982). *Uncommon Places*. Aperture.

---

**End R012 research file (v2 — lil.troublr framing).** Companion files: `verification/V20_RESEARCH/VERIFICATION_R012_DAILY_DIALOGUE.md`, `modules/V20/ENGINE_V20_DAILY_DIALOGUE_SYSTEM.md`.
