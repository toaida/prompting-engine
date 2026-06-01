---
name: ENGINE_V20_CAMERA_RELATIONSHIP_SYSTEM
description: Runtime system for subject-photographer relationship, camera recognition, and social-photo behavior.
areas: CAMERA / EXPRESSION / SOCIAL PHOTOGRAPHY
version: V20
status: ACTIVE — AUTO-MERGED
---

# ENGINE_V20_CAMERA_RELATIONSHIP_SYSTEM

## Core Philosophy

The camera is not neutral. Every image carries a relationship between subject and photographer.

```
Bad AI: subject performs at an abstract camera.
Good V20: subject responds to a specific person or device in a specific social context.
```

The engine chooses camera relationship before facial expression. Expression without camera relationship becomes model posing.

---

## Camera Awareness Spectrum

| Level | Token | Meaning | Use |
|---|---|---|---|
| 0 | `SIMULATED_CAMERA_OBLIVIOUS` | subject performs unawareness | documentary, street, private moment |
| 1 | `CAMERA_PERIPHERAL` | knows camera exists but continues activity | friend-shot, cafe, MTR |
| 2 | `CAMERA_REACTIVE` | just noticed camera | highest authenticity expression window |
| 3 | `CAMERA_ENGAGED` | interacts with photographer through lens | warm, flirty, personal |
| 4 | `CAMERA_PERFORMING` | intentionally poses | editorial, influencer, staged candid |

**Important:** In AI images Level 0 is simulated, not genuine. Prompt the visible signature of unawareness: continuous action, no lens recognition, activity evidence.

---

## Photographer Trust Matrix

```
                  TRUSTED FRIEND / PARTNER        STRANGER / LOW TRUST
OBLIVIOUS         vulnerable, relaxed              documentary, guarded if noticed
PERIPHERAL        comfortable ignoring             aware but defensive
REACTIVE          warm or playful recognition      startle, suspicion, guardedness
ENGAGED           intimate connection              defensive performance
PERFORMING        playful staged authenticity      public influencer mask
```

Always pair awareness level with photographer type.

---

## Recognition Moment Signatures

AI cannot generate milliseconds. It can generate the **visual residue** of a transition.

### `WARM_RECOGNITION`
```
eyes just found the phone camera, warmth arriving before the smile finishes,
old expression still visible at mouth corners
```

### `PLAYFUL_RECOGNITION`
```
noticed the friend filming, one eyebrow lifting, mouth pulling into a caught-you smirk,
body still in original action
```

### `SHY_RECOGNITION`
```
quick glance to lens then down, hand almost moving toward face, smile forming but not held
```

### `CONFIDENT_RECOGNITION`
```
eyes meet camera without flinching, expression deepens instead of changing,
body stays relaxed and owned
```

---

## Camera Object Patterns

| Token | Meaning | Prompt Use |
|---|---|---|
| `CAMERA_AS_MIRROR` | phone/camera used to check appearance | eyes on screen, adjusting hair |
| `CAMERA_AS_SHIELD` | device creates safe distance | phone held between subject and viewer |
| `CAMERA_AS_TROPHY` | subject reverses power | phone pointed back at photographer |
| `CAMERA_AS_WITNESS` | camera trusted during vulnerability | emotional moment continues despite camera |
| `CAMERA_FATIGUE` | over-photographed exhaustion | tired eyes, forced smile, closed posture |
| `GROUP_DISTRIBUTED_AWARENESS` | multiple people aware differently | one looks, one ignores, one reacts |

---

## Friend-Shot Runtime Rules

Friend-shot does not mean random candid. It means **the subject's behavior is shaped by trust**.

1. Activity continues after recognition.
2. Expression is in transit, not held.
3. Frame includes small social evidence: friend drink, hand edge, shared table, second bag.
4. Composition is competent but not studio-perfect.
5. Viewer should sense the photographer is a person, not an abstract lens.

---

## Environment Calibration

### MTR / Transit
- Stranger direct gaze is implausible.
- Friend direct gaze is plausible if phone-camera context exists.
- Default: `CAMERA_PERIPHERAL`, phone gaze, pole grip, crowd.

### Cafe / Restaurant
- Most common KOL environment.
- Camera often friend/partner.
- Use mid-conversation, drink/food evidence, not empty table.

### Hotel / Bedroom
- Higher intimacy; avoid default boudoir staging.
- Camera = partner, mirror, or friend getting-ready shot.
- Expression should be underperformed.

### Night Out
- Camera is social; group context matters.
- Laughter, drink, neon, movement; avoid static solo model in street.

---

## Anti-Patterns

- `ABSTRACT_CAMERA`: no photographer implied.
- `FROZEN_SMILE`: held smile with no transition.
- `MODEL_GAZE_IN_CANDID`: fashion gaze pretending to be documentary.
- `PUBLIC_DIRECT_GAZE_NO_CONTEXT`: direct lens in MTR/street without friend/device reason.
- `FAKE_CANDID_STIFFNESS`: pretending unaware but body arranged for lens.
- `NO_HANDS_VISIBLE`: camera relationship usually needs hands, phone, drink, hair, bag.

---

## Production Example

```
CAMERA_REACTIVE friend-shot in small HK cafe, she was looking down at iced milk tea and phone,
then notices her friend taking a photo; eyes have just found the lens, smile not fully formed,
one hand still around the cold cup, condensation visible, friend's second drink half visible at frame edge,
not a model stare, not a held smile
```
