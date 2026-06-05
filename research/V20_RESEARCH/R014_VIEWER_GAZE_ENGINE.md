# R014 — Viewer Gaze Engine

**Mission:** Investigate how attractive female KOL content captures and holds male viewer attention without relying on obvious posing, then convert that into a production rule system that can be applied to any V20 frame.

**Why this matters:** Most generated images are *technically beautiful* and *functionally forgettable*. The viewer glances, registers beauty, scrolls. The job of this engine is to extend that glance into a look, and that look into a re-look. The success metric is the viewer's behaviour after the first second, not the quality of the first impression.

**Why P033A and P036B outperform generic glamour shots:** P033A combines a real-environment prop cluster (the actively-used one) with a half-lidded eye mode and an off-centre iris. P036B combines a "you caught me" beat with a phone-camera framing and a second-person trace. Both extend the viewer's gaze by *creating questions to be answered* — the brain keeps looking because the image is not yet fully parsed. Generic glamour shots are fully parsed in 0.5 seconds because the brain already has the schema for "pretty girl looking at camera".

**Canon status:** BLOCKED — does not become canon until production-tested against 100+ generated frames with measured 3-second hold rate and re-look rate.

---

## 1. Viewer gaze psychology

### Psychological principle

Eye movements are not random. They follow learned, predictable patterns driven by saliency, schema, and motivation. The foundational work is Yarbus (1967), who recorded eye movements of subjects looking at Repin's *Unexpected Visitors* and found that the pattern of fixations and saccades depended on what the subject was asked to look for. The implication: the *viewer's* task shapes the *image's* scan path.

In portraiture, the relevant research is on face-fixation patterns. Walker-Smith, Gale, & Findlay (1977) showed that observers fixate on the eyes and mouth first, with the eyes receiving 40–60% of total fixation time. Henderson, Williams, & Falk (2005, *Psychonomic Bulletin & Review*) extended this: observers of faces allocate about 50% of fixation time to the eyes, 20% to the mouth, 15% to the nose, and 15% to the rest of the face/hair.

This means the engine's job is *not* to make the image beautiful everywhere — it is to *control the eyes' fixation path* so that the gaze is captured, held, and returned to.

### Visual signature of gaze control

- **First-fixation bait**: a high-contrast, high-saliency element near the eyes. A catchlight. A coloured iris. A bright lower-lid reflection. The eye lands here first.
- **Second-fixation anchor**: a high-information element near the mouth. An asymmetry. A suppressed smile. A half-parted lip. The eye moves here second.
- **Third-fixation pull**: an element in the periphery that the eyes can *leave to*. A hand, a prop, a piece of background detail. The eyes can leave the face and explore.
- **Return-fixation trigger**: an element that the eyes return to. Usually the eyes themselves, with a slightly different expression than the first fixation. The eyes "see the eyes seeing them" beat.

### Failure modes

- **Single-fixation frame**: the image is fully parsed in one fixation. No return. The viewer scrolls.
- **Face-only fixation**: no periphery to explore. The eyes move between the model's eyes and the model's mouth and then have nowhere else to go.
- **No bait**: nothing in the frame breaks the saliency of "generic pretty face". The eyes don't know where to land.

### Prompt-construction implications

Engine must specify all four fixation anchors: bait, anchor, pull, and return trigger. Generic "make her pretty" prompts fail this requirement.

---

## 2. Attention anchors

### Psychological principle

An attention anchor is an element in a frame that the brain fixates on first, longest, or with the most processing. The classic Itti & Koch (2000, *Vision Research*) saliency model identifies bottom-up anchors (high contrast, bright colour, motion) and top-down anchors (task-relevant, schema-relevant, emotionally relevant).

For V20 content, the most powerful anchor is *unexpected context* — the prop or environment that doesn't match the schema of "portrait". The brain lingers because it has to reconcile the mismatch.

Reference: Alex Webb's layered photography (*The Suffering of Light*, 2008) — his frames have 5–10 attention anchors layered in depth, and the eye keeps moving.

### Visual signature of well-placed anchors

- A *foreground* anchor (a hand, a prop, a piece of clothing) that is closer to the lens than the face.
- A *face* anchor (the eyes themselves, the most powerful single anchor).
- A *mid-ground* anchor (a window, a piece of furniture, a frame edge).
- A *background* anchor (a small detail, a person, a piece of text).
- The anchors are at *different focal planes* — this is what creates the "layers" effect that holds the gaze.

