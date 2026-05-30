# ENGINE_V16_ANTI_FORMULA_EMOTIONAL_SYSTEM.md

## V16 Core Module — Emotional Rhythm / Accidental Sexiness / AI Noise / Feed Realism System
### SOURCE: V16_ANTI_FORMULA_RESEARCH (Areas 04-07)
### STATUS: READY FOR INTEGRATION

---

## PURPOSE

This module addresses four interconnected problems in the lil.troublr generation engine: (1) emotional monotony — the system produces overwhelmingly positive/cute/flirty output with no variety or honesty; (2) intentional attraction — attractiveness feels designed rather than emergent from physics and accident; (3) AI texture hallucination — over-sharpened skin, crunchy pores, and uniform detail create uncanny AI signatures; and (4) feed-level inauthenticity — individually optimized images that collectively feel like a production rather than a lived-in personal feed. The module provides libraries, tokens, grammar rules, and compositional systems to generate emotionally alive, physically believable, optically authentic content that functions as a cohesive personal feed.

---

## KEY CONCEPTS

- **Emotional Rhythm Variation**: The principle that real feeds contain emotional dips, fatigue, distraction, awkwardness, and negative-adjacent states — not perpetual happiness. Variety creates honesty and prevents the "AI happy" signature.
- **Accidental Sexiness / Physical Causality**: The principle that attraction emerges from body physics, clothing response to movement/environment, and exhaustion — not from intentional seduction poses. Every exposure moment requires a physical cause. Sexiness is in the cause, not the display.
- **Optical Softness / Natural Detail Hierarchy**: The principle that real cameras preserve softness, create detail gradients, and exhibit optical behavior (bloom, falloff, lens character). AI over-sharpens everything equally, creating crunch. Real skin looks like skin, not a pore map.
- **Feed-Level Realism**: The principle that a feed tells a story of a person living multiple days. It includes filler, ugly-cute moments, repetition, transitional moments, photodumps, and quality variation. Individually perfect images create collectively suspicious feeds.
- **Cross-Module Composition**: All four systems work simultaneously. An image can have accidental sexiness (physical cause), low energy emotion (honest fatigue), optical softness (anti-AI texture), and feed-level context (filler or transitional). Systems reinforce each other for maximum realism.
- **HK-Specific Context**: All systems include Hong Kong–specific situations, locations, optical conditions, emotional contexts, and cultural patterns unique to the target demographic.

---

## EMOTIONAL_RHYTHM_LIBRARY

### Category A: Low Energy States (Honest Fatigue)

**Why important:** Exhausted = not performing. Realest state.

| Type | Description | Visual Markers | Token |
|------|-------------|----------------|-------|
| A1: POST_TIRED | Just-woke or late-night tired | Heavy lids, minimal expression, slack mouth | [POST_TIRED_EXPRESSION] |
| A2: MID_ACTIVITY_TIRED | Tired from doing something | Slight slouch, reduced posture | [MID_ACTIVITY_TIRED] |
| A3: EXHAUSTED_LAYERED | Multiple fatigue sources | Zoned out, distant gaze | [EXHAUSTED_LAYERED] |
| A4: SLEEPY_HEAD_NOD | Head dropping, fighting sleep | Micro-sleep fragments | [SLEEPY_NOD] |
| A5: ENERGY_CRASH | Was high-energy, now flat | Expression drop, slack posture | [ENERGY_CRASH] |

### Category B: Distracted/Absent States

**Why important:** Real people are often mentally elsewhere.

| Type | Description | Visual Markers | Token |
|------|-------------|----------------|-------|
| B1: PHONE_ABSORBED | Looking at phone, oblivious | Slight furrow, concentrated | [PHONE_ABSORBED] |
| B2: WINDOW_GAZING | Looking at nothing, mind wandering | Soft unfocused gaze | [WINDOW_GAZING] |
| B3: DEEP_THOUGHT | Thinking hard about something | Furrowed brow, distant | [DEEP_THOUGHT] |
| B4: OVERSTIMULATED | Too much input, shutting down | Slightly overwhelmed expression | [OVERSTIMULATED] |
| B5: MORNING_FOG | Not fully awake, processing | Blank, unfocused | [MORNING_FOG] |
| B6: THOUGHT_INTERRUPTED | Was thinking, got interrupted | Caught mid-process | [THOUGHT_INTERRUPTED] |

### Category C: Socially Uncomfortable States

**Why important:** Awkward = honest. Shows social reality.

| Type | Description | Visual Markers | Token |
|------|-------------|----------------|-------|
| C1: SHY_APPROACH | Not sure of camera/photographer | Averted gaze, slight smile | [SHY_APPROACH] |
| C2: AWKWARD_SMILE | Forced smile, uncomfortable | Too wide, eyes not engaged | [AWKWARD_SMILE] |
| C3: TOO_MANY_PEOPLE | Uncomfortable with group energy | Edge of frame, looking away | [CROWD_OVERWHELM] |
| C4: POSING_ANXIETY | Knows camera, unsure how to pose | Stiff posture, tentative expression | [POSING_ANXIETY] |
| C5: POST_ARGUMENT | Just finished disagreeing | Tense jaw, flat expression | [POST_ARGUMENT] |
| C6: FIRST_MEETING | New person, evaluating | Curious but guarded | [NEW_PERSON_CURIOSITY] |

### Category D: Negative-Adjacent Emotions

**Why important:** Perfect happiness is suspicious. Real includes irritation, boredom, frustration.

| Type | Description | Visual Markers | Token |
|------|-------------|----------------|-------|
| D1: BORED_STARE | Nothing interesting happening | Flat expression, slight frown | [BORED_STARE] |
| D2: SLIGHT_IRRITATION | Minor frustration | Furrowed brow, tight lips | [SLIGHT_IRRITATION] |
| D3: DISAPPOINTED | Expectation not met | Sighing posture, downturned | [DISAPPOINTED] |
| D4: MISSING_SOMEONE | Longing for absent person | Soft sad, distant | [MISSING_SOMEONE] |
| D5: REGRET_EXPRESSION | Something undone | Wincing, avoiding eye | [REGRET_EXPRESSION] |
| D6: FRUSTRATED_BITE_LIP | Biting lip in frustration | Tense, mouth involved | [FRUSTRATED_BITE_LIP] |

### Category E: Complex/Mixed Emotions

**Why important:** Real emotions are rarely pure. Mix = sophistication.

| Type | Description | Visual Markers | Token |
|------|-------------|----------------|-------|
| E1: HAPPY_BUT_TIRED | Positive but low energy | Soft smile, heavy eyes | [HAPPY_BUT_TIRED] |
| E2: EXCITED_BUT_SHY | Eager but nervous | Bright eyes, averting gaze | [EXCITED_BUT_SHY] |
| E3: SAD_BUT_OKAY | Sad but coping | Neutral-ish, eyes give it away | [SAD_BUT_OKAY] |
| E4: TEASING_PLAYFUL | Pushing boundaries playfully | Mischief in eyes, slight smirk | [TEASING_PLAYFUL] |
| E5: CONFIDENT_VULNERABLE | Strong but open | Direct gaze, soft mouth | [CONFIDENT_VULNERABLE] |
| E6: PROUD_BUT_HUMBLE | Accomplished but modest | Quiet satisfaction | [PROUD_BUT_HUMBLE] |
| E7: LYING_TO_SELF | Expression contradicts reality | Micro-tells, asymmetry | [DENIAL_EXPRESSION] |

### Category F: Post-Activity Emotional States

**Why important:** After something, during something = honest context.

| Type | Description | Context | Token |
|------|-------------|---------|-------|
| F1: POST_LAUGH_RESIDUE | Just finished laughing | Residual smile, tear | [POST_LAUGH_RESIDUE] |
| F2: POST_CRY_RED | Cried recently | Red eyes, puffy | [POST_CRY_REDNESS] |
| F3: POST_ARGUMENT_TENSION | Tension remains | Avoidance, stiffness | [POST_ARGUMENT_TENSION] |
| F4: POST_WORKOUT | Post-exercise glow | Flushed, energised | [POST_WORKOUT] |
| F5: POST_SWIM_MOOD | Post-pool ambience | Chlorine, relaxed | [POST_SWIM_MOOD] |
| F6: POST_PARTY | Post-event comedown | Tired but wired | [POST_PARTY] |
| F7: TRAIN_RIDE_REFLECTION | Late night transport mood | Contemplative, alone | [TRAIN_RIDE_REFLECTION] |
| F8: NIGHTLIFE_LONELY | In party setting but alone | Contrast, disconnect | [NIGHTLIFE_LONELY] |

