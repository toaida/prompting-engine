# WORM_EYE_ENVIRONMENT_SYSTEM.md
### V14.6 Core Module — Environmentally Immersive Low-Angle Perspective
### Status: ACTIVE — Promoted from V14_RESEARCH_v14_6/03

---

## CRITICAL DISTINCTION

### ❌ WRONG: Worm-eye AS glamour
Camera below subject, looking up at body, emphasizing curves/bust/legs. Subject is hero. Environment is backdrop.

### ✅ CORRECT: Worm-eye AS environmental immersion
Camera at ankle-knee height, looking at world from below. Emphasizing scale of environment, smallness of human within it, dominance of atmospheric conditions. Subject is PART of the world. Environment is the hero.

**Low-angle does NOT equal glamour in this system.**
Any use that creates body-display framing (curves emphasis, bust, leg display) violates this system.

Moderation check: *"Is the environment dominant? Is the human small? Is this about atmospheric presence, not body display?"*

---

## 7 ENVIRONMENTAL IMMERSION SYSTEMS

### WRM-01: Foot-Level Realism — Ankle-Knee Camera Height

**Camera height:** Ankle to knee level (15-50cm from ground)
**What viewer sees:** World from ground-level where buildings tower, sky dominates, human scale is small

**Visual behavior:**
- Environment dominates frame: subject small, environment large
- Scale contrast: buildings look massive, human looks tiny
- Ground visible: floor, pavement, feet, shoes, ground texture prominent
- Sky percentage: 50%+ of frame is sky
- Perspective compression: vertical lines converge strongly, buildings appear to lean

**Environmental authority mechanics:**
- Subject small → environment large
- Ground-level POV → viewer feels like standing in the scene
- Ankle-height visibility → human world texture at floor level visible

**Anti-AI logic:** Ground-level is uncommon in AI training data — not a "flattering" angle, it's an immersive angle. Ankle-knee height counters eye-level default.

---

### WRM-02: Environment Scale Amplification — Buildings Tower, Human Small

**Environment so large human becomes minor** — not diminishing, but showing vastness of world and specific smallness of being inside it.

**Visual behavior:**
- Building scale: towers above, leaning against frame edges
- Human placement: lower third or below, small in frame
- Compression: wide-angle feel, environment crowded in
- Dominance: 70-80% environmental frame, 20-30% human
- Emotional weight: world bigger than person — vulnerability without weakness

**Environmental authority mechanics:**
- HK density creates specific compression feel — church-in-grid
- Weather integration: rain dripping from above, wind affecting hair at human height
- Environment as primary visual interest

**Anti-AI logic:** AI frames human as hero, environment as backdrop. Environment scale amplification requires: environment PRIMARY, human SECONDARY.

---

### WRM-03: Sky Dominance — Large Sky %, Atmospheric Layer

**Sky is NOT backdrop — it's the active frame element that imposes emotional register.**

**Visual behavior:**
- Sky percentage: 40-70% of frame is sky
- Atmospheric layer: clouds, pollution, color temperature, weather visible in sky
- Non-human elements primary: building outlines, crane silhouettes, cloud formations
- Emotional register from sky: overcast = contemplative, clear = open, stormy = heavy, golden = nostalgic

**Environmental authority mechanics:**
- Sky as emotional anchor: mood of scene determined by sky, not subject
- Atmospheric perspective: layers of atmosphere visible
- Color temperature from sky: entire frame color-shifted by sky condition

**Anti-AI logic:** AI tends to make sky "nice backdrop" rather than active frame element. Large sky + weather presence requires treating sky as PRIMARY.

---

### WRM-04: Silhouette Elongation — Subject Stretched Toward Sky

**When camera below and subject above (standing, stairs, elevated), subject appears stretched vertically** — NOT sexual elongation, environmental response to scale.

**Visual behavior:**
- Vertical stretch: subject appears taller than reality
- Upward emphasis: face/head toward sky, feet toward ground
- Against sky: subject becomes dark silhouette against bright sky
- Scale relationship: subject bridges ground and sky
- Elongation direction: up toward sky, NOT laterally toward camera