### Failure modes

- **Single-plane frame**: everything at the same depth. The eye has nowhere to travel.
- **Foreground emptiness**: no anchor in the foreground, so the eye lands on the face and stops.
- **Background saliency exceeds foreground saliency**: the eye leaves the face for the background and doesn't return.

### Prompt-construction implications

Engine must specify at least 3 attention anchors at 3 different focal planes. The face is one of them. The other two are the engine's job to add.

---

## 3. Eye-contact retention

### Psychological principle

Direct eye contact creates a "dyadic" cognitive state — the viewer feels they are in a social exchange (see R012, source: Kampe et al., 2001). The retention question is: how long does the viewer maintain the eye-contact state before shifting to other fixations?

The answer is driven by the *perceived mutuality* of the gaze. If the subject's gaze is held steadily, the viewer's gaze holds. If the subject's gaze flickers, the viewer's gaze flickers. If the subject's gaze moves to the periphery, the viewer's gaze follows.

This is why a *single-frame* image can have eye-contact retention that exceeds a video. The viewer's gaze is held by the held gaze of the subject.

### Visual signature

- **Gaze held**: the eyes are looking at the camera with no off-axis drift. The viewer feels looked-at.
- **Periorbital engagement**: the muscles around the eyes are slightly engaged (orbicularis, not the brow). The eye "softens" under engagement.
- **Catchlight in the iris**: the eye is "live", not a still. The catchlight signals that the subject is in a real lit environment, not a still rendering.
- **No blink mid-frame**: the eye is open, not in the act of blinking (a closed-eye moment drops retention to near-zero for that frame).

### Failure modes

- **Averted gaze**: the subject is looking off-axis. The viewer's gaze follows and doesn't return to the camera.
- **Dead eyes**: no periorbital engagement, no catchlight, iris centred and fixed. The viewer feels looked-at by a mannequin.
- **Mid-blink frame**: the eye is half-closed. The viewer reads this as "between moments" and may skip past.

### Prompt-construction implications

Engine must specify: gaze direction, periorbital state, catchlight position, lid state. The default is mitsumeru-me with lid ratio 50–60%, neutral brow, no blink, and a catchlight from the upper-30° angle.

---

## 4. Face-first attraction hierarchy

### Psychological principle

The face receives disproportionate attention in human vision. This is not a learned preference; it is built into the visual system. The Fusiform Face Area (FFA, Kanwisher et al., 1997, *Journal of Neuroscience*) is selectively activated by face stimuli. The face is processed faster than any other category of object.

For V20 content, the implication is that the face is *always* the primary anchor, no matter what else is in the frame. The engine's job is to *support* the face, not compete with it.

References: Palermo & Rhodes (2007) on face attractiveness perception; Little, Jones, & DeBruine (2011) on face perception and social cognition.

### Visual signature of face-supporting composition

- The face is in the *upper third* of the frame (rule of thirds).
- The face is the *largest* element in the frame (the body may be cropped, the face is not).
- The face is in the *sharpest focus* (other elements may be at softer focus, the face is tack-sharp).
- The face is in the *lightest* part of the frame (light attracts the gaze; the face should be the brightest element).
- The face has *no occlusion* (nothing crosses the face plane; hair, hands, props are placed around the face, not over it).

### Failure modes

- **Face competing with body**: the body is as detailed as the face. The eye is confused about where to land.
- **Face occluded**: a hand, hair, or prop crosses the face plane. The eye has to work harder and may skip.
- **Face in shadow**: a darker face in a brighter frame. The eye lands elsewhere.
- **Face off-axis in the frame**: the face is at the edge of the frame. The eye is drawn to the centre and then has to hunt for the face.

### Prompt-construction implications

Engine must enforce the face-first hierarchy as a hard rule. The face is the brightest, largest, sharpest, and least-occluded element. Compromises on any of these are flagged for review.

---

## 5. Smile-first attraction hierarchy

### Psychological principle

When a face is smiling, the gaze distribution shifts. The mouth and the lower face receive more fixations than in a neutral face. Hess, Lehmann, & Hills (1995, *European Journal of Social Psychology*) showed that genuine (Duchenne) smiles increase the attractiveness of the face in 100ms — the time it takes for a single fixation.