---

### Mood-Rotation System

#### Feed-Level Rhythm Rules

```
EMOTIONAL_ROTATION_RULESET:

Rule 1: Every 5 images must have at least one "low energy" (A types) emotion
Rule 2: Positive emotions (happy, flirty, warm) should not exceed 60% of feed
Rule 3: Every 10 images should have at least one "negative-adjacent" (D types) emotion
Rule 4: "Cute + flirty" should not appear in consecutive images
Rule 5: Post-activity states (F types) should appear every 3-4 images
```

#### Emotion Density Guidelines

| Emotion Type | Percentage of Feed | Purpose |
|-------------|-------------------|---------|
| Warm/Positive (classic) | 40-50% | Core lil.troublr identity |
| Low Energy (honest) | 15-20% | Realism anchor |
| Distracted/Absent | 10-15% | Life-continuity |
| Uncomfortable (social) | 5-10% | Social reality |
| Negative-adjacent | 5-10% | Honesty variety |
| Complex/Mixed | 5-10% | Sophistication |

---

### Anti-Emotional-Loop Grammar

#### Combination Rules

```
CAN_COMBINE:
- [POST_TIRED_EXPRESSION] + [SAD_BUT_OKAY]
- [BORED_STARE] + [WINDOW_GAZING]
- [EXCITED_BUT_SHY] + [TEASING_PLAYFUL]
- [PHONE_ABSORBED] + [MORNING_FOG]

CANNOT_COMBINE (too similar):
- [EXHAUSTED_LAYERED] + [SLEEPY_NOD]
- [AWKWARD_SMILE] + [POSING_ANXIETY]
- [SLIGHT_IRRITATION] + [FRUSTRATED_BITE_LIP]

CONTEXT_REQUIRED:
- [POST_ARGUMENT] → requires social context
- [POST_CRY_REDNESS] → requires story context
- [NIGHTLIFE_LONELY] → requires nightlife context
```

#### Prompt Grammar

```
[primary_emotion]:[A1-F8]_
[secondary_emotion]:[if_applicable]_
[intensity]:[mild_moderate_strong]_
[expression_completeness]:[full_partial_residual]_
[context_marker]:[location_or_activity]
```

**Examples:**
```
[POST_TIRED_EXPRESSION:A1]_emotion
intensity:moderate
expression_completeness:partial
context:late_morning_home

[EXCITED_BUT_SHY:E2]_emotion
intensity:mild
expression_completeness:full_with_micro_tells
context:first_time_trying_something

[BORED_STARE:D1]_emotion
intensity:mild
expression_completeness:full
context:waiting_for_friend_at_cafe
```

---

### HK-Specific Emotional Contexts

| Situation | Emotional State | Token |
|-----------|----------------|-------|
| MTR Rush Hour | [CROWD_OVERWHELM] + [OVERSTIMULATED] | [MTR_RUSH_EXHAUSTED] |
| Late Night Delivery | [TRAIN_RIDE_REFLECTION] + tired | [LATE_NIGHT_ALONE] |
| Post-Exam | [ENERGY_CRASH] + relieved | [POST_EXAM] |
| First Day at New Job | [NEW_PERSON_CURIOSITY] + nervous | [NEW_JOB_NERVOUS] |
| After Gym | [POST_WORKOUT] + tired | [POST_GYM] |
| Waiting for Boyfriend | [MISSING_SOMEONE] + anticipatory | [WAITING_BOYFRIEND] |
| Post-DSE exam | Relief + exhaustion | [DSE_RELEASE] |
| Long overtime work | Mental drain + tunnel vision | [OT_HEAVY] |
| Family dinner tension | Suppressed irritation + passive face | [FAMILY_DINNER_TENSE] |
| Shenzhen haggle fail | Disappointed + frustrated | [SHENZHEN_HAGGLE] |
| Post-breakup | Sad but okay + nightlife lonely | [POST_BREAKUP] |
| Live shopping nervous | Excited but shy + overstimulated | [LIVE_SHOPPING_NERVOUS] |
| Waiting BF late | Missing + slight irritation | [WAITING_BF_LATE] |

---

## ACCIDENTAL_SEXINESS_LIBRARY

### Category A: Movement-Based Accidental Exposure

**Principle:** Body moves → clothing responds → attraction emerges naturally.

| Type | Trigger | What Happens | Realism Signal | Token |
|------|---------|--------------|----------------|-------|
| A1: SHIRT_SHIFT_UP | Reaching, stretching, lifting arms | Shirt rises, midriff exposed | Movement cause | [SHIRT_RISE_MOVEMENT] |
| A2: TEE_NECKLINE_STRETCH | Head forward, looking down | Neckline widens, collarbone exposed | Posture cause | [NECKLINE_STRETCH] |
| A3: ARM_RAISE_UNDERARM | Arm up, reaching for something | Underarm exposed, skin visible | Practical cause | [UNDERARM_EXPOSED_ARMS_UP] |
| A4: BEND_FORWARD_CLEAVAGE | Leaning forward, seated | Gravity + compression = cleavage | Seated cause | [BEND_FORWARD_EXPOSE] |
| A5: SQUAT_BOTTOM_PULL | Squatting, bending down | Shorts/dress rides up | Movement cause | [SQUAT_RIDE_UP] |
| A6: WIND_BLOW_THIN_FABRIC | Wind, light fabric | Fabric clings, silhouette visible | Environmental cause | [WIND_CLING_SILHOUETTE] |
| A7: STRETCH_TIGHT_FABRIC | Stretching, arms up | Fitted fabric stretches, body visible | Body cause | [STRETCH_FABRIC_TIGHT] |
| A8: WALKING_HIP_SWAY | Normal walking gait | Natural hip movement, clothing shifts | Natural cause | [WALKING_HIP_SHIFT] |

### Category B: Seated/Compressed Attraction

**Principle:** Sitting creates predictable compression points.

| Type | Trigger | What Happens | Token |
|------|---------|--------------|-------|
| B1: SEATED_THIGH_GAP | Sitting with knees together | Legs pressed, thigh contact | [SEATED_THIGH_PRESS] |
| B2: CHAIR_FORWARD_LEAN | Leaning on chair back | Chest compressed against arms | [FORWARD_LEAN_CHEST] |
| B3: CROSS_LEGGED_SLIDE | Cross-legged, shifting | Dress/shorts ride up slightly | [CROSS_LEG_RIDE] |
| B4: LOW_CUT_SEATED | Seated, top shifts | Low neckline exposes more | [LOW_CUT_SEATED_SHIFT] |
| B5: LEGS_SPREAD_SEATED | Casual seated spread | More exposed, relaxed | [CASUAL_SPREAD_SEATED] |
| B6: KNEES_TO_CHEST | Arms around knees, compact | Body compressed, intimate | [KNEES_CHEST_COMPACT] |

### Category C: Fabric/Clothing Behavior

**Principle:** Clothing responds to body and environment.

| Type | Trigger | What Happens | Token |
|------|---------|--------------|-------|
| C1: SWEAT_WET_CLING | Humidity, exercise | Fabric transparent-ish, clings | [SWEAT_CLING] |
| C2: WET_BIKINI_SHIFT | Post-swim, wet fabric | Swimsuit heavy, shifts position | [WET_FABRIC_SHIFT] |
| C3: STRETCHED_COLLAR_REVEAL | Collar stretched from wear | Shoulder/collarbone visible | [STRETCHED_COLLAR_REVEAL] |
| C4: LOOSE_FABRIC_GAP | Thin/loose fabric, movement | Skin visible through gaps | [FABRIC_GAP_SKIN] |
| C5: HIGH_WAIST_SLIDE | High-waisted, sitting | Waistband creates line, shifts | [WAISTBAND_SLIDE] |
| C6: SHOULDER_SLIP | Sleeveless, relaxed | Strap falls off shoulder | [SHOULDER_STRAP_SLIP] |
| C7: BABY_TEE_STRETCH | Fitted tee, reaching | Fabric stretched thin, body visible | [TEE_STRETCH_BODY_VISIBLE] |

### Category D: Exhaustion/Relaxation Attraction

**Principle:** Tired = honest = attractive in honest way.