**Environmental authority mechanics:**
- Subject connects earth and sky: standing figure is bridge between ground and atmosphere
- Silhouette against sky: subject becomes atmospheric element, not framed subject
- Scale demonstration: silhouetted against large sky, subject demonstrates sky scale

**Anti-AI logic:** AI interprets vertical stretch as "unrealistic" and corrects. This system treats stretch as environmental response — subject stretching toward environment, not being distorted for glamour.

**CRITICAL MODERATION:** Vertical stretch toward sky = environmental connectivity, NOT sexual elongation. Subject silhouetted, not framed for body.

---

### WRM-05: Walking Realism — Ground-Level Walking Shot

**Camera captures walking from low angle — feet hitting ground, weight transfer, human in motion through space.**

**Visual behavior:**
- Ground visible: pavement, shoes, feet, ground texture
- Walking motion: one foot possibly lifted, weight mid-transfer
- Low angle: camera at ankle-knee height
- Environment: ground plane visible, sense of walking through space
- Realism: any person walking — not model-walking, just walking

**Environmental authority mechanics:**
- Ground-plane emphasis: where human walks, what surface
- Motion captured: human in motion, not static — natural, unplanned
- Scale reference: ground visibility establishes environment scale

**Anti-AI logic:** AI tends to capture "standing and posing." Walking shots require motion blur, imperfect framing, ground visibility — elements AI doesn't default to.

---

### WRM-06: Accidental Tourist-Photo Energy — Unplanned Upward Angle

**Camera angle feels unplanned — like someone held camera at waist level and accidentally pointed up, awkward but authentic.**

**Visual behavior:**
- Awkward framing: not composed, not rule-of-thirds, slightly off
- Unplanned feel: like camera raised without thinking
- Tourist energy: "I was there and the building was big so I pointed up"
- Imperfect: not polished, not professional — authentic
- Composition: environment dominates, human small, awkward angle

**Environmental authority mechanics:**
- No professionalism: tourist photos aren't trying to be good — they're documenting
- "Look how big this was": exactly what V14.6 needs
- Accidental composition = real documentation

**Anti-AI logic:** AI tends to compose "correctly" — rule-of-thirds, balanced, professional. Tourist accidental energy requires explicit imperfectness.

---

### WRM-07: Atmospheric Weight — Environment Emotional Authority

**When environment is larger than human in frame, environment GAINS emotional authority.**

**Visual behavior:**
- Environment frame dominance: 70%+ environment, <30% human
- Emotional register: environment mood dominates scene mood
- Scale consequence: human small → environment significant
- Weather/light: environmental conditions are frame's primary visual interest

**Environmental authority mechanics:**
- Environment as emotional protagonist: NOT backdrop, but protagonist
- Human as element: human is part of environment, not separate from it
- Emotional weight from scale: by making environment large, scene gains weight
- Contemplative quality: big environment = contemplative mood = introspective moment

**Anti-AI logic:** AI makes human "pop" — bright, sharp, significant. Atmospheric weight requires human to be quiet, small, atmospheric, not competing with environment.

---

## V14.6 UPGRADE MODULES

### WRM-SYSTEM-01: GROUND_LEVEL_IMMERSION
**Trigger:** Environment dominant (building/sky/pavement scale) OR emotional weight requires world larger than human
**Prompt grammar:**
```
[CAMERA HEIGHT: ground level ankle-knee]
— [environment dominates frame]
— [human small in frame]
— [ground plane visible]
— [sky percentage: 40-70%]
```

### WRM-SYSTEM-02: ENVIRONMENT_SCALE_REVERSAL
**Trigger:** Emotional register contemplative/heavy/awe OR environment architecturally significant
**Prompt grammar:**
```
[ENVIRONMENT PRIMARY]
— [human secondary: small atmospheric not competing]
— [scale contrast: environment large human small]
— [70-80% environmental frame]
— [compression: environment crowded in human tiny]
```

### WRM-SYSTEM-03: SKY_DOMINANCE
**Trigger:** Overcast, clear, stormy, golden hour, or any moment where sky mood affects scene
**Prompt grammar:**
```
[SKY PRIMARY: 40-70% of frame]
— [weather active in sky: clouds/pollution/haze]
— [color temperature from sky]
— [non-human elements: buildings cranes clouds]
```