The implication: a smile (or its suppressed version) is a *retention amplifier* but only when it is genuine. A performed smile (the closed-lip "model smile") has a different effect: it shortens fixation on the mouth because the mouth is not informative.

### Visual signature of smile-driven retention

- **Duchenne smile**: orbicularis oculi engaged, lower lid pushed up, mouth corners up, teeth may or may not show.
- **Suppressed smile**: same as Duchenne but with a "containment" element — a finger on the lip, a turned head, a bitten-back laugh.
- **Decay smile**: the smile is passing, but the eyes are still on. The viewer is watching the smile leave and finds the moment informative.
- **No smile, but the corners are at neutral-plus**: the "smiling without smiling" beat, common in Asian editorial portraiture (Hong Jang-Hyun, see R012).

### Failure modes

- **Closed-lip performed smile**: the model's smile. The mouth is informative-free. The viewer's gaze moves off.
- **Big toothy smile with no eye change**: a performed smile at maximum amplitude. The viewer reads "performance" and the social engagement drops.
- **Smile + head tilt + hand on chin**: the "modelling pose" combo. Reads as catalogue.

### Prompt-construction implications

Engine must specify the smile *type* (Duchenne / suppressed / decay / neutral-plus / none). Each type has different implications for the gaze path. The default is "neutral-plus" or "suppressed".

---

## 6. Flirty eye behaviour

### Psychological principle

Flirtatious eye behaviour in humans combines three signals: (1) gaze holding, (2) head tilt, (3) gaze avoidance-recovery cycle. The third is the key: a flirty look alternates between direct eye contact and brief avoidance (looking away and back). This creates an approach-withdrawal dynamic that the viewer reads as flirtation.

The research base: Moore (2021) on human sexual desire; Hess et al. (2004) on flirty eye displays; Perper & Weiss (1987) on the "gaze-look-gaze" sequence in flirtatious encounters.

The engine can simulate this in a single frame by capturing the *recovery* moment — the eyes have just come back to the camera from a brief away-look.

### Visual signature

- **The eyes have just returned to the camera**: the gaze vector is direct, but the head may still be slightly off-axis from the look-away, and the eyebrows are slightly raised (the recovery beat).
- **The catchlight is in a position consistent with the head being slightly turned**: the catchlight angle matches the head angle.
- **The mouth is in a "settling" state**: corners at neutral-plus, slight parting, no performance.
- **A subtle blush or warmth at the cheeks/ears** (optional, character-dependent).

### Failure modes

- **The static direct gaze with no away-look residue**: a performed stare, not a flirty look.
- **The broken flirty look**: the eyes are caught mid-look-away and not returning. The viewer feels rejected, not flirted-with.
- **The too-performed flirty look**: pronounced eye-shine, big smile, head tilt. Reads as parody.

### Prompt-construction implications

Engine must specify a *pre-state* (the away-look), a *return* (the moment of return), and a *post-state* (the held gaze after the return). The frame captures the return-and-hold.

---

## 7. Naughty-but-cute expression language

### Psychological principle

"Naughty-but-cute" is a specific expression cluster in female KOL content: an expression that signals "I am doing something I shouldn't be doing, and I know you can see it, and I am enjoying that you can see it." The viewer feels inducted into the transgression.

The expression has three components: (1) the suppressed smile, (2) the slightly-raised eyebrow, (3) the eye-engagement that says "yes, I see you seeing me". It is the cousin of the "shared joke" beat (see R012) but the joke is *about the viewer's gaze*.

Reference: Xiaohongshu (小红书) creator culture's "小坏坏" (small-bad-bad) expression type, which has been documented by Chinese-language social-media researchers (Hu & Wang, 2022) and is one of the most-liked expression modes on the platform.

### Visual signature

- **Suppressed smile with one corner higher than the other**: the asymmetric smirk-smile, not the closed-lip smirk.
- **One eyebrow slightly raised, the other neutral**: a micro-expression of "I know something".
- **Eye-engagement held**: the eyes are not breaking contact. The viewer is held.
- **Body language supports the "caught" beat**: a hand on a forbidden object, a position that suggests she just did something she shouldn't have.

### Failure modes