| Type | Trigger | What Happens | Token |
|------|---------|--------------|-------|
| D1: EXHAUSTED_NECK_EXPOSE | Head dropped, tired | Neck extended, vulnerable | [TIRED_NECK_EXTENDED] |
| D2: RELAXED_SHOULDER_DROP | Shoulders dropped, relaxed | Shoulder blade more visible | [RELAXED_SHOULDER_BLADE] |
| D3: SLEEPY_HEAD_TILT | Fighting sleep, head tilted | Neck exposed, soft expression | [SLEEPY_HEAD_TILT] |
| D4: SLUMP_CHEST_RELIEF | Slumped, back rounded | Chest relaxes, less held | [SLUMP_CHEST_RELEASE] |
| D5: HAND_BEHIND_HEAD | Supporting head | Underarm exposed, casual | [HAND_SUPPORT_HEAD] |
| D6: EYES_CLOSED_RELAXED | Eyes closed, breathing | Face relaxed, no performance | [EYES_CLOSED_TRUST] |

### Category E: Environmental Accidental

**Principle:** Environment causes clothing/body response.

| Type | Trigger | What Happens | Token |
|------|---------|--------------|-------|
| E1: HOT_DAY_STICKY | Heat, humidity | Fabric sticks, sheen | [HOT_DAY_STICKY] |
| E2: AIR_CON_CONTRAST | Entering AC from heat | Nipple visibility increase | [AC_NIPPLE_VISIBILITY] |
| E3: FLASH_FLATTEN | Camera flash | Fabric smooth, slight shine | [FLASH_SMOOTH] |
| E4: WATER_DROPS_DRIP | Post-pool, post-rain | Water tracks, transparency | [WATER_DROP_TRACKS] |
| E5: SUNSCREEN_OILY | Post-sunscreen application | Greasy sheen, glistening | [SUNSCREEN_GREASY_SHEEN] |
| E6: WIND_BLOW_HAIR_MOUTH | Wind, hair in face | Mouth parted, hair stuck | [HAIR_MOUTH_PARTED] |
| E7: AC_UNIT_DIRECT_BLOW | Standing in AC wind | Fabric shifts, moves | [AC_WIND_SHIFT] |
| E8: HOT_COLD_TRANSITION | Entering AC from heat | Goosebumps + fabric shift | [HEAT_COLD_TRANSITION] |
| E9: HUMID_SWEAT_CLING | Humid day, light fabric | Sweat + fabric = body visible | [HUMID_BODY_CLING] |
| E10: POST_RAIN_WET | Rain on fabric | Water tracks + transparency shift | [WET_FABRIC_HK] |
| E11: STEAM_ROOM | Hot shower, sauna | Skin glistening, red | [STEAM_ROOM_HK] |
| E12: WOK_HEAT_FACE | Cooking, kitchen heat | Flushed, sweating slightly | [COOKING_FLUSH] |

### Additional Forbidden Patterns (Too Intentional)

```
AVOID:
- Subject holding exposure in place (hand on shirt to keep it up)
- Subject actively creating the cause (leaning intentionally)
- Subject's gaze returning to camera after exposure
- Subject adjusting clothing to maintain exposure
- Close-up on exposed area while subject is aware
```

---

### Physical-Causality Seduction System

#### Principle

Every accidental attraction moment must have a **physical cause**. The seduction is in the cause, not the display.

**Wrong:** Subject is positioned to show cleavage (intentional)
**Right:** Subject is leaning forward to pick something up, which causes cleavage (physical causality)

#### Grammar

```
[physical_cause]:[movement_posture_environment]_
[clothing_response]:[what_fabric_does]_
[resulting_exposure]:[what_becomes_visible]_
[accidental_level]:[totally_accidental_mostly_accidental_minimally_designed]
```

**Examples:**
```
[REACHING_FOR_OBJECT:A7]_cause
clothing_response:[TEE_STRETCH_BODY_VISIBLE:C7]
exposure:midriff_and_body_contour
accidental_level:totally_accidental

[SEATED_WRITING:B1]_cause
clothing_response:thighs_pressed_together
exposure:[SEATED_THIGH_PRESS]
accidental_level:totally_accidental

[HUMID_NIGHT:E1]_cause
clothing_response:[SWEAT_CLING:C1]
exposure:fabric_cling_transparentish
accidental_level:environmental_accident
```

---

### Anti-Glamour Attraction Grammar

#### Rules

1. **Always include physical cause** — no exposure without cause
2. **Keep expression neutral/minimal** — sexiness is in physics, not performance
3. **Avoid close-up on exposed area** — context shot, not zoom
4. **Use exhausted/relaxed expression** — performance = intentional
5. **Environmental cause preferred** — humidity, wind, movement > deliberate pose

#### Forbidden Patterns (Too Intentional)

```
AVOID:
- Subject looking at exposed area
- Subject adjusting exposure (fixing it)
- Close-up on exposed area
- "Oops" expression or reaction
- Camera pointing at exposure
- Subject aware of exposure
```

---

## AI_NOISE_REDUCTION_LIBRARY

### Category A: Lens Softness Sources

Real lenses create softness. AI over-sharpens everything.

| Source | What It Does | Realism Signal | Token |
|--------|--------------|----------------|-------|
| A1: WIDE_APERTURE | Shallow DOF, face sharp, rest soft | Natural separation | [WIDE_APERTURE_SOFT] |
| A2: OLD_LENS_CHARACTER | Vintage/cheap lens, soft edges | Film era aesthetic | [OLD_LENS_SOFT] |
| A3: LOW_LIGHT_ISO | High ISO noise, grain, softness | Night authenticity | [LOW_LIGHT_SOFT] |
| A4: FOCUS_ERROR_SLIGHT | Subject not perfectly sharp | Candid authenticity | [FOCUS_SLIGHT_SOFT] |
| A5: ZOOM_LENS_SOFT | Telephoto compression + soft edges | Natural telephoto look | [TELEPHOTO_SOFT] |
| A6: POINT_AND_SHOOT_QUALITY | Compact camera softness | Amateur document | [COMPACT_SOFT] |

### Category B: Optical Bloom Sources

Light behaves optically — creates bloom, halos, softness.

| Source | What It Does | Realism Signal | Token |
|--------|--------------|----------------|-------|
| B1: BACKLIT_SOFT | Behind subject, creates glow | Natural warm | [BACKLIT_GLOW_SOFT] |
| B2: WINDOW_DIFFUSED | Soft box effect, gentle | Studio without studio | [WINDOW_DIFFUSE_SOFT] |
| B3: FLARE_ORGANIC | Lens flare, adds softness | Natural light accident | [ORGANIC_LENS_FLARE] |
| B4: CATCHLIGHT_SOFT | Eye catch light, alive | Human presence | [SOFT_CATCHLIGHT] |
| B5: SILHOUETTE_SOFT | Edge softness from backlight | Atmospheric | [SOFT_EDGE_SILHOUETTE] |

### Category C: Focus Falloff

Real focus is a gradient, not binary.

| Type | Description | Token |
|------|-------------|-------|
| C1: FRONT_FOCUS_SLIGHT | Slightly in front of subject | [FRONT_FOCUS_SOFT] |
| C2: BACK_FOCUS_SLIGHT | Slightly behind subject | [BACK_FOCUS_SOFT] |
| C3: EDGE_FALLOFF | Edges progressively soft | [EDGE_FOCUS_FALLOFF] |
| C4: CORNER_SOFT | Corners soft, center sharp | [CORNER_SOFTNESS] |
| C5: ENVIRONMENT_FUZZY | Background not perfectly sharp | [ENVIRONMENTAL_BLUR] |

### Category D: Sensor Characteristics

Real sensors have specific behaviors.

| Type | Description | Token |
|------|-------------|-------|
| D1: SKIN_SMOOTHING | Sensor noise reduction | [SENSOR_SMOOTH_SKIN] |
| D2: SHADOW_NOISE | Low-key, grain in shadows | [SHADOW_GRAIN] |
| D3: HIGHLIGHT_CLIP_SOFT | Bright areas soft-clip | [SOFT_HIGHLIGHT_CLIP] |
| D4: COLOR_NOISE_LOW | Slight color noise | [MINIMAL_COLOR_NOISE] |
| D5: DETAIL_LIMIT | Sensor detail limit | [SENSOR_DETAIL_LIMIT] |

### Category E: Flash Flattening

Flash changes everything — removes texture, flattens.

