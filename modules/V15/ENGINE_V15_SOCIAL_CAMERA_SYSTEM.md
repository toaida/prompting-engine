# ENGINE_V15_SOCIAL_CAMERA_SYSTEM.md

## V15 Core Module — Camera Operator Library V2
### AREAS: 01 (Social Camera) | Status: READY FOR INTEGRATION

---

## PURPOSE

The camera operator system models the photographer as an active social agent whose behavior, relationship to subject, and technical skill fundamentally alter the image output. Human operators create image characteristics no automated system replicates: fingerprints of human consciousness, human error, and human relationship.

---

## KEY CONCEPTS

**Operator Type** determines authenticity, technical quality, relationship warmth, and failure frequency.

**Social Distance** (5 levels) determines framing geometry and subject comfort.

**Photographer Presence** (5 levels) determines subject behavior — from invisible candid to fully directed performance.

---

## CAMERA_OPERATOR_LIBRARY_V2

### Core Operators (HK Context)

**OP_01: INTIMATE PARTNER**
```
Relationship: High emotional investment, physical comfort, intimate settings
Behavioral: Downward angle of affection, rapid burst, genuine expressions mid-laugh
Technical: Portrait mode aggressive, 1.5-2x zoom (beauty zoom), front camera common
Failures: Partial face cut, ghosting low light, eye-blink caught mid-motion
Authenticity: HIGH | Technical: MEDIUM | Warmth: HIGH | Failures: MEDIUM
Token: [OP_INTIMATE_PARTNER]
```

**OP_02: GIRLFRIEND AMATEUR**
```
Relationship: Female friend who "takes good photos," conscious direction
Behavioral: Directs actively, mental pose library, above-angle flattering
Technical: Portrait mode correct, rule-of-thirds, natural window light
Failures: Over-processing, over-cropped, sterile but technically correct
Authenticity: MEDIUM | Technical: HIGH | Warmth: MEDIUM | Failures: LOW
Token: [OP_GIRLFRIEND_AMATEUR]
```

**OP_03: BOYFRIEND CLUELESS**
```
Relationship: Takes photos because asked, minimal composition interest
Behavioral: Few shots, full wide angle, no direction given
Technical: No portrait mode, smudged lens, vertical orientation default
Failures: Subject tiny in vast space, motion blur, horizon tilt
Authenticity: MEDIUM | Technical: LOW | Warmth: LOW | Failures: HIGH
Token: [OP_BOYFRIEND_CLUELESS]
```

**OP_04: TOURIST STRANGER**
```
Relationship: Complete stranger, transactional favor, hyper-aware subject
Behavioral: Subject stiffens, countdown, full wide, rarely portrait mode
Technical: Both hands wobble, may switch to front camera accidentally
Failures: Frontal face-on pose, forehead chopped, extreme wide distortion
Authenticity: LOW | Technical: LOW | Warmth: LOW | Failures: HIGH
Token: [OP_TOURIST_STRANGER]
```

**OP_05: STREET DOCUMENTARY**
```
Relationship: Photographer separate from subject, observer not participant
Behavioral: Long lens/cropped, no interaction, shooting quickly
Technical: 2-5x zoom, burst, natural ambient light
Failures: Eye-line diverted, motion blur, face partially turned
Authenticity: HIGH | Technical: MEDIUM | Warmth: NONE | Failures: MEDIUM
Token: [OP_STREET_DOCUMENTARY]
```

**OP_06: SELFIE SPECIALIST**
```
Relationship: Subject operates camera themselves, maximum self-awareness
Behavioral: Front camera, "good side" maximally exploited, multiple attempts
Technical: Beauty mode, arms extended fixed distance, selfie stick
Failures: Beauty mode too aggressive, both arms visible, sterile expression
Authenticity: LOW | Technical: MEDIUM | Warmth: NONE | Failures: HIGH
Token: [OP_SELFIE_SPECIALIST]
```

**OP_07: CREATIVE COLLABORATOR**
```
Relationship: Back-and-forth co-creation, shared aesthetic vision
Behavioral: Mutually directing, photographer shows screen, iteration
Technical: Rear camera portrait, deliberate light scouting, bracketing
Failures: Pose fatigue, overdirected, overcomposed background
Authenticity: HIGH | Technical: HIGH | Warmth: HIGH | Failures: LOW
Token: [OP_CREATIVE_COLLABORATOR]
```

