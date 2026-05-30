# AREA 03: CAMERA DISTANCE DIVERSITY SYSTEM

## The Problem

Current engine relies on:
- Same intimacy distance (close-up, medium close-up dominance)
- Same framing rhythm (2-shot, 3-shot repeating same structure)
- Same eye-level energy (neutral or slightly above)
- Same "head-and-shoulders" or "waist-up" crop dominance

Real social media camera variety: from extreme close-up to environmental wide, from planned to accidental.

---

## CAMERA_DISTANCE_VARIATION_LIBRARY

### Distance Categories (Based on Social Photography Research)

| Distance Type | Focal Length Equivalent | Frame Coverage | Emotional Tone | Token |
|--------------|------------------------|----------------|-----------------|-------|
| EXTREME_CLOSEUP | 35mm, <30cm | Face dominant, 60%+ frame | Intimate, voyeuristic | [EXTREME_CLOSEUP] |
| FACE_CLOSEUP | 50mm, 30-50cm | Face 50-70%, hair/shoulders | Personal, direct | [FACE_CLOSEUP] |
| HEAD_SHOULDERS | 85mm, 50-80cm | Head to mid-chest | Portrait classic | [HEAD_SHOULDERS] |
| WAIST_UP | 85-105mm, 1-1.5m | Waist to head | Social portrait | [WAIST_UP] |
| KNEE_TO_HEAD | 105mm, 1.5-2m | Knee to head | Environmental portrait | [KNEE_TO_HEAD] |
| FULL_BODY | 135mm, 2-3m | Full body, some floor/ceiling | Contextual | [FULL_BODY_SHOT] |
| ENVIRONMENTAL | 24-35mm, 3-5m | Body small, environment large | Documentary | [ENVIRONMENTAL_WIDE] |
| DISTANT_CANDID | Telephoto, 5m+ | Person as element | Stolen shot, observer | [DISTANT_CANDID] |

### Intimacy-Distance Framework

**Principle:** Distance = emotional contract. Closer = more intimacy, more expectation of relationship.

```
INTIMACY_DISTANCE_MATRIX:

Level 1: STRANGER_DISTANCE (3m+)
- Emotional tone: Public observation, documentary
- Expectation: None
- Token: [STRANGER_DISTANCE]

Level 2: ACQUAINTANCE_DISTANCE (1.5-3m)
- Emotional tone: Social but not intimate
- Expectation: Polite recognition
- Token: [ACQUAINTANCE_DISTANCE]

Level 3: FRIEND_DISTANCE (0.5-1.5m)
- Emotional tone: Comfortable, casual
- Expectation: Some relationship
- Token: [FRIEND_DISTANCE]

Level 4: INTIMATE_DISTANCE (<0.5m)
- Emotional tone: Private, intimate
- Expectation: Deep relationship
- Token: [INTIMATE_DISTANCE]
```

---

## Framing Diversity System

### 2D Composition Types

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| CENTRAL_COMPOSITION | Subject center frame | Intentionally framed, directed | [CENTRAL_COMPOSITION] |
| RULE_OF_THIRDS_OFF | Subject at intersection point | Slightly considered | [RULE_OF_THIRDS] |
| EDGE_FRAME | Subject near frame edge | Accident or creative | [EDGE_FRAME] |
| BOTTLENECK | Subject at narrow point in scene | Environmental framing | [BOTTLENECK_FRAME] |
| REFLECTION_FRAME | Subject in mirror, window, water | Self-documentation | [REFLECTION_FRAME] |
| OVER_THE_SHOULDER | Subject seen through another person's shoulder | Social document | [OVER_SHOULDER_SHOT] |
| HIDDEN_OBSERVER | Subject unaware, observer angle | Stolen shot | [HIDDEN_OBSERVER] |
| ACCIDENTAL_CROP | Framing appears imperfect | Authentic amateur | [ACCIDENTAL_CROP] |

### HK-Specific Framing Situations

| Situation | Framing Type | Token |
|-----------|-------------|-------|
| MTR Train Reflection | Mirror/reflection frame | [MTR_REFLECTION_SHOT] |
| Convenience Store Window | Window reflection, AC contrast | [CONVENIENCE_REFLECTION] |
| Ferry Deck Wide | Environmental, harbor context | [FERRY_WIDE] |
| Tea Restaurant Table | Overhead or side angle | [TEA_RESTAURANT_ANGLE] |
| Night Market Neon | Neon light framing, face lit by sign | [NEON_FACE_LIT] |
| Escalator Up | Ascending/descending, level change | [ESCALATOR_LEVEL] |

### Group Dynamics (EXPANDED)

| Type | Description | Token |
|------|-------------|-------|
| DUO_CLOSE | Two people, close together | [DUO_CLOSE] |
| DUO_APART | Two people, separate | [DUO_APART] |
| TRIO_GROUP | Three, dynamic triangle | [TRIO_DYNAMIC] |
| GROUP_SELFIE | Group selfie, front camera | [GROUP_SELFIE] |
| OVERHEARD | Person in background of other's photo | [OVERHEARD_IN_BACKGROUND] |
| GROUP_DINNER_4P | Four people, dinner setup | [GROUP_DINNER_4] |
| LARGE_GROUP_EVENT | 6+ people, event photo | [LARGE_GROUP_EVENT] |
| SOMEONE_ELSE_PHOTO | Someone else photographing subject | [SOMEONE_ELSE_PHOTO] |
| PHOTO_BOMB_HK | Accidental person in background | [PHOTO_BOMB_HK] |
| BACK_VIEW_PRIMARY | Subject's back as primary subject | [BACK_VIEW_PRIMARY] |
| RANDOM_IN_FRAME | Random person in frame, not posed | [RANDOM_IN_FRAME] |