| Type | Description | Token |
|------|-------------|-------|
| E1: DIRECT_FLASH_HARD | Hard shadow, flat face | [DIRECT_FLASH_FLAT] |
| E2: BOUNCE_FLASH_SOFT | Soft fill, natural-ish | [BOUNCE_FLASH_SOFT] |
| E3: OFF_CAMERA_SOFT | Directional but soft | [OFF_CAMERA_FLASH] |
| E4: NO_FLASH_INDOOR | Available light, grain | [NO_FLASH_INDOOR] |

---

### Natural Detail Hierarchy

#### Principle

Real images have **detail hierarchy** — some things detailed, some soft. AI makes everything equally detailed = uncanny.

#### Hierarchy Rules

```
DETAIL_HIERARCHY_MATRIX:

HIGHEST DETAIL: Face (especially eyes, mouth)
HIGH DETAIL: Skin (subject's)
MEDIUM DETAIL: Immediate clothing (subject's)
LOW DETAIL: Background props
LOWEST DETAIL: Background environment (far)
NEAR-ZERO: Extreme edges

ANTI-AI RULE: If background has AI-like uniform sharpness (no lens falloff, no optical aberration) = AI
```

#### Prompt Grammar

```
[optical_softness_source]:[A1-A6]_
[bloom_type]:[B1-B5]_
[focus_type]:[C1-C5]_
[sensor_character]:[D1-D5]_
[flash_type]:[E1-E4]_
[detail_hierarchy]:[face_high_env_low]_
[softness_level]:[subtle_moderate_heavy]
```

**Examples:**
```
[WIDE_APERTURE_SOFT:A1]_optical
bloom:[WINDOW_DIFFUSE_SOFT:B2]
focus:[EDGE_FOCUS_FALLOFF:C3]
sensor:[SENSOR_SMOOTH_SKIN:D1]
flash:[NO_FLASH_INDOOR:E4]
detail_hierarchy:face_high_clothing_medium_env_fuzzy
softness_level:moderate
```

---

### Anti-Crunch Realism System

#### Crunchy Skin Causes

AI skin looks "crunchy" when:
1. Over-sharpened individual pores
2. Noise added to skin texture
3. Every pore equally visible
4. Skin has "texture" without softness
5. Edge enhancement on skin

#### Solutions

```
ANTI_CRUNCH_PRESCRIPTION:

1. Use: [SENSOR_SMOOTH_SKIN] — sensor NR softens skin
2. Use: [WIDE_APERTURE_SOFT] — shallow DOF de-focuses skin edges
3. Use: [LOW_LIGHT_SOFT] — natural grain masks AI texture
4. Avoid: Detail emphasis on skin
5. Avoid: Pore visibility as "detail"
6. Rule: Skin should look like skin, not pore map
```

#### Texture Density Balancing

| Scene Type | Texture Level | Reason |
|-----------|---------------|--------|
| Close-up face | LOW texture | Skin softness, intimacy |
| Medium shot body | MEDIUM texture | Visible but not crunchy |
| Wide environmental | LOW texture | Background fades |
| Night/low light | VERY LOW | Grain dominates texture |
| Flash | VERY LOW | Flattened, soft |

---

### HK-Specific Optical Situations

| Situation | Optical Solution | Token |
|-----------|------------------|-------|
| MTR fluorescent | [LOW_LIGHT_SOFT] + [FLUORESCENT_POLLUTION] | [MTR_OPTICAL_SOFT] |
| Night market neon | [ORGANIC_LENS_FLARE] + [BACKLIT_GLOW_SOFT] | [NEON_OPTICAL_SOFT] |
| Indoor pool | [WIDE_APERTURE_SOFT] + [CHLORINE_REFLECTION] | [POOL_OPTICAL_SOFT] |
| Tea restaurant | [COMPACT_SOFT] + available light | [TEA_REST_OPTICAL] |
| Ferry deck night | [TELEPHOTO_SOFT] + harbor lights | [FERRY_OPTICAL_SOFT] |
| 茶餐廳油煙 | [LOW_LIGHT_SOFT] + greasy steam | [TEA_REST_STEAM] |
| 主題公園煙火 | [FLASH_SMOOTH] + dark + sparkles | [FIREWORKS_OPTICAL] |
| 天台夜景 | [TELEPHOTO_SOFT] + city lights | [ROOFTOP_NIGHT_OPTICAL] |
| 巴士上層 | [MOTION_BLUR_SOFT] + window frame | [BUS_INTERIOR_OPTICAL] |
| 旺角行人隧道 | [FLUORESCENT_POLLUTION] + footsteps | [MONGKOK_TUNNEL_OPTICAL] |

---

## FEED_LEVEL_REALISM_LIBRARY

### Category A: Filler/Low-Effort Content

**Why real:** Not every photo is a production. Some are just "I'm here."

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| A1: QUICK_SELFIE | 2 seconds in bathroom mirror | Low quality, spontaneous | [QUICK_SELFIE] |
| A2: FOOD_DOCUMENT | Food photo, subject secondary | "Look what I ate" | [FOOD_DOCUMENT] |
| A3: RANDOM_SNAPSHOT | Nothing special, moment captured | "I was here" energy | [RANDOM_SNAPSHOT] |
| A4: BACKGROUND_CAPTURE | Subject accidentally in shot | Forgot to check frame | [ACCIDENTAL_BACKGROUND] |
| A5: CLOSEUP_DETAIL | Just a hand, object, feet | Partial, intimate | [BODY_PART_CLOSEUP] |
| A6: SCREENSHOT_REPOST | Reposted story, screen captured | Meta, digital | [SCREENSHOT_REPOST] |
| A7: OCTOPUS_RECEIPT | Octopus reload receipt | Daily life, transit | [OCTOPUS_RECEIPT] |
| A8: GARBAGE_BAG_TAG | Trash bag charge receipt visible | 垃圾徵費 daily | [GARBAGE_TAG] |
| A9: TAKEAWAY_LUNCH | Delivery packaging, open box | 外賣 culture | [TAKEAWAY_LUNCH] |
| A10: QUEUE_TICKET | Number ticket from queue | MTR/minivan wait | [QUEUE_TICKET] |

### Category B: Repetition/Life Continuity

**Why real:** Real girls repeat things — outfits, locations, people. This is identity.

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| B1: SAME_LOCATION_AGAIN | Back to same cafe/park/place | "This is my spot" | [SAME_PLACE_AGAIN] |
| B2: SAME_OUTFIT_REPEAT | Wearing yesterday's clothes | "Did laundry yet?" | [SAME_OUTFIT_REPEAT] |
| B3: SAME_FRIEND_GROUP | Same people appearing | Social continuity | [SAME_FRIEND_AGAIN] |
| B4: CONTINUING_STORY | Sequel to previous post | Narrative continuity | [CONTINUING_STORY] |
| B5: RETURNING_AFTER_BREAK | Back after hiatus | "I'm still here" | [RETURNING_AFTER_BREAK] |

### Category C: "Ugly-Cute" Moments

**Why real:** Perfect beauty is suspicious. Cute-but-not-perfect humanizes.

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| C1: BUNNY_SNORING | Cute sleeping face, mouth open | Vulnerability, honesty | [SLEEPING_BUNNY_SNORE] |
| C2: BAD_ANGLE_HANDSOME | Technically bad photo but cute subject | "Still pretty right?" | [BAD_ANGLE_STILL_CUTE] |
| C3: UNCOMBED_HAIR | Just woke up, hair everywhere | Morning honesty | [MESSY_MORNING_HAIR] |
| C4: FOOD_ON_FACE | Eating messily, food on cheek | Playful, unperformed | [FOOD_ON_CHEEK] |
| C5: EYES_CLOSED_SQUINT | Squinting in bright light, laughing | Unflattering but real | [SQUINT_LAUGH] |
| C6: WEIRD_FACIAL_EXPRESSION | Random silly face | Playful, not performing | [SILLY_FACE] |
| C7: DOUBLE_CHIN_MOMENT | Head angle creates double chin | Honest moment | [DOUBLE_CHIN_HONEST] |

### Category D: Transitional Moments

**Why real:** Life is transitions. Between places, moods, activities.

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| D1: GETTING_READY | In bathroom, getting prepared | Pre-event ritual | [GETTING_READY] |
| D2: TAXI_RIDE_TRANSIT | In car, arriving somewhere | In-between moment | [TAXI_TRANSIT] |
| D3: WAITING_FOR_SOMEONE | Standing/waiting, looking around | Anticipation | [WAITING_SOMEONE] |
| D4: POST_EVENT_COME_DOWN | After party, still in clothes | Comedown energy | [POST_EVENT_DOWN] |
| D5: MID_CONVERSATION | Talking to someone, not posing | Social moment | [MID_CONVERSATION] |
| D6: CHECKING_PHONE | Pulled out phone, checking | Distracted, normal | [CHECKING_PHONE] |
| D7: ENTERING_FRAME | Walking into photo, not set up | Environmental entry | [ENTERING_FRAME] |