**OP_08: UNDERCOVER SHOT**
```
Relationship: Subject unaware of capture, photographer concealing
Behavioral: Phone low at hip/chest, silent shutter, burst
Technical: Screen-off, front camera concealment, no flash
Failures: Extreme angles, subject partially cropped, motion blur
Authenticity: HIGHEST | Technical: LOW | Warmth: NONE | Failures: HIGH
Token: [OP_UNDERCOVER_SHOT]
```

**OP_09: ELDER RELATIVE**
```
Relationship: Maximum emotional investment, minimal skill
Behavioral: Full arm extension, "say cheese," many photos taken
Technical: Full wide, flash auto, vertical orientation confused
Failures: Subject tiny, blinking, flash washout, cracked lens artifact
Authenticity: MEDIUM | Technical: LOW | Warmth: HIGHEST | Failures: HIGH
Token: [OP_ELDER_RELATIVE]
```

**OP_10: PROFESSIONAL HIRE**
```
Relationship: Performance pressure, staged energy, skilled but cold
Behavioral: Directs everything, subject waits passively, fast shooting
Technical: Professional lighting, RAW, backup equipment
Failures: Emotionally dead, stiff from direction, overretouched
Authenticity: LOW | Technical: HIGHEST | Warmth: LOW | Failures: LOW
Token: [OP_PROFESSIONAL_HIRE]
```

**OP_11: DRUNK NIGHT PHOTOGRAPHER**
```
Relationship: Impaired judgment, chaotic celebration memories
Behavioral: Unpredictable angles, shouts instructions, 50 photos succession
Technical: Flash compulsively, high ISO, no review
Failures: Severe motion blur, flash washout, red-eye, frame chaos
Authenticity: HIGHEST | Technical: LOWEST | Warmth: HIGH | Failures: HIGHEST
Token: [OP_DRUNK_NIGHT]
```

**OP_12: LONG DISTANCE PARTNER**
```
Relationship: Remote partner longing, photography as love act
Behavioral: Intentional dressing, considered composition, front camera bedroom
Technical: Self-timer full body, soft lamp lighting, phone propped
Failures: Mirror reflection captures phone, bedroom context visible
Authenticity: HIGH | Technical: MEDIUM | Warmth: HIGHEST | Failures: MEDIUM
Token: [OP_LONG_DISTANCE]
```

### HK-Specific Operators

**OP_13: MTR PLATFORM COMMUTER** `[HK]`
```
Relationship: Bored transit documentation, liminal space photography
Behavioral: Waits for train, captures strangers, long exposure crowds
Technical: Fluorescent platform light, shoots through glass reflections
Failures: Platform green-yellow cast, train motion blur, stranger sharp unexpectedly
Token: [OP_MTR_PLATFORM]
```

**OP_14: LATE-NIGHT TAXI** `[HK]`
```
Relationship: Backseat intimate group, neon reflections, cramped space
Behavioral: Backseat selfie with friends, window neon shots, video common
Technical: Flash blocked by hand, high ISO, window glass reflection
Failures: Interior over exterior, neon color contamination, driver silhouette
Token: [OP_LATE_NIGHT_TAXI]
```

**OP_15: ROOFTOP FRIEND** `[HK]`
```
Relationship: Deliberate climb, skyline as real subject, safety concern
Behavioral: Subject at edge, sunset/night timing, group shots cramped
Technical: HDR, self-timer, night mode
Failures: Skyline over/under exposed, railing bisecting frame, wind hair blur
Token: [OP_ROOFTOP_FRIEND]
```

**OP_16: CONVENIENCE STORE** `[HK]`
```
Relationship: 7-Eleven/gsr ritual pre-night-out, fluorescent social hub
Behavioral: Holding snack/drink, cramped aisle, group selfie
Technical: Fluorescent, front camera, beauty mode, flash fired
Failures: Green-white cast, refrigerator light backlit, GSR logo visible
Token: [OP_CONVENIENCE_STORE]
```

**OP_17: FERRY DECK** `[HK]`
```
Relationship: Harbour iconic documentation, tourist and local mixed
Behavioral: Subject against harbour, sunset timing, selfie stick over water
Technical: Rear camera, panorama, portrait mode fails on boat
Failures: Boat motion blur, salt haze, subject tiny against massive harbour
Token: [OP_FERRY_DECK]
```

