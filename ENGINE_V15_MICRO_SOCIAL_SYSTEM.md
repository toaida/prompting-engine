---
name: ENGINE_V15_MICRO_SOCIAL_SYSTEM
description: Micro Social Interaction System for authentic interpersonal moments
areas: AREA 09
version: V15
status: READY FOR INTEGRATION
---

# ENGINE_V15_MICRO_SOCIAL_SYSTEM

## Core Philosophy

Micro social = the tiny, involuntary, real-time adjustments humans make toward each other. A hand on a shoulder, a glance, adjusting someone's hair, sharing a bite — moments so small they rarely make it into photography. These micro-interactions are the "glue" that makes subjects look like they're in relationship, not just adjacent.

---

## MICRO_SOCIAL_INTERACTION_LIBRARY

### 5 Interaction Categories

| Category | Type | Description | Token |
|----------|------|-------------|-------|
| A | PRACTICAL_ADJUSTMENT | Functional touch: towel, hair, clothing | [PRACTICAL_ADJUST] |
| B | PLAYFUL_TOUCH | Light, brief, consensual: splash, poke, tickle | [PLAYFUL_TOUCH] |
| C | INTIMATE_GESTURE | Affectionate: hug, lean, hold | [INTIMATE_GESTURE] |
| D | SOCIAL_GESTURE | Handshake, wave, high-five, fist bump | [SOCIAL_GESTURE] |
| E | ENVIRONMENTAL_SHARE | Passing objects, pointing, directing attention | [ENV_SHARE] |

---

## INTERRUPTION_ACTION_SYSTEM

### 5 Patterns

| Pattern | What Happens | Visual Signature | Token |
|---------|--------------|------------------|-------|
| B1 | TUCKING_BEHIND_EAR | Fixer tucks strand, brief ear contact | [EAR_TUCK] |
| B2 | HAIR_FLIP_ASSIST | Hand through hair, gravity assist | [HAIR_FLIP_ASSIST] |
| B3 | SHOULDER_TAP | Attention redirect, light touch | [SHOULDER_TAP] |
| B4 | HAND_HOLD_ADJUST | Re-grasping, repositioning hands | [HAND_ADJUST] |
| B5 | SPATIAL_REDIRECT | Hand pointing, body angle shift | [SPATIAL_REDIRECT] |

### Candid Reaction Grammar (6 Rules)

1. **Reaction precedes recognition** — Subject reacts to person before reacting to camera
2. **Gaze vector indicates relationship** — Who subject looks at = who's important in frame
3. **Touch = relationship marker** — Who touches whom, duration, intent
4. **Body orientation follows social hierarchy** — Subject turns toward higher-status person
5. **Expression matching** — Subject's expression mirrors interaction type
6. **Environmental accommodation** — Subjects use environment as social prop

---

## Prompt Grammar

```
[micro_interaction]:[category]_
[interruption_pattern]:[if_applicable]_
[candid_reaction]:[rule_1-6_applied]_
[gaze_vector]:_[target]_
[touch_duration]:_[brief_prolonged]_
[relationship_marker]:_[type]
```

**Examples:**
```
[PRACTICAL_ADJUST]_micro_social
interruption_pattern:[EAR_TUCK]_hair_strand_behind_ear
candid_reaction:subject_looks_at_friend_not_camera_first
gaze_vector:friend_center_camera_right
touch_duration:brief_under_1_second
relationship_marker:sister_comfortable_intimate

[PLAYFUL_TOUCH]_micro_social
interruption_pattern:[SHOULDER_TAP]_attention_redirect_laugh_follows
candid_reaction:expression_mirrors_social_gesture
gaze_vector:friend_center_camera_left
touch_duration:brief_flash_tap
relationship_marker:close_friend_spontaneous
```

---

## 76 Core Tokens

**Practical:** [TOWEL_ADJUST] [HAIR_TUCK] [COLLAR_FIX] [SHOULDER_BRUSH] [ARM_CLEAR]
**Playful:** [LIGHT_TAP] [GENTLE_POKE] [TICKLE_RESPONSE] [SPLASH_MOMENT] [HAIR_RUFFLE]
**Intimate:** [LEAN_AGAINST] [ARM_AROUND] [HAND_HOLD] [FOREHEAD_TOUCH] [BACK_RUB]
**Social:** [WAVE] [HIGH_FIVE] [FIST_BUMP] [HANDSHAKE] [POINT_SHARE]
**Environmental:** [PASS_BOTTLE] [DIRECT_ATTENTION] [REACH_OVER] [SHARE_ITEM] [SPATIAL_GESTURE]

**Reaction Tokens:** [GENUINE_LAUGH] [SURPRISE_BLINK] [CONFUSED_FURROW] [HAPPY_SCRUNCH] [CONTENT_SOFT] [INTERESTED_FORWARD]

---

## HK-Specific Content

- **Tea Restaurant Sharing**: Chopstick food sharing, tea pouring, menu pointing
- **MTR Crowding**: Accidental touch, spatial negotiation, ignore culture
- **Karaoke Close**: Micro-social amplified by confined space
- **BBQ Social**: Food sharing, fire proximity, casual intimacy

**HK Tokens:** [TEA_RESTAURANT_SHARE] [MTR_CROWD_TOUCH] [KARAOKE_CLOSE] [BBQ_SHARE]

---

## Moderation Warnings

⚠ **COERCIVE = BAD**: Subject visibly flinching, holding breath, frozen, eyes averted
⚠ **ACCEPTABLE = GOOD**: Subject initiates or readily accepts, brief functional, mutual consent visible
⚠ Practical adjustments: brief, functional, not sensual
⚠ Never capture subjects in genuinely distressed states

---

## Distribution Targets

- Category A (Practical): 30% — most common in HK social contexts
- Category B (Playful): 20% — friends, casual relationships
- Category C (Intimate): 25% — couples, close friends
- Category D (Social): 15% — greeting, farewell moments
- Category E (Environmental): 10% — active social scenes

---

## Cross-References

- Complements SOCIAL_CAMERA (relationship dynamic drives interaction choice)
- Complements FACE_FIRST (micro social triggers face expressions)
- Complements CONTINUITY_PERSISTENCE (repeated interactions = relationship signal)

---

*Module: ENGINE_V15_MICRO_SOCIAL_SYSTEM.md*
*Source: AREA 09 — V15 Research*
*Status: READY FOR INTEGRATION*
