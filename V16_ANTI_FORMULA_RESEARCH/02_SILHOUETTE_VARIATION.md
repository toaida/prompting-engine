# AREA 02: SILHOUETTE VARIATION SYSTEM

## The Problem

Current engine relies on:
- Leaning forward (expose chest, show interest)
- Oversized neckline drift (slipped shoulder, casual seduction)
- Exposed shoulder (half-dressed intimacy)
- Same torso compression logic
- Same "attractiveness geometry" repeating

Real bodies create attraction through **natural use, movement, and spatial negotiation** — not designed poses.

---

## SILHOUETTE_VARIATION_LIBRARY

### Category A: Weight-Bearing Postures (Body in Use)

**Principle:** Body承受 weight = realistic, relatable, non-performative.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| A1: ONE_LEG_SUPPORT | Standing, weight on one leg, hip shift | Asymmetry, natural stance | [ONE_LEG_SUPPORT] |
| A2: HIP_WEIGHT_SHIFT | Hip pushed to one side, shoulders opposite | Classic "model" but real version | [HIP_WEIGHT_SHIFT] |
| A3: KNEE_BEND | Slight knee bend, ready to move | Dynamic potential, not static | [SLIGHT_KNEE_BEND] |
| A4: BACKBEND_LEAN | Lower back arch, chest forward slightly | Natural counterbalance | [NATURAL_BACKBEND] |
| A5: WALL_LEAN | Body against wall, hip or shoulder | Casual weight-bearing | [WALL_LEAN_CASUAL] |
| A6: HAND_ON_WALL | One hand supporting, body angled | Spatial negotiation | [HAND_ON_WALL] |
| A7: SHOULDER_AGAINST_DOOR | Arm up, shoulder to frame | Casual doorway use | [SHOULDER_DOORFRAME] |

### Category B: Seated/Mounted Compression

**Principle:** Sitting creates predictable compression points that reveal body without posing.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| B1: CROSS_LEGGED_COMPACT | Legs crossed, knees high, compact | Thigh compression, small silhouette | [CROSS_LEGGED_COMPACT] |
| B2: KNEE_TO_CHEST | Arms around knees, self-contained | Foetal-adjacent comfort | [KNEES_TO_CHEST] |
| B3: SIDE_SEATED | Legs to side, knees bent | Hip angle, casual | [SIDE_SEATED_CASUAL] |
| B4: STAIR_SITTING | On stairs, different heights | Level variation, leg reveal | [STAIR_SITTING] |
| B5: FLOOR_LOUNGE | Lying or recline, casual floor | Most relaxed state | [FLOOR_LOUNGE_CASUAL] |
| B6: CHAIR_FORWARD | Leaning forward on chair, arms crossed on back | Desk-adjacent, study | [CHAIR_FORWARD_LEAN] |
| B7: LEGS_OVER_ARM | Legs draped over sofa/arm | Lived-in living room | [LEGS_OVER_ARM] |

### Category C: Movement-Based Silhouettes

**Principle:** Body mid-motion = most realistic. Stillness is performance.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| C1: WALKING_MOMENTUM | Mid-stride, natural gait, slight lean | Dynamic, captured candid | [WALKING_CAPTURED] |
| C2: BENDING_TO_PICKUP | Hinge at hips, reaching down | Hip angle, practicality | [BENDING_TO_PICKUP] |
| C3: HAIR_PUSH_BACK | Hand through hair, head back slightly | Neck exposure, motion | [PUSHING_HAIR_BACK] |
| C4: STRETCH_REACHING | Arms up, body elongating | Posture extension | [STRETCH_REACHING_UP] |
| C5: TURNING_AWAY | Mid-turn, profile or back view | Mystery, non-performance | [MID_TURN_AWAY] |
| C6: LOOKING_BACK | Over shoulder, neck twist | Classic but real | [OVER_SHOULDER_GLANCE] |
| C7: ARM_RAISED | One or both arms up, stretching or reaching | Underarm exposure, casual | [ARMS_RAISED_CASUAL] |
| C8: BUCKET_CARRY | Carrying something, both hands occupied | Practical, non-performative | [CARRYING_OBJECT] |

### Category D: Asymmetry Generators

**Principle:** Perfect symmetry = professional/posed. Real bodies are asymmetrical.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| D1: HEAD_TILT | Head to one side, not centered | Asymmetry, casual | [HEAD_TILT_CASUAL] |
| D2: SHOULDER_DROP | One shoulder higher than other | Weight asymmetry | [SHOULDER_DROP] |
| D3: ASYMMETRIC_SQUAT | One leg down, one leg bent | Street/casual squat | [ASYMMETRIC_SQUAT] |
| D4: ARM_HANG | One arm hanging, other doing something | Action asymmetry | [ONE_ARM_HANGING] |
| D5: EYE_LEVEL_TILT | Camera above but head tilted down | Natural counter-angle | [NATURAL_TILT_DOWN] |
| D6: BACKPACK_PULL | Backpack strap pulling one shoulder | Weight imbalance | [BACKPACK_SHOULDER_PULL] |

### Category E: Exhausted/Relaxed States