### Category E: Social Proof/Group Dynamics

**Why real:** Real life includes other people. Social context = authenticity.

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| E1: GROUP_PHOTO_CROP | Someone cropped out, face visible | Someone else's photo | [GROUP_PHOTO_CROPPED] |
| E2: IN_BACKGROUND_OTHERS | Other people in frame | Social context | [OTHERS_IN_BACKGROUND] |
| E3: CELEBRATION_MOMENT | Birthday, achievement, milestone | Social event | [CELEBRATION_MOMENT] |
| E4: FRIEND_SOLO_WITH | Solo but friend took it | "My friend took this" | [FRIEND_TOOK_PHOTO] |
| E5: OVERHEARD_STORY | Photo of someone else, story about them | Social awareness | [STORY_ABOUT_OTHER] |

---

### Photodump Pacing System

#### Principle

Photodump = multiple related photos that feel like documentation, not production.

#### Photodump Sub-Types

```
PHOTODUMP_SESSION now has structured sub-types:

[PHOTODUMP_SAME_OUTFIT] — 3-4 shots, same clothes, different activities/angles
[PHOTODUMP_LOCATION] — 3-4 shots, same location, different times/angles
[PHOTODUMP_MOMENT] — sequential moments, like mini-story (before/after)
[PHOTODUMP_MIXED] — random selection, like phone dump

Rules within session:
- At least 1 distance change (close → medium → wide OR vice versa)
- At least 1 "lower quality" shot (grainy, slightly blurry, awkward)
- Max 1 "hero" quality shot per session
```

#### Pacing Rules

```
PHOTODUMP_COMPOSITION:

1. MIX_QUALITY: 2-3 "good" photos + 1-2 "filler" photos
2. VARIED_DISTANCE: One close, one medium, one wide
3. MIXED_EXPRESSIONS: 1 candid, 1 smiling, 1 distracted
4. REPEATED_LOCATION: All at same place, different angles
5. CONTINUITY_SHOT: Sequential moment captured
```

#### Feed Architecture

```
FEED_ARCHITECTURE:

WEEK_ARCHITECTURE:
- 1 "hero" post: Production quality, high effort
- 2-3 "story" posts: Narrative, ongoing
- 1-2 "filler" posts: Low effort, real life
- 1 "ugly-cute" post: Vulnerable, honest

PATTERN_NOT_TO_FOLLOW:
- ❌ Perfect quality every single photo
- ❌ Same expression every photo
- ❌ Same distance every photo
- ❌ No transitional moments
- ❌ No filler/low-quality shots
```

---

### Continuity-Feed Architecture

#### Principle

Feed should tell a story. Each photo relates to others. Continuity creates life narrative.

#### Continuity Types

```
CONTINUITY_LIBRARY:

CON_01: OUTFIT_CONTINUITY
- Same outfit, different angles/activities
- Token: [OUTFIT_CONTINUITY]

CON_02: LOCATION_CONTINUITY
- Same location across days/weeks
- Token: [LOCATION_CONTINUITY]

CON_03: MOOD_CONTINUITY
- Same emotional state continuing
- Token: [MOOD_CONTINUITY]

CON_04: NARRATIVE_CONTINUITY
- Sequel to previous post's story
- Token: [NARRATIVE_CONTINUITY]

CON_05: PERSON_CONTINUITY
- Same friend/people appearing
- Token: [PERSON_CONTINUITY]

CON_06: TIME_CONTINUITY
- Before/after, morning/night, then/now
- Token: [TIME_CONTINUITY]
```

#### Feed Example

```
IMAGE_01: [POST_WORKOUT] + [OUTFIT_CONTINUITY: same gym outfit from yesterday]
IMAGE_02: [SAME_PLACE_AGAIN] + [LOCATION_CONTINUITY: same gym]
IMAGE_03: [QUICK_SELFIE] + [FOOD_DOCUMENT] + [RANDOM_SNAPSHOT] = [PHOTODUMP_SESSION]
IMAGE_04: [RETURNING_AFTER_BREAK] + [SAME_FRIEND_AGAIN]
```

---

### Social-Upload Rhythm Grammar

#### When Real Girls Post

```
UPLOAD_RHYTHM:

RHYTHM_A: MORNING_DOC (Morning person)
- Morning photo, wake-up face
- Coffee, morning light
- Token: [MORNING_POST]

RHYTHM_B: AFTERNOON_CANDID (Spontaneous afternoon)
- Random afternoon moment
- Nothing special happening
- Token: [AFTERNOON_RANDOM]

RHYTHM_C: EVENING_GLAM (Going out prep)
- Getting ready, outfit reveal
- Evening/event context
- Token: [EVENING_GLAM]

RHYTHM_D: LATE_NIGHT_REFLECTION (Night owl)
- Late night, reflective
- 11pm+ posts
- Token: [LATE_NIGHT_REFLECT]

RHYTHM_E: WEEKEND_VARIATION (Weekend vs weekday)
- Weekend: more casual, spontaneous
- Weekday: more curated
- Token: [WEEKEND_CASUAL]
```

---

### HK-Specific Feed Patterns

| Pattern | Description | Token |
|---------|-------------|-------|
| Tea restaurant repeat | Same tea restaurant, different dishes | [TEA_REST_FEED] |
| MTR same station | Same MTR station, different days | [MTR_STATION_FEED] |
| Friend group rotation | Same friends, different activities | [HK_FRIEND_FEED] |
| Night market documentation | Night market visit, food focus | [NIGHT_MARKET_FEED] |
| Beach day series | Beach trip, photodump style | [BEACH_DAY_FEED] |
| Staycation repetition | Same hotel, different occasions | [STAYCATION_FEED] |

---

### Feed-Level Anti-Repetition Rules

1. **Every 5 images: at least one "ugly-cute" or "filler" type**
2. **Every 7 images: at least one photodump session (3+ related shots)**
3. **Every 10 images: at least one transitional moment**
4. **Quality variation is key**: Mix high-quality + medium + low-quality shots. Not every photo should be hero quality.
5. **"Accidental bad" ≠ "consistently bad"**: 1-2 genuinely awkward/blurry shots per 10 images = authenticity. Every photo looking low-quality = low-skill generation.
6. **Anti-formula rule**: If the last 5 images all have similar silhouette (tight top + tight bottom), the next image MUST have loose/baggy silhouette.

---

## CROSS_MODULE_INTEGRATION

### How All Four Systems Compose Together

The four systems — Emotional Rhythm, Accidental Sexiness, AI Noise Reduction, and Feed-Level Realism — are not independent modules. They are layers that compose simultaneously to produce a single image. Every generated image should activate appropriate tokens from each system, creating images that are emotionally varied, physically believable, optically authentic, and feed-contextually appropriate.

#### Layering Principle

```
IMAGE_GENERATION_STACK:

Layer 1: EMOTIONAL STATE (from EMOTIONAL_RHYTHM_LIBRARY)
         → Sets primary expression, energy level, social context
         → Examples: [POST_TIRED_EXPRESSION], [EXCITED_BUT_SHY], [BORED_STARE]

Layer 2: PHYSICAL_CAUSALITY (from ACCIDENTAL_SEXINESS_LIBRARY)
         → Adds movement, posture, or environmental trigger
         → Examples: [REACHING_FOR_OBJECT], [SEATED_THIGH_PRESS], [HUMID_BODY_CLING]

Layer 3: OPTICAL_CHARACTER (from AI_NOISE_REDUCTION_LIBRARY)
         → Defines lens behavior, softness, detail hierarchy
         → Examples: [WIDE_APERTURE_SOFT], [WINDOW_DIFFUSE_SOFT], [SENSOR_SMOOTH_SKIN]

Layer 4: FEED_CONTEXT (from FEED_LEVEL_REALISM_LIBRARY)
         → Sets content type, quality variation, social proof
         → Examples: [PHOTODUMP_SESSION], [SAME_PLACE_AGAIN], [UGLY_CUTE]
```

#### Composition Examples