### WRM-SYSTEM-04: SILHOUETTE_VERTICAL
**Trigger:** Subject above camera (standing, stairs, elevated) AND sky is large
**Prompt grammar:**
```
[SILHOUETTE AGAINST SKY]
— [vertical stretch: subject toward sky]
— [face/head toward sky feet toward ground]
— [scale: subject bridges ground and sky]
— [NEVER lateral stretch toward camera for display]
```

### WRM-SYSTEM-05: WALKING_MOTION_CAPTURE
**Trigger:** Scene is about transit, movement, going somewhere, environmental transit
**Prompt grammar:**
```
[WALKING CAPTURE: ground visible]
— [motion: weight transfer mid-step]
— [low angle: ankle-knee height]
— [realism: any walking not model-walking]
```

### WRM-SYSTEM-06: TOURIST_ACCIDENTAL_COMPOSITION
**Trigger:** Moment is about being present in massive environment (building/mountain/harbor/landmark)
**Prompt grammar:**
```
[TOURIST COMPOSITION: unplanned]
— [no rule-of-thirds awkward framing]
— [upward angle: accidental pointing up]
— [environment proves scale: building/mountain/harbor large]
— [authenticity: not professional just real]
```

### WRM-SYSTEM-07: ATMOSPHERIC_WEIGHT
**Trigger:** Emotional register requires contemplation/heaviness/awe/nostalgia OR weather/time creates mood
**Prompt grammar:**
```
[ATMOSPHERIC WEIGHT: environment protagonist]
— [human quiet: small atmospheric not competing]
— [emotional weight from scale: big environment = weighted scene]
— [contemplative mood: big world small human time passing]
```

---

## ANTI-AI LOGIC

1. **Eye-level default prevention:** AI defaults to eye-level for "normal" shots. Ground-level requires explicit override.
2. **Human-as-subject prevention:** AI defaults human-as-hero, environment-as-backdrop. Reversal required.
3. **Composition correctness prevention:** AI composes "correctly." Tourist accidental energy requires explicit incorrectness.
4. **Perfect framing prevention:** AI frames to make subject look good. Ground visibility + sky dominance counters optimization.
5. **Vertical stretch rejection:** AI interprets vertical stretch as "error." Treat as environmental response, not distortion.
6. **Body-emphasis prevention:** AI uses low angle for curves/bust/legs. Ground-level + environment-dominance prevents emphasis.

---

## MODERATION: CRITICAL SAFETY DISTINCTION

**All 7 systems = HIGH SAFETY** when used correctly.

The key is: worm-eye in V14.6 is about **ENVIRONMENTAL IMMERSION, not GLAMOUR PRESENTATION.**

❌ VIOLATION: Low angle + body-display (curves, bust emphasis, leg display) = glamour = NOT permitted
✅ PERMITTED: Low angle + environment-dominance + human-small = atmospheric immersion

**Per-module moderation:**
- WRM-01 Ground-Level: ✅ No body-display, subject small
- WRM-02 Scale Reversal: ✅ Environment primary, human atmospheric
- WRM-03 Sky Dominance: ✅ Sky is frame element, not body
- WRM-04 Silhouette Vertical: ✅ Stretch toward sky, NOT toward camera for display
- WRM-05 Walking: ✅ Functional, not performative
- WRM-06 Tourist Accidental: ✅ Anti-professional, anti-glamour
- WRM-07 Atmospheric Weight: ✅ Environment is protagonist

---

## CROSS-REFERENCE

- **ENVIRONMENT_EXPANSION_SYSTEM.md** — Ground-level works best with D-series (Weather) and E-series (Transit): wet pavement reflections, typhoon rain shelter, post-rain street
- **ENVIRONMENTAL_COLOR_MEMORY_SYSTEM.md** — CineStill + ground-level = electric HK night immersion; overcast + Fuji Pro 400H; clear night + moonlight retention
- **CAMERA_AWARENESS_SYSTEM.md** — Level 3-4 natural for worm-eye (documentary/street)
- **MEMORY_CAPTURE_SYSTEM.md** — Incomplete framing (System 1) natural pairing — worm-eye causes accidental crop
