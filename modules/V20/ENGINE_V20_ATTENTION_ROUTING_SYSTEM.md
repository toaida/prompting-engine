---
name: ENGINE_V20_ATTENTION_ROUTING_SYSTEM
description: Runtime system for viewer attention path, scroll-stop logic, and retention intent.
areas: ATTENTION / VISUAL PRIORITY / PHOTO EXISTENCE
version: V20
status: ACTIVE — AUTO-MERGED
---

# ENGINE_V20_ATTENTION_ROUTING_SYSTEM

## Core Philosophy

Eye flow is where the viewer looks. Attention routing is **why the viewer cares enough to keep looking**.

Every generated image must answer:

```
What does the viewer notice first?
Why does the eye stop there?
What unresolved question makes the viewer keep looking?
What memory trace remains after 5 seconds?
```

V20 corrects the old "pretty subject = attention" assumption. Beauty can capture glance, but **narrative tension, photographer context, and social meaning** hold attention.

---

## Runtime Attention Window

```
0.0-0.1s  PRE-ATTENTIVE CAPTURE
          Motion, contrast edge, luminance spike, face detection.

0.1-0.5s  ATTENTION CAPTURE
          Eye lands on strongest salience point: face, motion, light, object.

0.5-1.5s  ATTENTION HOLD
          Viewer asks: "What is happening? Why was this taken?"

1.5-3.0s  ENGAGEMENT
          Viewer builds a story: photographer, subject, relationship, place.

3.0-5.0s  MEANING RESOLUTION
          Viewer decides if the image is memorable, shareable, or skippable.

5.0s+     RETENTION
          Image leaves a mood, identity, place, or desire trace.
```

**Critical Correction:** AI images usually fail at ATTENTION HOLD, not initial capture. The first glance may work; the second glance finds no reason.

---

## Attention Anchor Hierarchy

Use this as runtime priority, not rigid law:

1. **Motion / High Contrast Edge** — strongest in peripheral vision.
2. **Face / Eyes / Skin Luminance** — strongest once the face is foveal.
3. **Narrative Object** — phone, drink, bag, food, mirror, window.
4. **Light Source / Brightness Spike** — especially at night.
5. **Body Language Read** — posture that tells story.
6. **Environment / HK Locality** — context that confirms place and identity.

### Exceptions

- If face is in shadow, body language or object may lead.
- If phone screen is bright, it may lead before face.
- If environment is the story, first anchor can be sign/street/window before subject.
- If direct eye contact exists, it dominates unless intentionally underlit or occluded.

---

## Attention Path Types

### A. FACE-DOMINANT PATH
Use when expression is the payload.

```
FACE → EYES → MICRO-EXPRESSION → MEMORY
```

Prompt fragment:
```
face is the sharpest emotional anchor, eyes carrying the reason this photo exists,
background soft and secondary, no brighter object competing with her expression
```

### B. OBJECT-TO-FACE PATH
Use for candid/social realism.

```
OBJECT → HAND → BODY ORIENTATION → FACE
```

Prompt fragment:
```
eye starts at the phone screen at frame edge, travels through her hand and tilted
shoulder to her face, she is reacting to something on the phone rather than posing
```

### C. ENVIRONMENT-TO-SUBJECT PATH
Use for HK local, street, MTR, night, market.

```
HK SIGNIFIER → BODY POSITION → FACE / GAZE
```

Prompt fragment:
```
traditional Chinese street sign and wet pavement pull attention first, then her
crossbody bag and fast walking posture lead the eye to her face
```

### D. BODY-LANGUAGE-READ PATH
Use when posture is the story.

```
GROUND CONTACT / LEAN / WEIGHT SHIFT → ACTION REASON → FACE
```

Prompt fragment:
```
attention begins at her crouched balance and hand reaching toward the dropped
Octopus card, then rises to her amused face noticing the friend photographing her
```

### E. LIGHT-SOURCE PATH
Use at night.

```
VISIBLE LIGHT SOURCE → COLORED SKIN / REFLECTION → FACE
```

Prompt fragment:
```
pink LED sign at left is the first visual anchor, its color falling across one side
of her face while the opposite side falls into warm street-lamp shadow
```

---

## Scroll-Stopping Mechanisms

| Token | Use When | Prompt Cause |
|---|---|---|
| `NARRATIVE_GAP` | Something just happened or is off-frame | gaze, turn, laughter, interruption |
| `INTERRUPTED_ACTION` | Body is mid-transition | mid-sit, mid-step, mid-reach |
| `GAZE_TETHER` | Looking away with visible reason | phone, friend, window, food, view |
| `PHOTOGRAPHER_REASON` | Viewer senses who took it and why | friend, partner, stranger, self |
| `SOCIAL_LENS` | Photo carries a relationship | friend-shot, partner-shot, group-shot |
| `ENVY_FREEDOM` | Viewer wants her moment/life | beach, travel, night, spontaneous |
| `ENVY_CONNECTION` | Viewer wants her social world | friends, shared drinks, laughter |
| `FRAME_WITHIN_FRAME` | Secondary frame deepens attention | mirror, window, phone, doorway |

---

## Photographer's Lens Rule

Every strong photo implies a photographer with intention.

```
Photographer was [distance] away, at [angle], captured her [timing]
because [moment reason].
```

Examples:

```
friend was close enough to catch her noticing the camera, eye-level phone angle,
photo taken because she laughed before she could pose
```

```
partner-shot distance, slightly above bed height, captured while she checked her
phone in morning light, not a model pose
```

---

## Platform Calibration

- **Instagram:** face or high contrast must work in top half; 0.5s decision.
- **TikTok cover:** motion implication beats static beauty; 0.3s decision.
- **X/Twitter:** contrast and oddness matter; image competes with text.
- **Xiaohongshu:** social proof, lifestyle clues, product/place usefulness matter.
- **Photobook:** slower gaze; environment and emotional residue can lead.

---

## Anti-Patterns

- `NO_REASON_TO_LOOK`: beautiful subject, no narrative.
- `TOO_MANY_ANCHORS`: face, phone, neon, legs, sign all fight equally.
- `UNTETHERED_GAZE`: looking away with no visible reason.
- `OUTPUT_LABEL_TOKEN`: using "high retention" as prompt instead of mechanism.
- `CULTURAL_MISFIRE`: Western gaze logic applied to HK/XHS context.
- `ATTENTION_FATIGUE`: same direct smile / phone gaze / neon path repeated every image.

---

## Production Example

```
HK night street friend-shot, attention path begins at wet pavement reflecting red taxi lights,
travels to her white sneakers mid-step, crossbody bag bouncing, then to her face as she turns
because her friend called her name; eyes just found the phone camera, expression between
annoyed and laughing, Chinese LED signs visible but not brighter than her face, no static pose
```
