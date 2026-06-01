---
name: ENGINE_V20_BODY_LANGUAGE_ATTRACTION_SYSTEM
description: Runtime system converting poses into action-justified, physically plausible body language.
areas: BODY / POSTURE / ATTRACTION / ACTION JUSTIFICATION
version: V20
status: ACTIVE — AUTO-MERGED
---

# ENGINE_V20_BODY_LANGUAGE_ATTRACTION_SYSTEM

## Core Philosophy

Attractive body language is not exposure. It is **confidence expressed through physically believable posture in a real situation**.

Every body position must answer:

```
Why is her body here?
Where is her weight?
What action caused this posture?
What will her body do next?
```

---

## Runtime Frequency Reality Check

DeepSeek verification corrected the research bias:

```
Real KOL frequency estimate:
70% standing / phone-mediated posture
20% cafe or restaurant sitting
5% walking / transit movement
5% ground-level posture
```

Ground posture is powerful but rare. Use it only when environment/action justifies it.

---

## Primary Category: Phone-Mediated Body Language

Phone is the most common body-language driver in HK/KOL content.

| Token | Body Logic | Prompt Use |
|---|---|---|
| `PHONE_DOWN_GAZE` | neck flexion, shoulders slightly rounded | transit, cafe, waiting |
| `PHONE_CHEST_HOLD` | arms folded inward, guarded/social | MTR, crowd, queue |
| `PHONE_ONE_HAND_ASYM` | one hand occupied, one hand free | walking, drink, bag |
| `PHONE_AS_SHIELD_BODY` | object between torso and camera | shy, crowded, guarded |
| `PHONE_SHOWING_FRIEND` | torso leans toward another person | social proof, friend-shot |
| `PHONE_MIRROR_CHECK` | hand/hair adjustment, screen gaze | outfit, makeup, bathroom |

---

## Ground-Level Posture Taxonomy

### `SQUAT_ACTION`
Use only with visible reason: pet, dropped item, low shelf, market goods, beach shells.

Biomechanics:
- heels down OR slightly lifted depending on flexibility
- knees follow foot direction
- calf/thigh compression visible
- hands should stabilize or interact with object

Prompt:
```
squatting to pick up the dropped Octopus card, weight balanced slightly forward,
one heel slightly lifted, hand reaching down, not squatting for the photo
```

### `CROUCH_FORWARD`
Use for interest or inspection.

```
forward crouch to look at something low, weight mid-foot, one hand on knee for balance,
face curious rather than posed
```

### `KNEEL_CONTEXTUAL`
Use carefully. Needs strong context.
- Japan/Korea seiza = formal/respectful
- China/HK kneeling = ceremonial/submissive unless action-justified
- Western = proposal/supplicant/intimate

Safer HK uses: pet interaction, floor dining, organizing luggage, reaching under bed.

### `SEATED_LOW`
Use for beach, curb, stairs, park, waiting, eating.

Subtypes:
- `SEATED_CROSS_LEGGED` — moderate vulnerability, high confidence
- `SEATED_STAIR` — urban waiting / transitional
- `SEATED_LEGS_EXTENDED` — beach / park relaxation
- `SEATED_KNEES_UP` — compact, self-contained, private

### `LEANING_WEIGHT_SHIFT`
Most common public confidence posture.

- wall lean = waiting
- rail lean = view / thought
- table lean = engaged conversation
- hip shift = casual standing
- mid-step shift = movement realism

---

## Transitional State Tokens

| Token | Visual Signature |
|---|---|
| `MID_SIT_TO_STAND` | hands on knees, weight rising |
| `MID_STAND_TO_SIT` | hips lowering, one hand seeking support |
| `MID_TURN` | torso rotates before feet finish |
| `MID_REACH` | arm leads, shoulder follows, body angle reacts |
| `WEIGHT_SHIFTING` | one hip loaded, other leg relaxed |
| `HAND_ADJUSTING` | hair, strap, skirt, shoe, phone, bag |
| `BREATH_VISIBLE_BODY` | shoulders, ribcage, relaxed pause |

---

## Environment-to-Posture Map

| Environment | Best Postures | Avoid |
|---|---|---|
| MTR | standing, pole lean, phone chest hold | crouch/kneel unless dropped item |
| Street market | squat/crouch, bag-forward, item inspection | model stance blocking aisle |
| Cafe | table lean, seated phone, drink hold | empty-hand static posing |
| Beach | seated low, towel shift, wet-hair hand | perfect upright model squat |
| Hotel | bed edge, floor luggage, mirror check | direct bed gaze without reason |
| Night street | walking, wall lean, drink hold | frozen solo neon pose |

---

## Action Justification Rule

```
BODY POSITION + VISIBLE ACTION = believable
BODY POSITION + no action = posed / AI
```

High-believability actions:
- phone use
- eating/drinking
- pet interaction
- adjusting shoe/clothing/bag
- looking at low shelf / market item
- waiting / queueing
- getting up / sitting down

---

## Anti-Patterns

- `STATIC_SQUAT_POSE`: no reason to squat.
- `FLOATING_WEIGHT`: no visible support, tension, or ground shadow.
- `ARMS_FLOATING`: hands have no job.
- `COMFORT_MISMATCH`: face uncomfortable but body supposedly relaxed.
- `GROUND_POSTURE_OVERUSE`: every image uses crouch/kneel.
- `HK_PUBLIC_OVERSEXUALIZATION`: body language too overt for HK street/lifestyle context.

---

## Production Example

```
HK street market, BODY_LANGUAGE: CROUCH_FORWARD because she is checking a tray of phone cases
on a low stall, phone in one hand, other hand reaching, weight on mid-foot, crossbody bag pulled
forward from crowd pressure, face amused as friend photographs her from standing height, not posed
```