### HK-Specific Framing Situations (EXPANDED)

| Situation | Framing Type | Token |
|-----------|-------------|-------|
| MTR Train Reflection | Mirror/reflection frame | [MTR_REFLECTION_SHOT] |
| Convenience Store Window | Window reflection, AC contrast | [CONVENIENCE_REFLECTION] |
| Ferry Deck Wide | Environmental, harbor context | [FERRY_WIDE] |
| Tea Restaurant Table | Overhead or side angle | [TEA_RESTAURANT_ANGLE] |
| Night Market Neon | Neon light framing, face lit by sign | [NEON_FACE_LIT] |
| Escalator Up | Ascending/descending, level change | [ESCALATOR_LEVEL] |
| 屋苑平台花園 | Estate podium garden, natural light | [ESTATE_FRAMING] |
| 行人天橋 | Footbridge, elevated view | [FOOTBRIDGE_WIDE] |
| 的士後座 | Taxi interior, rear seat view | [TAXI_REAR_SEAT] |
| 大學校園樓梯 | University stairwell, layered | [UNI_STAIRS] |
| 便利店玻璃 | Convenience store glass reflection | [CS_GLASS_REFLECTION] |
| 旺角行人隧道 | Mongkok pedestrian tunnel | [MONGKOK_TUNNEL] |

---

## Camera Height Variation

**Principle:** Same eye-level creates same energy. Real photos come from every angle.

| Height | Description | Effect | Token |
|--------|-------------|--------|-------|
| HIGH_ANGLE | Camera above subject (>15° down) | Subordinate, vulnerable, cute | [HIGH_ANGLE_CAMERA] |
| EYE_LEVEL | Camera at subject eye level | Neutral, equal | [EYE_LEVEL_CAMERA] |
| LOW_ANGLE | Camera below subject (>15° up) | Dominant, empowering, heroic | [LOW_ANGLE_CAMERA] |
| GROUND_LEVEL | Camera near floor | Immersive, worm-eye | [GROUND_LEVEL_CAMERA] |
| OVERHEAD | Camera directly above | Flat, bird's eye, abstract | [OVERHEAD_CAMERA] |
| HIP_LEVEL | Camera at hip height | Casual, candid | [HIP_LEVEL_CAMERA] |

---

## Shot Type Variation

### Candid vs Posed Spectrum

```
SHOT_TYPE_SPECTRUM:

P1: HIDDEN_CAMERA (most candid)
- Subject unaware
- No awareness, no performance
- Token: [HIDDEN_CAMERA_SHOT]

P2: FORGOTTEN_CAMERA
- Subject knows camera exists, but ignoring it
- Token: [FORGOTTEN_CAMERA]

P3: ACCIDENTAL_AWARENESS
- Subject notices camera at moment of capture
- Token: [ACCIDENTAL_AWARE]

P4: COOPERATIVE_FRIEND
- Subject knows, cooperating but casual
- Token: [COOPERATIVE_FRIEND]

P5: DIRECTED_PERFORMANCE
- Subject posing, aware and performing
- Token: [DIRECTED_PERFORMANCE]
```

### Group Dynamics

| Type | Description | Token |
|------|-------------|-------|
| DUO_CLOSE | Two people, close together | [DUO_CLOSE] |
| DUO_APART | Two people, separate | [DUO_APART] |
| TRIO_GROUP | Three, dynamic triangle | [TRIO_DYNAMIC] |
| GROUP_SELFIE | Group selfie, front camera | [GROUP_SELFIE] |
| OVERHEARD | Person in background of other's photo | [OVERHEARD_IN_BACKGROUND] |

---

## Prompt Grammar

```
[distance_type]:[EXTREME_CLOSEUP to DISTANT_CANDID]_
[intimacy_level]:[Level_1-4]_
[framing_type]:[CENTRAL to ACCIDENTAL_CROP]_
[camera_height]:[HIGH_ANGLE to OVERHEAD]_
[shot_type]:[P1-P5]_
[group_dynamics]:[solo/duo/trio/group]_
[awareness_level]:[unaware_forgotten_aware_cooperating_performing]
```

**Examples:**
```
[FULL_BODY_SHOT]_distance_
[intimacy:Level_3_FRIEND_DISTANCE]_
[framing:ENVIRONMENTAL_WIDE]_ferry_deck_harbor_context_
[camera_height:EYE_LEVEL_CAMERA]_
[shot_type:FORGOTTEN_CAMERA:P2]_
[group: solo]_
awareness:casual_streetwear_girl_harbor_evening

[FACE_CLOSEUP]_distance_
[intimacy:Level_4_INTIMATE_DISTANCE]_
[framing:REFLECTION_FRAME]_morning_bathroom_mirror_
[camera_height:HIP_LEVEL_CAMERA]_
[shot_type:COOPERATIVE_FRIEND:P4]_
[group:solo]_
awareness:no_makeup_morning_face_intimate
```

---

*Research: AREA 03 — Camera Distance Diversity System*
*Status: IN PROGRESS — Ready for DeepSeek verification + extension*