**Example 1: Low-energy candid, physically accidental, optically soft, feed-appropriate**
```
[EMOTIONAL]: [POST_TIRED_EXPRESSION:A1] + intensity:moderate + expression_completeness:partial
[CAUSALITY]: [REACHING_FOR_PHONE] + clothing_response:[TEE_STRETCH_BODY_VISIBLE:C7] + exposure:midriff
[OPTICAL]: [WIDE_APERTURE_SOFT:A1] + [SENSOR_SMOOTH_SKIN:D1] + [ENVIRONMENTAL_BLUR:C5] + softness:moderate
[FEED]: [RANDOM_SNAPSHOT] + [SAME_OUTFIT_REPEAT] + distance:medium
```

**Example 2: Post-workout, environmental sexiness, natural optical, photodump context**
```
[EMOTIONAL]: [POST_WORKOUT:F4] + intensity:strong + expression_completeness:residual
[CAUSALITY]: [HUMID_BODY_CLING:E9] + [SWEAT_CLING:C1] + environmental_accident
[OPTICAL]: [LOW_LIGHT_SOFT:A3] + [ORGANIC_LENS_FLARE:B3] + detail_hierarchy:face_high_env_low
[FEED]: [PHOTODUMP_SAME_OUTFIT] + distance:varied (close-medium-wide)
```

**Example 3: Night transit, distracted, realistic optical, transitional feed**
```
[EMOTIONAL]: [TRAIN_RIDE_REFLECTION:F7] + [PHONE_ABSORBED:B1] + intensity:mild
[CAUSALITY]: [WINDOW_GAZING] + ambient_seated
[OPTICAL]: [LOW_LIGHT_SOFT:A3] + [TELEPHOTO_SOFT:A5] + [SHADOW_GRAIN:D2] + softness:heavy
[FEED]: [TRANSITIONAL_MOMENT] + [LATE_NIGHT_REFLECT] + distance:medium
```

#### Cross-Module Rules

1. **Emotional state constrains physical causality**: Exhausted emotions ([POST_TIRED_EXPRESSION], [SLEEPY_NOD]) pair naturally with relaxation attractions ([TIRED_NECK_EXTENDED], [EYES_CLOSED_TRUST]). They should not pair with high-energy movements.

2. **Optical character should match emotional/physical context**: Post-workout plausibly has [LOW_LIGHT_SOFT] + [SENSOR_SMOOTH_SKIN]. High-key studio would be wrong. Night transit requires [LOW_LIGHT_SOFT] + [SHADOW_GRAIN].

3. **Feed context overrides individual image optimization**: Even a "perfect" shot should sometimes be generated as [QUICK_SELFIE] or [BAD_ANGLE_STILL_CUTE] because feed-level realism demands quality variation.

4. **Accidental sexiness requires emotional neutrality**: When physical causality produces exposure, expression should be [POST_TIRED_EXPRESSION], [EYES_CLOSED_TRUST], [PHONE_ABSORBED] — not a reaction to the exposure. Awareness of exposure = intentional = wrong.

5. **HK-specific contexts activate cross-module HK tokens**: A Hong Kong MTR rush hour scene should combine [MTR_RUSH_EXHAUSTED] (emotional) + [MTR_OPTICAL_SOFT] (optical) + [MTR_STATION_FEED] (feed) for maximum local authenticity.

#### Anti-Formula Cross-Module Check

Before finalizing any generated image, run the following checks:

```
CROSS_MODULE_ANTI_FORMULA_CHECK:

✓ EMOTIONAL: Is there at least one low-energy or negative-adjacent emotion? (Not all positive)
✓ SEXINESS: Does exposure have a physical cause? (Not intentional display)
✓ OPTICAL: Does detail hierarchy exist? (Face > Clothing > Environment)
✓ FEED: Would this image feel at home in a real person's IG feed? (Not too perfect)
✓ SILHOUETTE: If last 5 images were tight-on-tight, is this loose/baggy?
```

---

## IMPLEMENTATION

### How to Use — Practical Guidance with Example Prompts

This section provides concrete prompt structures and generation examples for integrating all four systems into production workflows.

### Basic Prompt Structure

For any generated image, include the following sections in order:

```
PREFIX_OVERRIDE: anti_formula_v16
STYLE: authentic_hong_kong_kol
QUALITY: natural_photographic

[EMOTIONAL_LAYER]
primary_emotion: [TOKEN]
intensity: [mild/moderate/strong]
completeness: [full/partial/residual]
context: [location_or_activity]

[PHYSICAL_LAYER]
cause: [movement/posture/environment]
clothing_response: [TOKEN or description]
exposure: [what_becomes_visible]
accidental_level: [totally/mmostly/minimally_accidental]

[OPTICAL_LAYER]
lens: [TOKEN]
bloom: [TOKEN]
focus: [TOKEN]
sensor: [TOKEN]
flash: [TOKEN]
detail_hierarchy: [face_high_env_low/medium/etc]
softness: [subtle/moderate/heavy]

[FEED_LAYER]
content_type: [TOKEN]
continuity: [TOKEN if applicable]
distance: [close/medium/wide/varied]
quality_tier: [hero/good/filler/accidental_bad]
```

### Example Prompts

#### Example 1: Late Night Home, Post-Shower, Casual

```
PREFIX_OVERRIDE: anti_formula_v16
STYLE: authentic_hong_kong_kol
QUALITY: natural_photographic

[EMOTIONAL_LAYER]
primary_emotion: [POST_TIRED_EXPRESSION:A1]
intensity: mild
completeness: partial
context: late_night_home_bathroom

[PHYSICAL_LAYER]
cause: just_finished_showering relaxed_posture
clothing_response: thin_towel loose_fabric_gap
exposure: shoulder_back_skin
accidental_level: totally_accidental

[OPTICAL_LAYER]
lens: [COMPACT_SOFT:A6]
bloom: none_minimal
focus: [FRONT_FOCUS_SOFT:C1]
sensor: [SENSOR_SMOOTH_SKIN:D1]
flash: none
detail_hierarchy: face_high_skin_medium_env_low
softness: moderate

[FEED_LAYER]
content_type: [QUICK_SELFIE]
continuity: none
distance: close
quality_tier: filler
```

#### Example 2: MTR Rush Hour, Tired, Morning Commute

```
PREFIX_OVERRIDE: anti_formula_v16
STYLE: authentic_hong_kong_kol
QUALITY: natural_photographic

[EMOTIONAL_LAYER]
primary_emotion: [MTR_RUSH_EXHAUSTED]
intensity: strong
completeness: residual (worn off)
context: mtr__platform_morning

[PHYSICAL_LAYER]
cause: standing_holding_pole crowded
clothing_response: humid_fabric sticky_sheer
exposure: fabric_cling_body_outline
accidental_level: environmental_accident

[OPTICAL_LAYER]
lens: [LOW_LIGHT_SOFT:A3]
bloom: [ORGANIC_LENS_FLARE:B3] (fluorescent flicker)
focus: [FOCUS_SLIGHT_SOFT:A4]
sensor: [MINIMAL_COLOR_NOISE:D4]
flash: none
detail_hierarchy: face_high_env_fuzzy
softness: heavy

[FEED_LAYER]
content_type: [RANDOM_SNAPSHOT]
continuity: [MTR_STATION_FEED]
distance: medium
quality_tier: good
```

#### Example 3: Beach Day, Post-Swim, Wind + Sun + Water

```
PREFIX_OVERRIDE: anti_formula_v16
STYLE: authentic_hong_kong_kol
QUALITY: natural_photographic

[EMOTIONAL_LAYER]
primary_emotion: [POST_SWIM_MOOD:F5]
intensity: moderate
completeness: full
context: beach_shoulder_season

[PHYSICAL_LAYER]
cause: wind_coming_off_water body_still_wet
clothing_response: [WET_FABRIC_SHIFT:C2] bikini heavy_cling
exposure: fabric_transparentish body_visible
accidental_level: totally_accidental

[OPTICAL_LAYER]
lens: [WIDE_APERTURE_SOFT:A1]
bloom: [BACKLIT_GLOW_SOFT:B1]
focus: [EDGE_FOCUS_FALLOFF:C3]
sensor: [SENSOR_SMOOTH_SKIN:D1]
flash: none
detail_hierarchy: face_high_body_medium_env_soft
softness: subtle

[FEED_LAYER]
content_type: [PHOTODUMP_MIXED]
continuity: [BEACH_DAY_FEED]
distance: varied
quality_tier: good
```

#### Example 4: Tea Restaurant, Lunch, Accidental Backlight