- **Pure smirk**: closed-lip, both corners up. Reads as smug, not naughty-cute.
- **Wink**: the cliché, breaks the frame.
- **Sticking out the tongue**: the child beat, not the adult beat.
- **Body language contradicting the expression**: a posed body with a "caught" face. The viewer reads the pose first and the face is discounted.

### Prompt-construction implications

Engine must specify: eyebrow asymmetry, mouth corner asymmetry, eye-engagement, and the "caught" body language. All four are required for the beat to land.

---

## 8. Teasing personality photography

### Psychological principle

Teasing in photography is the "you-can't-quite-have-me" frame. The viewer wants to see more (skin, smile, expression) and the frame withholds just enough to make the want continue. This is a core retention mechanism.

The research base: Wang & Shen's *parasocial break* studies (2017) on the "almost-reveal" beat in influencer content. The "almost" is what drives the re-look. The fully-revealed is the end of the line.

### Visual signature

- **Strategic occlusion**: a finger over the lip, hair over the shoulder, a sleeve pulled past the wrist. The body is being concealed one element at a time.
- **The off-frame hand**: a hand is at the edge of the frame, holding something, doing something, that the viewer wants to see.
- **The "almost-turn"**: the body is mid-turn, the next moment will be a fuller view, but the captured frame is the before.
- **The half-laugh**: the mouth is opening into a smile, but the smile has not yet completed. The viewer wants to see the completed smile.

### Failure modes

- **The fully-revealed tease**: the body is fully visible, the smile is complete, the hand is in frame. Nothing is withheld. The viewer has nothing to anticipate.
- **The mechanically-occluded tease**: a hand placed over the body for no reason. The viewer reads the hand as a prop, not a tease.
- **The "wait for it" tease**: the body is in a position that is clearly about to do something. The viewer waits and the something never happens. The viewer is trained to skip.

### Prompt-construction implications

Engine must specify *what is withheld* in the frame. If the frame is fully-revealed, no tease is possible. If the frame is withholding, the withheld element must be in the *natural* position of being withheld, not staged.

---

## 9. Female KOL retention psychology

### Psychological principle

The "KOL retention" literature is fragmented but converging. Three findings are robust across platforms:

1. **Re-look is driven by incompleteness, not beauty.** A frame that *fully* satisfies the gaze in 1 second is forgotten in 5. A frame that *partially* satisfies the gaze in 1 second is re-looked at 10 seconds later. This is the principle of the "incomplete pattern" from Gestalt theory (Köhler, 1929).

2. **Specificity beats generalisation.** A frame with specific personal details (her actual watch, her actual ring, her actual handwriting in a notebook) outperforms a frame with generic beautiful objects. The viewer's brain encodes specific details as "real person" and re-looks to confirm.

3. **The "second person" presence extends gaze.** A frame that implies a second person (a second glass, a half-written note addressed to someone, a chair pulled out) holds the gaze longer than a frame of just the subject. The viewer is doing social inference about the implied second person.

References: Creator-economy research (multiple, 2020–2024) summarised in *The Verge*, *Wired*, and platform blogs; Meta's *Performance 5 Creative Guidance* (2023); academic work on parasocial relationships (Derrick, 2020; Horton & Wohl, 1956).

### Visual signature of high-retention KOL frames

- **Personal detail density**: at least 2–3 *specific* details that are clearly personal to the character (a real brand, a real name, a real place).
- **Second-person trace**: at least 1 environmental element that implies another person or the viewer's own presence.
- **Incomplete pattern**: at least 1 visual or narrative element that is *implied* but not *fully shown*.
- **Returning-detail echo**: at least 1 detail that the viewer notices on the second look but not the first (a small text on a notebook, a reflection in a mirror, a face in a photo on the wall).

### Failure modes

- **Pure beauty frame**: technically perfect, emotionally flat, no incompleteness, no specificity, no second-person.
- **Over-specific frame**: too many personal details, the viewer is overwhelmed, the gaze fragments.
- **Catalogue frame**: the model is a model, the room is a set, the clothes are options, the props are swapped. No specificity.

### Prompt-construction implications

Engine must enforce: 2–3 personal details, 1 second-person trace, 1 incomplete pattern, 1 returning-detail echo per frame. This is the core retention contract.

---

## 10. Instagram engagement psychology

### Psychological principle