**OP_18: INDOOR PLAYGROUND CROUCH** `[HK]`
```
Relationship: Parent documenting chaotic children, low angle struggle
Behavioral: Crouching/kneeling, burst mode, waiting for attention
Technical: Portrait mode attempted, low angle flare, high ISO
Failures: Ceiling flare, up-shot distortion, ball pit clutter, grain
Token: [OP_PLAYGROUND_CROUCH]
```

**OP_19: WEDDING GUEST** `[HK]`
```
Relationship: Personal memories at Chinese banquet 筵席, cultural event
Behavioral: Shooting over heads, capturing couple, video of ceremony
Technical: Flash disabled, high angle, auto white balance confused
Failures: Guest heads cropping, spotlight hot spot, red-gold clutter
Token: [OP_WEDDING_GUEST]
```

**OP_20: AIRPORT DEPARTURE** `[HK]`
```
Relationship: Liminal departure moment, goodbye happening here
Behavioral: Boarding gate context, passport/boarding pass props, exhausted traveler
Technical: Departure hall signage, portrait mode, early/late timing
Failures: Fluorescent green cast, departure board visible, reflection in glass
Token: [OP_AIRPORT_DEPARTURE]
```

**OP_21: BEACH FRIEND-BEHIND** `[HK]`
```
Relationship: Walking figure against sea/sky, casual beach documentation
Behavioral: Photographer behind, three-quarter walking view, friends calling
Technical: Sky as background, 2-3x zoom, silhouette common
Failures: Sky over/under exposed, harsh mid-day shadows, Hong Kong density visible
Token: [OP_BEACH_BEHIND]
```

**OP_22: ESCALATOR FRIEND-ABOVE** `[HK]`
```
Relationship: Mid-Levels Escalator iconic documentation, vertical transit
Behavioral: Above shooting down, escalator movement, SOHO street behind
Technical: 2-3x zoom, vertical format, backlit situations
Failures: Escalator steps diagonal lines, other riders visible, handrail bisecting
Token: [OP_ESCALATOR_FRIEND]
```

---

## SOCIAL DISTANCE TAXONOMY

**SD_01: INTIMATE DISTANCE** (< 45cm)
```
Physical: Arm's reach, face fills frame, breathing audible
Behavior: No performance, breath may fog lens, eyes direct comfortable
Image: Face dominant, no context, skin texture visible, wide-angle distortion
Prompt: "intimate distance less than 45cm, face fills frame completely,
        breath visible, skin texture with pore detail, physical proximity"
Token: [SD_INTIMATE]
```

**SD_02: PERSONAL DISTANCE** (45-120cm)
```
Physical: Arm's length, waist-up framing possible
Behavior: Aware of camera, natural smile for specific person
Image: Waist to head, face primary, shoulders visible, bokeh on background
Prompt: "personal distance arm's length, waist-up framing,
        natural smile for photographer relationship"
Token: [SD_PERSONAL]
```

**SD_03: SOCIAL DISTANCE** (120-360cm)
```
Physical: Several feet, full figures possible, group photos
Behavior: Aware but less focused, interacts with people not camera
Image: Full figure(s), environment 40-60%, multiple people clustered
Prompt: "social distance several feet, full figures with environmental context,
        subjects oriented to each other not camera"
Token: [SD_SOCIAL]
```

**SD_04: PUBLIC DISTANCE** (360cm+)
```
Physical: Small figure in vast environment, stranger to subject
Behavior: Unaware or indifferent, walking/waiting/moving
Image: Subject small, face detail absent, environment dominant
Prompt: "public distance small scale human in vast environment,
        street photography documentary distance"
Token: [SD_PUBLIC]
```

**SD_05: TECHNICAL DISTANCE** (Selfie Inversion)
```
Physical: Subject operates camera, fixed arm's length + face distance
Behavior: Maximum self-awareness, "good side" exploited, micro-expressions rehearsed
Image: Face fills/extends to edges, both arms visible, eyes locked with lens
Prompt: "selfie distance front camera, subject controlling camera themselves,
        maximum self-awareness, controlled examined expression"
Token: [SD_SELFIE]
```

---

## PHOTOGRAPHER PRESENCE SYSTEM