```
PREFIX_OVERRIDE: anti_formula_v16
STYLE: authentic_hong_kong_kol
QUALITY: natural_photographic

[EMOTIONAL_LAYER]
primary_emotion: [BORED_STARE:D1]
intensity: mild
completeness: full
context: tea_restaurant_lunch_waiting

[PHYSICAL_LAYER]
cause: seated_windowside window_light_behind
clothing_response: [WINDOW_DIFFUSE_SOFT:B2] highlights
exposure: edge_silhouette
accidental_level: totally_accidental

[OPTICAL_LAYER]
lens: [COMPACT_SOFT:A6]
bloom: [SOFT_EDGE_SILHOUETTE:B5]
focus: [CORNER_SOFTNESS:C4]
sensor: [SOFT_HIGHLIGHT_CLIP:D3]
flash: none
detail_hierarchy: face_medium_env_low
softness: moderate

[FEED_LAYER]
content_type: [FOOD_DOCUMENT] + [SELF_IF_IN_FRAME]
continuity: [TEA_REST_FEED]
distance: medium
quality_tier: filler
```

#### Example 5: Post-Party, Nightlife Lonely, Taxi Transit

```
PREFIX_OVERRIDE: anti_formula_v16
STYLE: authentic_hong_kong_kol
QUALITY: natural_photographic

[EMOTIONAL_LAYER]
primary_emotion: [NIGHTLIFE_LONELY:F8]
intensity: strong
completeness: full
context: late_night_taxi_home

[PHYSICAL_LAYER]
cause: slumped_in_taxi tired_after_event
clothing_response: party_outfit_relaxed wrinkled
exposure: minimal_accidental
accidental_level: environmental_accident

[OPTICAL_LAYER]
lens: [LOW_LIGHT_SOFT:A3]
bloom: [ORGANIC_LENS_FLARE:B3] (street lights)
focus: [ENVIRONMENTAL_BLUR:C5]
sensor: [SHADOW_GRAIN:D2]
flash: none
detail_hierarchy: face_high_env_near_zero
softness: heavy

[FEED_LAYER]
content_type: [TAXI_TRANSIT] + [SELFIE_ATTEMPT]
continuity: [NIGHT_MARKET_FEED] or [POST_EVENT_DOWN]
distance: close
quality_tier: accidental_bad (intentionally lower quality)
```

### Generation Rules Summary

1. **Every image must have an emotional state** — never default to "happy" or "neutral"
2. **Every accidental sexiness token must have a physical cause** — no exposure without trigger
3. **Every image must have optical character** — never generate without lens/sensor behavior
4. **Every 5 images must include one filler, ugly-cute, or low-quality type** — feed variety is mandatory
5. **Never generate two consecutive images with the same emotional archetype** — rotate
6. **Never generate two consecutive images with the same silhouette profile** — mix tight/loose
7. **HK contexts activate HK-specific tokens** — local authenticity compounds

---

## TOKEN REFERENCE

### Emotional Rhythm Tokens (Area 04)

| Token | Category | Type |
|-------|----------|------|
| [POST_TIRED_EXPRESSION] | A: Low Energy | A1 |
| [MID_ACTIVITY_TIRED] | A: Low Energy | A2 |
| [EXHAUSTED_LAYERED] | A: Low Energy | A3 |
| [SLEEPY_NOD] | A: Low Energy | A4 |
| [ENERGY_CRASH] | A: Low Energy | A5 |
| [PHONE_ABSORBED] | B: Distracted | B1 |
| [WINDOW_GAZING] | B: Distracted | B2 |
| [DEEP_THOUGHT] | B: Distracted | B3 |
| [OVERSTIMULATED] | B: Distracted | B4 |
| [MORNING_FOG] | B: Distracted | B5 |
| [THOUGHT_INTERRUPTED] | B: Distracted | B6 |
| [SHY_APPROACH] | C: Uncomfortable | C1 |
| [AWKWARD_SMILE] | C: Uncomfortable | C2 |
| [CROWD_OVERWHELM] | C: Uncomfortable | C3 |
| [POSING_ANXIETY] | C: Uncomfortable | C4 |
| [POST_ARGUMENT] | C: Uncomfortable | C5 |
| [NEW_PERSON_CURIOSITY] | C: Uncomfortable | C6 |
| [BORED_STARE] | D: Negative-Adjacent | D1 |
| [SLIGHT_IRRITATION] | D: Negative-Adjacent | D2 |
| [DISAPPOINTED] | D: Negative-Adjacent | D3 |
| [MISSING_SOMEONE] | D: Negative-Adjacent | D4 |
| [REGRET_EXPRESSION] | D: Negative-Adjacent | D5 |
| [FRUSTRATED_BITE_LIP] | D: Negative-Adjacent | D6 |
| [HAPPY_BUT_TIRED] | E: Complex | E1 |
| [EXCITED_BUT_SHY] | E: Complex | E2 |
| [SAD_BUT_OKAY] | E: Complex | E3 |
| [TEASING_PLAYFUL] | E: Complex | E4 |
| [CONFIDENT_VULNERABLE] | E: Complex | E5 |
| [PROUD_BUT_HUMBLE] | E: Complex | E6 |
| [DENIAL_EXPRESSION] | E: Complex | E7 |
| [POST_LAUGH_RESIDUE] | F: Post-Activity | F1 |
| [POST_CRY_REDNESS] | F: Post-Activity | F2 |
| [POST_ARGUMENT_TENSION] | F: Post-Activity | F3 |
| [POST_WORKOUT] | F: Post-Activity | F4 |
| [POST_SWIM_MOOD] | F: Post-Activity | F5 |
| [POST_PARTY] | F: Post-Activity | F6 |
| [TRAIN_RIDE_REFLECTION] | F: Post-Activity | F7 |
| [NIGHTLIFE_LONELY] | F: Post-Activity | F8 |

### HK-Specific Emotional Tokens

| Token | Context |
|-------|---------|
| [MTR_RUSH_EXHAUSTED] | MTR Rush Hour |
| [LATE_NIGHT_ALONE] | Late Night Delivery |
| [POST_EXAM] | Post-Exam |
| [NEW_JOB_NERVOUS] | First Day at New Job |
| [POST_GYM] | After Gym |
| [WAITING_BOYFRIEND] | Waiting for Boyfriend |
| [DSE_RELEASE] | Post-DSE exam |
| [OT_HEAVY] | Long overtime work |
| [FAMILY_DINNER_TENSE] | Family dinner tension |
| [SHENZHEN_HAGGLE] | Shenzhen haggle fail |
| [POST_BREAKUP] | Post-breakup |
| [LIVE_SHOPPING_NERVOUS] | Live shopping nervous |
| [WAITING_BF_LATE] | Waiting BF late |

### Accidental Sexiness Tokens (Area 05)

| Token | Category | Type |
|-------|----------|------|
| [SHIRT_RISE_MOVEMENT] | A: Movement | A1 |
| [NECKLINE_STRETCH] | A: Movement | A2 |
| [UNDERARM_EXPOSED_ARMS_UP] | A: Movement | A3 |
| [BEND_FORWARD_EXPOSE] | A: Movement | A4 |
| [SQUAT_RIDE_UP] | A: Movement | A5 |
| [WIND_CLING_SILHOUETTE] | A: Movement | A6 |
| [STRETCH_FABRIC_TIGHT] | A: Movement | A7 |
| [WALKING_HIP_SHIFT] | A: Movement | A8 |
| [SEATED_THIGH_PRESS] | B: Seated | B1 |
| [FORWARD_LEAN_CHEST] | B: Seated | B2 |
| [CROSS_LEG_RIDE] | B: Seated | B3 |
| [LOW_CUT_SEATED_SHIFT] | B: Seated | B4 |
| [CASUAL_SPREAD_SEATED] | B: Seated | B5 |
| [KNEES_CHEST_COMPACT] | B: Seated | B6 |
| [SWEAT_CLING] | C: Fabric | C1 |
| [WET_FABRIC_SHIFT] | C: Fabric | C2 |
| [STRETCHED_COLLAR_REVEAL] | C: Fabric | C3 |
| [FABRIC_GAP_SKIN] | C: Fabric | C4 |
| [WAISTBAND_SLIDE] | C: Fabric | C5 |
| [SHOULDER_STRAP_SLIP] | C: Fabric | C6 |
| [TEE_STRETCH_BODY_VISIBLE] | C: Fabric | C7 |
| [TIRED_NECK_EXTENDED] | D: Exhaustion | D1 |
| [RELAXED_SHOULDER_BLADE] | D: Exhaustion | D2 |
| [SLEEPY_HEAD_TILT] | D: Exhaustion | D3 |
| [SLUMP_CHEST_RELEASE] | D: Exhaustion | D4 |
| [HAND_SUPPORT_HEAD] | D: Exhaustion | D5 |
| [EYES_CLOSED_TRUST] | D: Exhaustion | D6 |
| [HOT_DAY_STICKY] | E: Environmental | E1 |
| [AC_NIPPLE_VISIBILITY] | E: Environmental | E2 |
| [FLASH_SMOOTH] | E: Environmental | E3 |
| [WATER_DROP_TRACKS] | E: Environmental | E4 |
| [SUNSCREEN_GREASY_SHEEN] | E: Environmental | E5 |
| [HAIR_MOUTH_PARTED] | E: Environmental | E6 |
| [AC_WIND_SHIFT] | E: Environmental | E7 |
| [HEAT_COLD_TRANSITION] | E: Environmental | E8 |
| [HUMID_BODY_CLING] | E: Environmental | E9 |
| [WET_FABRIC_HK] | E: Environmental | E10 |
| [STEAM_ROOM_HK] | E: Environmental | E11 |
| [COOKING_FLUSH] | E: Environmental | E12 |