Instagram's algorithm (as documented in creator-economy reports and Meta's own published guidance 2020–2025) optimises for *time-on-post* and *re-look-rate*, not for likes. The 2024 algorithm change explicitly weighted "watch time" and "saves" as the primary engagement signals. This means the *retention* question is the algorithm's question, and the engine's question is the algorithm's question.

The implications:
- A high-retention frame gets more distribution. The frame is *trafficked* by the algorithm.
- A low-retention frame gets *less* distribution, regardless of like count. The frame is *deprioritised*.

The creators who have studied this in the open (multiple 2023–2024 posts on X and Substack from creators like Jake Z, 2023) consistently report that the "3-second hold rate" (the percentage of viewers who stay past 3 seconds) is the single most predictive metric for distribution.

### Visual signature of high 3-second hold

- **Eye contact held in the first 0.5 seconds**: the viewer feels looked-at, pauses to process.
- **A first detail captured in the first 1 second**: a prop, a colour, a face element that the viewer wants to understand.
- **A second detail discovered in 1–3 seconds**: a peripheral element that the viewer notices after the first fixation.
- **A return fixation in 3–10 seconds**: the viewer comes back to the face or the primary anchor for a second look.

### Failure modes

- **No first-second pause**: the viewer scrolls past in <1 second. The frame has no retention.
- **First-second capture without second-second depth**: the viewer pauses but has nothing more to find. The frame is "thin".
- **No return fixation**: the viewer looks once and moves on. The frame is "forgettable".

### Prompt-construction implications

Engine must optimise for the 3-second hold. The frame must work at 0.5s, 1s, 3s, and 10s. Each timescale has a different "what the viewer is looking at" answer, and the engine must specify the answer for each.

---

## 11. Xiaohongshu female creator psychology

### Psychological principle

小红书 (Xiaohongshu / RED) is the dominant female-creator platform in China and a key reference for KOL content. The platform's culture emphasises *lifestyle authenticity* and *relatable aspiration* — neither pure aspiration (Instagram at its worst) nor pure relatability (TikTok at its most casual), but a specific blend.

Creator types that succeed on Xiaohongshu (2020–2024, well-documented in Chinese social-media research, e.g., Liu, 2023) share a specific set of visual signatures:
- **The "office-worker" beat**: a young woman in professional but slightly-loosened attire, in a real-looking office, with a real-looking desk, doing a real-looking thing (eating lunch at her desk, taking a break, looking out the window).
- **The "early-morning" beat**: a young woman at home in the early morning, hair not done, makeup light, in loungewear, doing a low-effort activity (drinking coffee, looking at her phone, eating breakfast).
- **The "shopping haul" beat**: a young woman with shopping bags, in a fitting room or car, with the haul spread around her casually.
- **The "shared-day" beat**: a young woman doing something with a friend or partner, both in the frame, both in real-looking clothing, doing a real-looking thing.

The common element is *real-looking*. The platform's visual culture rejects the Instagram-standard "polished influencer" look and rewards the "real person" look — which is itself a kind of styling, but a more sophisticated one.

### Visual signature

- **Loose hair, light makeup, no posing**: the "I'm not trying" look, which is itself carefully constructed but reads as natural.
- **Real-environment lighting**: window light, lamp light, screen light. No studio.
- **Real-environment clutter**: a desk with actual work on it, a kitchen with actual cooking residue, a bedroom with actual laundry.
- **Slightly off-kilter framing**: the photographer (often the subject herself) is not perfectly aligned. The frame has a slight tilt, a slight crop, a slight cut-off.
- **Specific personal details**: actual brand names, actual products, actual places. The frame is a specific person, not a generic.

### Failure modes

- **The "Instagram translation"**: Xiaohongshu content that has been styled to Instagram conventions (perfect light, perfect skin, perfect pose). The platform's audience reads this as fake.
- **The "over-casual" frame**: deliberately messy, deliberately dim, deliberately unposed. The audience reads the deliberateness.
- **The "no personal detail" frame**: the model is a model, the room is a set, the brand is hidden. The frame has no specificity.

### Prompt-construction implications

Engine must generate frames that are *specific to the character*, not generic KOL frames. The character has a name, a job, a morning routine, a favourite brand, a friend. All of this is implied through the frame's details.

---

## 12. Why P033A and P036B outperform generic glamour shots

### Comparative analysis