**PP_01: INVISIBLE** — Subject unaware
```
Behavior: Completely natural, no awareness, no adjustment
Marks: Extreme angles, no eye contact, environmental dominance
Prompt: "photographer invisible subject unaware, genuine natural behavior"
Token: [PP_INVISIBLE]
```

**PP_02: MINIMALLY VISIBLE** — Aware but not interacting
```
Behavior: Aware but continues activity, occasional glance at camera
Marks: Occasional eye contact, slightly composed, some environmental awareness
Prompt: "subject minimally aware photographer observing not interacting,
        slightly composed but not posed"
Token: [PP_MINIMAL]
```

**PP_03: ACTIVE SOCIAL** — Photographer participates
```
Behavior: Trust, warmth, photographer calls for attention, genuine affection
Marks: Subject laughing at photographer, warm body language
Prompt: "photographer actively participating social situation,
        subject responding with genuine warmth to person holding camera"
Token: [PP_ACTIVE_SOCIAL]
```

**PP_04: DIRECTORIAL** — Photographer commands
```
Behavior: Subject follows instructions, pose/expression directed
Marks: Specific pose, expression on command, no relational interaction
Prompt: "photographer directly commanding subject through verbal instruction,
        mechanical or forced response"
Token: [PP_DIRECTORIAL]
```

**PP_05: COMPLETE PERFORMANCE** — Subject knows final use
```
Behavior: Performing representation for unseen audience
Marks: Practiced pose, "the smile," intentional clothing/grooming
Prompt: "subject fully aware image purpose, performing idealized self"
Token: [PP_PERFORMANCE]
```

---

## PROMPT GRAMMAR

```
[OPERATOR]: Shot by [operator_type] [relationship_context]
[DISTANCE]: [social_distance_token]
[PRESENCE]: [photographer_presence_token]
[CONTEXT]: [HK_context_if_applicable]
[TECHNICAL]: [camera_habits] [failure_type_if_present]
[BEHAVIORAL]: [subject_behavior_signature]
[EXAMPLE]: [prompt_grammar_from_library]
```

---

## TOKEN LIBRARY

```
OPERATORS:
[OP_INTIMATE_PARTNER] [OP_GIRLFRIEND_AMATEUR] [OP_BOYFRIEND_CLUELESS]
[OP_TOURIST_STRANGER] [OP_STREET_DOCUMENTARY] [OP_SELFIE_SPECIALIST]
[OP_CREATIVE_COLLABORATOR] [OP_UNDERCOVER_SHOT] [OP_ELDER_RELATIVE]
[OP_PROFESSIONAL_HIRE] [OP_DRUNK_NIGHT] [OP_LONG_DISTANCE]
[OP_MTR_PLATFORM] [OP_LATE_NIGHT_TAXI] [OP_ROOFTOP_FRIEND]
[OP_CONVENIENCE_STORE] [OP_FERRY_DECK] [OP_PLAYGROUND_CROUCH]
[OP_WEDDING_GUEST] [OP_AIRPORT_DEPARTURE] [OP_BEACH_BEHIND]
[OP_ESCALATOR_FRIEND]

DISTANCE:
[SD_INTIMATE] [SD_PERSONAL] [SD_SOCIAL] [SD_PUBLIC] [SD_SELFIE]

PRESENCE:
[PP_INVISIBLE] [PP_MINIMAL] [PP_ACTIVE_SOCIAL] [PP_DIRECTORIAL] [PP_PERFORMANCE]
```

---

## MODERATION PROFILE

**Operator Selection Guide:**
- Maximum authenticity + interesting failures: OP_08, OP_11
- Clean directed imagery: OP_07, OP_10
- Relationship warmth + moderate failures: OP_01, OP_12
- HK-specific authenticity: OP_13-22

**Cross-Reference:** Combines with ENGINE_V15_BAD_PHOTO_REALISM_SYSTEM for failure type injection. HK operators marked with `[HK]` require environmental verification tokens.

**Distribution Target:**
- Intimate/Personal distance: 50-60%
- Social/Public distance: 30-40%
- Selfie/Technical: 10-15%

---

*V15 Module: ENGINE_V15_SOCIAL_CAMERA_SYSTEM.md*
*Status: READY FOR INTEGRATION*
*Dependencies: ENGINE_V15_BAD_PHOTO_REALISM_SYSTEM (failure types)*