**Principle:** Tired body = honest body. Exhaustion removes performance.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| E1: SLUMPED_SHOULDERS | Shoulders rounded, chin down | Vulnerability, honesty | [SLUMPED_EXHAUSTED] |
| E2: HAND_ON_NECK | Supporting head, neck exposed | Fatigue + neck display | [HAND_BEHIND_NECK] |
| E3: EYES_CLOSED_RELAX | Eyes closed, face relaxed | Comfortable non-performance | [EYES_CLOSED_RELAXED] |
| E4: MOUTH_PARTIAL | Slightly open, breathing or talking | Real-time moment | [MOUTH_SLIGHTLY_OPEN] |
| E5: HUNCHED_FORWARD | Back curved, protective posture | Self-contained, shy | [HUNCHED_PROTECTIVE] |
| E6: WEIGHT_ON_ELBOW | Reclining on elbow, half-up | Casual recline | [RECLINE_ON_ELBOW] |
| E7: PHONE_CHECK | Looking at phone, chin dropped | Distracted, real | [PHONE_CHECK_POSTURE] |

---

## Body-Weight Realism System

### Principle

Real bodies **accept gravity**. Every body part has weight. Weight creates:
- Compression (skin against fabric, skin against skin)
- Draping (loose fabric falls naturally)
- Exposed lines (under arm, between breasts, neck base)
- Pressure marks (slight indentation from clothing)

### Compression Points

```
COMPRESSION_POINT_LIBRARY:

CP_01: UNDER_BREAST
- When: seated, bending forward, bra band
- Creates: breast separation, under-breast shadow
- Token: [UNDERBREAST_SHADOW]

CP_02: THIGH_GAP_OR_NOT
- When: seated cross-legged, tight skirt/dress
- Creates: thigh contact or gap, depends on body
- Token: [THIGH_CONTACT]

CP_03: ABDOMINAL_FOLD
- When: seated, forward lean, high-waisted clothing
- Creates: natural skin fold, not fat
- Token: [ABDOMINAL_SOFT_FOLD]

CP_04: UNDERARM_SKIN
- When: arm raised, relaxed arm, sleeveless
- Creates: exposed underarm, natural skin
- Token: [UNDERARM_EXPOSED]

CP_05: NECK_BASE_V
- When: head forward, chin down
- Creates: exposed V at neck base
- Token: [NECK_BASE_EXPOSED]

CP_06: SPINE_REVEAL
- When: back arch, leaning forward
- Creates: visible spine line through clothing
- Token: [SPINE_VISUAL_LINE]

CP_07: SHOULDER_BLADE_BULGE
- When: shoulders back, tight top
- Creates: natural shoulder blade prominence
- Token: [SHOULDERBLADE_VISIBLE]
```

---

## Posture Diversity Grammar

```
[primary_posture]:[A1-A7/B1-B7/C1-C8/D1-D6/E1-E7]_
[compression_point]:[CP01-CP07]_
[body_axis]:[upright_forward_side_reclined]_
[weight_distribution]:[balanced_left_heavy_right_heavy]_
[movement_state]:[still_mid-motion_transitioning]
```

**Examples:**
```
[SIDE_SEATED_CASUAL:B3]_posture
compression:[THIGH_CONTACT:CP02]
body_axis:side_tilted
weight_distribution:right_heavy
movement_state:still

[WALKING_CAPTURED:C1]_posture
compression:[UNDERBREAST_SHADOW:CP01]_from_motion
body_axis:forward_lean_slight
weight_distribution:alternating
movement_state:mid-motion
```

---

## HK-Specific Postures (Context-Added)

**Why real:** Specific HK postures from daily life, not generic poses.

| Type | Description | Attraction Mechanism | Token |
|------|-------------|---------------------|-------|
| F1: MTR_HANDRAIL_LEAN | One hand on rail, body tilted, hip shift | Spatial negotiation, casual | [MTR_RAIL_LEAN] |
| F2: QUEUE_WEIGHT_CYCLE | Standing in line, shifting weight leg to leg | Waiting behavior, natural | [QUEUE_WEIGHT_SHIFT] |
| F3: STREET_SQUAT_HK | Squatting on ground, common in street markets | Very HK, casual接地氣 | [STREET_SQUAT_HK] |
| F4: WALL_QUEUE_STAND | Standing against wall while queuing | One leg bent, hip shift | [WALL_QUEUE_STAND] |
| F5: ESCALATOR_STILL | Standing still on escalator, not walking | MTR etiquette, casual | [ESCALATOR_STILL] |

**Note on CP_07 (Shoulder Blade Prominence):** Works best for lean/athletic body types. For other body types, use alternative compression points.

---

## Anti-Repetition Rules

1. **Same posture category (A/B/C/D/E) should not repeat within 3 images**
2. **Same compression point should not repeat within 4 images**
3. **Movement state (C types) should appear at least once every 5 images**
4. **Exhausted states (E types) should appear at least twice per 10-image feed**

---

*Research: AREA 02 — Silhouette Variation System*
*Status: IN PROGRESS — Ready for DeepSeek verification + extension*