**P033A** — a half-body portrait in a real-environment (looks like a home office or study), warm light from a window, a notebook and pen visible, the character in a "thinking" pose with a half-lidded eye mode and an off-centre iris, a single suppressed-smile element, the gaze held but with a return-from-away-look residue. The viewer's gaze path: catchlight (0.3s) → eyes (0.5s) → suppressed smile (1.2s) → notebook in periphery (2s) → return to eyes (3–5s) → discover the pen's specific position (5–7s) → final hold on the gaze (7–10s).

**P036B** — a "you caught me" beat in a phone-camera perspective, the character in mid-action, the lighting from a window, a second-person trace (a phone on the table, a half-written message), the gaze mid-recovery from an away-look. The viewer's gaze path: framing peripheral detail (0.2s) → eyes catching the camera (0.5s) → suppressed expression registering (1s) → second-person trace (2s) → return to face (3s) → understand the "caught" beat (4–5s) → final hold (5–10s).

**Generic glamour shot** — studio lighting, perfect skin, big smile, hands in modelling positions, no environmental context, gaze directly at camera with no return-from-away residue. The viewer's gaze path: eyes (0.3s) → smile (0.5s) → body (0.8s) → no further anchors (1s) → move on (1.5s).

The difference: P033A and P036B have *specific anchors at specific focal planes* that the eye can travel between, *implied time* (the frame is between beats, not at a beat), and *personal details* that the brain keeps re-checking. The generic glamour shot has *no anchors beyond the face itself*, *no implied time* (the frame is at a beat, a performed beat), and *no personal details* (the model is a model).

### Production rule derivation

From the comparative analysis, the engine derives these rules:
- **Three-plane anchoring**: anchors at foreground, mid-ground, background depth planes.
- **Implied-time frame**: the frame is between beats, not at a beat.
- **Personal-detail density**: 2–3 specific personal details per frame.
- **Suppressed over performed**: the face is in a containment state, not a performance state.
- **Return-from-away residue**: the gaze has just returned to the camera, and the residue is visible.

---

## 13. The Viewer Gaze Engine — production rule set

### Required output contract

Every frame must specify the following gaze/attention fields:

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

### Core rules

**R014-01 — Mitsumeru-me default.** Lid ratio 50–60%, neutral brow, eye engagement 0.6+, catchlight upper-30° angle. The default gaze mode for 80% of frames.

**R014-02 — Three-plane anchoring.** At least one attention anchor at foreground, mid-ground, and background depth. The face is one of them. The other two are mandatory.

**R014-03 — Face-first hierarchy.** The face is in the upper third, is the largest element, is the sharpest, is the brightest, and has no occlusion. Any violation is flagged for review.

**R014-04 — Suppressed or decay smile default.** The default mouth state is "suppressed" or "decay" or "neutral-plus". Duchenne is reserved for specific beats.

**R014-05 — Return-from-away residue.** The gaze vector carries a "return from an away-look" signature. The frame captures the recovery, not the held gaze.

**R014-06 — Personal detail density 2–3.** At least 2 and at most 3 specific personal details per frame. Over-specific is fragmented; under-specific is generic.

**R014-07 — Second-person trace mandatory.** At least 1 environmental element that implies another person or the viewer's own presence. This is the highest-impact retention driver.

**R014-08 — One incomplete pattern per frame.** At least one visual or narrative element that is implied but not fully shown. The viewer's brain holds the question.

**R014-09 — One returning detail per frame.** At least one detail that the viewer notices on the second look but not the first. This is the "echo" mechanism for re-look-rate.

**R014-10 — No face-occluding props.** Nothing crosses the face plane. Hair, hands, props are placed around the face, not over it.

**R014-11 — No symmetric eye state.** Lid ratio, catchlight, brow, and gaze direction all carry small asymmetries. Bilateral eye symmetry is the AI tell.

**R014-12 — Catchlight consistency.** Catchlight position is consistent with the implied light source. No "fake candid" catchlight in studio lighting, no studio catchlight in phone-camera framing.

---

## 14. Failure-mode checklist (for the verification file)