### AI Noise Reduction Tokens (Area 06)

| Token | Category | Type |
|-------|----------|------|
| [WIDE_APERTURE_SOFT] | A: Lens | A1 |
| [OLD_LENS_SOFT] | A: Lens | A2 |
| [LOW_LIGHT_SOFT] | A: Lens | A3 |
| [FOCUS_SLIGHT_SOFT] | A: Lens | A4 |
| [TELEPHOTO_SOFT] | A: Lens | A5 |
| [COMPACT_SOFT] | A: Lens | A6 |
| [BACKLIT_GLOW_SOFT] | B: Bloom | B1 |
| [WINDOW_DIFFUSE_SOFT] | B: Bloom | B2 |
| [ORGANIC_LENS_FLARE] | B: Bloom | B3 |
| [SOFT_CATCHLIGHT] | B: Bloom | B4 |
| [SOFT_EDGE_SILHOUETTE] | B: Bloom | B5 |
| [FRONT_FOCUS_SOFT] | C: Focus | C1 |
| [BACK_FOCUS_SOFT] | C: Focus | C2 |
| [EDGE_FOCUS_FALLOFF] | C: Focus | C3 |
| [CORNER_SOFTNESS] | C: Focus | C4 |
| [ENVIRONMENTAL_BLUR] | C: Focus | C5 |
| [SENSOR_SMOOTH_SKIN] | D: Sensor | D1 |
| [SHADOW_GRAIN] | D: Sensor | D2 |
| [SOFT_HIGHLIGHT_CLIP] | D: Sensor | D3 |
| [MINIMAL_COLOR_NOISE] | D: Sensor | D4 |
| [SENSOR_DETAIL_LIMIT] | D: Sensor | D5 |
| [DIRECT_FLASH_FLAT] | E: Flash | E1 |
| [BOUNCE_FLASH_SOFT] | E: Flash | E2 |
| [OFF_CAMERA_FLASH] | E: Flash | E3 |
| [NO_FLASH_INDOOR] | E: Flash | E4 |

### HK-Specific Optical Tokens

| Token | Context |
|-------|---------|
| [MTR_OPTICAL_SOFT] | MTR fluorescent |
| [NEON_OPTICAL_SOFT] | Night market neon |
| [POOL_OPTICAL_SOFT] | Indoor pool |
| [TEA_REST_OPTICAL] | Tea restaurant |
| [FERRY_OPTICAL_SOFT] | Ferry deck night |
| [TEA_REST_STEAM] | 茶餐廳油煙 |
| [FIREWORKS_OPTICAL] | 主題公園煙火 |
| [ROOFTOP_NIGHT_OPTICAL] | 天台夜景 |
| [BUS_INTERIOR_OPTICAL] | 巴士上層 |
| [MONGKOK_TUNNEL_OPTICAL] | 旺角行人隧道 |

### Feed-Level Realism Tokens (Area 07)

| Token | Category | Type |
|-------|----------|------|
| [QUICK_SELFIE] | A: Filler | A1 |
| [FOOD_DOCUMENT] | A: Filler | A2 |
| [RANDOM_SNAPSHOT] | A: Filler | A3 |
| [ACCIDENTAL_BACKGROUND] | A: Filler | A4 |
| [BODY_PART_CLOSEUP] | A: Filler | A5 |
| [SCREENSHOT_REPOST] | A: Filler | A6 |
| [OCTOPUS_RECEIPT] | A: Filler | A7 |
| [GARBAGE_TAG] | A: Filler | A8 |
| [TAKEAWAY_LUNCH] | A: Filler | A9 |
| [QUEUE_TICKET] | A: Filler | A10 |
| [SAME_PLACE_AGAIN] | B: Continuity | B1 |
| [SAME_OUTFIT_REPEAT] | B: Continuity | B2 |
| [SAME_FRIEND_AGAIN] | B: Continuity | B3 |
| [CONTINUING_STORY] | B: Continuity | B4 |
| [RETURNING_AFTER_BREAK] | B: Continuity | B5 |
| [SLEEPING_BUNNY_SNORE] | C: Ugly-Cute | C1 |
| [BAD_ANGLE_STILL_CUTE] | C: Ugly-Cute | C2 |
| [MESSY_MORNING_HAIR] | C: Ugly-Cute | C3 |
| [FOOD_ON_CHEEK] | C: Ugly-Cute | C4 |
| [SQUINT_LAUGH] | C: Ugly-Cute | C5 |
| [SILLY_FACE] | C: Ugly-Cute | C6 |
| [DOUBLE_CHIN_HONEST] | C: Ugly-Cute | C7 |
| [GETTING_READY] | D: Transitional | D1 |
| [TAXI_TRANSIT] | D: Transitional | D2 |
| [WAITING_SOMEONE] | D: Transitional | D3 |
| [POST_EVENT_DOWN] | D: Transitional | D4 |
| [MID_CONVERSATION] | D: Transitional | D5 |
| [CHECKING_PHONE] | D: Transitional | D6 |
| [ENTERING_FRAME] | D: Transitional | D7 |
| [GROUP_PHOTO_CROPPED] | E: Social | E1 |
| [OTHERS_IN_BACKGROUND] | E: Social | E2 |
| [CELEBRATION_MOMENT] | E: Social | E3 |
| [FRIEND_TOOK_PHOTO] | E: Social | E4 |
| [STORY_ABOUT_OTHER] | E: Social | E5 |

### Continuity Tokens

| Token | Type |
|-------|------|
| [OUTFIT_CONTINUITY] | CON_01 |
| [LOCATION_CONTINUITY] | CON_02 |
| [MOOD_CONTINUITY] | CON_03 |
| [NARRATIVE_CONTINUITY] | CON_04 |
| [PERSON_CONTINUITY] | CON_05 |
| [TIME_CONTINUITY] | CON_06 |

### Photodump Sub-Type Tokens

| Token | Type |
|-------|------|
| [PHOTODUMP_SAME_OUTFIT] | Session sub-type |
| [PHOTODUMP_LOCATION] | Session sub-type |
| [PHOTODUMP_MOMENT] | Session sub-type |
| [PHOTODUMP_MIXED] | Session sub-type |

### Upload Rhythm Tokens

| Token | Type |
|-------|------|
| [MORNING_POST] | RHYTHM_A |
| [AFTERNOON_RANDOM] | RHYTHM_B |
| [EVENING_GLAM] | RHYTHM_C |
| [LATE_NIGHT_REFLECT] | RHYTHM_D |
| [WEEKEND_CASUAL] | RHYTHM_E |

### HK-Specific Feed Pattern Tokens

| Token | Context |
|-------|---------|
| [TEA_REST_FEED] | Tea restaurant repeat |
| [MTR_STATION_FEED] | MTR same station |
| [HK_FRIEND_FEED] | Friend group rotation |
| [NIGHT_MARKET_FEED] | Night market documentation |
| [BEACH_DAY_FEED] | Beach day series |
| [STAYCATION_FEED] | Staycation repetition |

---

*ENGINE Module: V16_ANTI_FORMULA_EMOTIONAL_SYSTEM*
*Source: V16_ANTI_FORMULA_RESEARCH (Areas 04-07)*
*Status: READY FOR INTEGRATION*
*Last Updated: 2026*