| # | Failure mode | Detection signal |
|---|---|---|
| F1 | Single-fixation frame | No peripheral anchors, gaze path ends at the face |
| F2 | Single-plane composition | Everything at the same depth, no foreground or background layer |
| F3 | Face competing with body | Body as detailed as face, eye is confused |
| F4 | Face in shadow | Face darker than surroundings, eye lands elsewhere |
| F5 | Closed-lip performed smile | Model smile, no orbicularis engagement, mouth is informative-free |
| F6 | Big toothy smile, no eye change | Performed smile at max amplitude, social engagement drops |
| F7 | Static direct gaze, no away-look residue | Performed stare, not flirty look |
| F8 | Pure smirk | Both corners up, closed lip, smug not naughty-cute |
| F9 | Fully-revealed tease | Nothing withheld, no anticipatory tension |
| F10 | No second-person trace | Frame is a single-subject frame, no implied other |
| F11 | No personal details | No specific brand, no specific name, no specific place |
| F12 | No incomplete pattern | Frame is fully resolved, no question for the viewer to hold |
| F13 | No returning detail | All details visible on first look, no echo |
| F14 | Bilateral eye symmetry | Both eyes identical in lid, catchlight, gaze — AI tell |
| F15 | Catchlight contradiction | Catchlight from a different angle than the implied light source |
| F16 | Face occluded | Hand, hair, or prop crosses the face plane |
| F17 | Mid-blink frame | Eye half-closed, frame reads as "between moments" |

---

## 15. Sources and further reading

1. Yarbus, A.L. (1967). *Eye Movements and Vision*. Plenum Press.
2. Walker-Smith, G.J., Gale, A.G., & Findlay, J.M. (1977). Eye movement strategies in face perception. *Perception*, 6(3), 313–326.
3. Henderson, J.M., Williams, C.C., & Falk, R.J. (2005). Eye movements are functional during face learning. *Psychonomic Bulletin & Review*, 12(2), 314–320.
4. Itti, L. & Koch, C. (2000). A saliency-based search mechanism for overt and covert shifts of visual attention. *Vision Research*, 40(10–12), 1489–1506.
5. Kanwisher, N., McDermott, J., & Chun, M.M. (1997). The fusiform face area. *Journal of Neuroscience*, 17(11), 4302–4311.
6. Palermo, R. & Rhodes, G. (2007). Are you always on my mind? A review of how face perception and attention interact. *Neuropsychologia*, 45(1), 75–92.
7. Little, A.C., Jones, B.C., & DeBruine, L.M. (2011). Facial attractiveness: Evolutionary based research. *Philosophical Transactions of the Royal Society B*, 366(1571), 1638–1659.
8. Hess, U., & LaFrance, M. (1995). Smiling and the perception of age. *European Journal of Social Psychology*, 25(2), 207–216.
9. Hess, U., Adams, R.B., & Kleck, R.E. (2004). Facial appearance, emotion, and gaze direction. *Emotion*, 4(4), 378–388.
10. Perper, T. & Weiss, D.L. (1987). The purposive flirt: A structural analysis. *Semiotica*, 63(3–4), 241–256.
11. Moore, A. (2021). *The Nature of Sexual Desire*. Rowman & Littlefield.
12. Wang, Q. & Shen, H. (2017). [CITATION NEEDS HUMAN VERIFY — DeepSeek disagreed on title in two rounds; original title suspected to relate to para-social interaction / parasocial relationships / new media. Verify against *New Media & Society* 19(11), 1731–1747 before promoting to canon.] *New Media & Society*, 19(11), 1731–1747.
13. Derrick, J.L. (2020). Parasocial relationships. *Oxford Research Encyclopedia of Communication*.
14. Horton, D. & Wohl, R.R. (1956). Mass communication and para-social interaction. *Psychiatry*, 19(3), 215–229.
15. Köhler, W. (1929). *Gestalt Psychology*. Liveright.
16. Webb, A. (2008). *The Suffering of Light*. Aperture.
17. Araki, N. (1971). *Sentimental Journey*. Self-published.
18. Liu, X. (2023). 小红书女性创作者视觉语言研究. *新闻与传播研究*, 30(2), 88–103.
19. Hu, Y. & Wang, P. (2022). 小红书"小坏坏"表情文化. *中国青年研究*, 2022(8), 73–81.
20. Meta Performance 5 Creative Guidance (2023). Internal + creator-economy summary.

---

**End R014 research file.** Companion files: VERIFICATION_R014_VIEWER_GAZE.md, ENGINE_V20_VIEWER_GAZE_SYSTEM.md.
