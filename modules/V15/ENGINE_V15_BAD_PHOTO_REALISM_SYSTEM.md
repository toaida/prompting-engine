# ENGINE_V15_BAD_PHOTO_REALISM_SYSTEM.md

## V15 Core Module — Imperfect Photo System
### AREA: 02 (Bad Photo Realism) | Status: READY FOR INTEGRATION

---

## PURPOSE

The bad photo realism system identifies specific failure modes that signal authentic human capture rather than professional construction. Imperfect photos feel more real because the human visual system is trained on billions of imperfect amateur photographs. Technical perfection reads as constructed; imperfection is the signature of the real.

---

## KEY CONCEPTS

**Failure Type** = Mechanical Cause + Visual Signature + Authenticity Signal

**Combined Failure Patterns** = Clusters of failures that identify specific capture contexts

**Authenticity Weight** = Each failure type carries different authenticity density

---

## IMPERFECT_PHOTO_SYSTEM — 26 FAILURE TYPES

### Failure Category A: Framing Failures

**FAIL_01: ACCIDENTAL CROP**
```
Cause: Photographer failed to frame subject correctly
Visual: Face cut at edge, body truncated at waist/knee, hand severed at wrist
Authenticity: MEDIUM — non-professional evidence
Prompt: "accidental face crop with forehead cut off by frame edge,
        asymmetric framing suggesting inattention, amateur framing error"
Token: [FAIL_ACCIDENTAL_CROP]
```

**FAIL_21: OUT OF FRAME**
```
Cause: Subject moved before/during exposure or photographer misframed
Visual: Subject missing entirely, only environment captured
Authenticity: HIGH — timing failure evidence
Prompt: "out of frame with subject completely missing,
        only environment captured, timing error"
Token: [FAIL_OUT_OF_FRAME]
```

### Failure Category B: Motion Failures

**FAIL_02: MOTION BLUR (Subject)**
```
Cause: Shutter too slow to freeze subject motion
Visual: Body/face smeared, edges trail behind movement, hair creates motion trails
Authenticity: HIGH — impossible to pose
Prompt: "motion blur from subject movement during exposure,
        body smeared with trails, hair creating motion trails,
        low light interior no flash"
Token: [FAIL_MOTION_BLUR_SUBJECT]
```

**FAIL_03: MOTION BLUR (Camera Shake)**
```
Cause: Photographer hand moved during exposure
Visual: Entire frame blurs uniformly, diagonal/rotational direction
Authenticity: HIGH — unique handheld fingerprint
Prompt: "uniform camera shake blur affecting entire frame,
        diagonal rotational blur direction revealing photographer tremor,
        handheld smartphone fingerprint"
Token: [FAIL_MOTION_BLUR_CAMERA]
```

**FAIL_22: CAMERA DROP/SHAKE**
```
Cause: Camera jostled/dropped during exposure
Visual: Chaotic blur not in consistent direction, parts displaced
Authenticity: HIGH — physical trauma evidence
Prompt: "camera dropped or shaken during exposure creating chaotic blur,
        entire frame affected, physical camera trauma"
Token: [FAIL_CAMERA_DROP]
```

### Failure Category C: Exposure Failures

**FAIL_04: SEVERE UNDEREXPOSURE**
```
Cause: Camera metered for background not subject
Visual: Subject silhouette, face near-black, background correctly exposed
Authenticity: MEDIUM — no fill flash evidence
Prompt: "severe underexposure with subject silhouette shape only,
        background correctly exposed bright, no fill flash used"
Token: [FAIL_UNDEREXPOSURE]
```

**FAIL_05: SEVERE OVEREXPOSURE**
```
Cause: Camera metered for subject or flash fired in dark
Visual: Face white, highlights clipped, background blown to white
Authenticity: MEDIUM — one-way failure unrecoverable
Prompt: "severe overexposure with subject face completely white,
        highlights clipped unrecoverable, flash washout"
Token: [FAIL_OVEREXPOSURE]
```

### Failure Category D: Focus Failures

**FAIL_09: AUTOFOCUS MISS**
```
Cause: Camera locked onto wrong area (background not subject)
Visual: Subject face soft/out of focus, background sharp, eyes particularly soft
Authenticity: MEDIUM-HIGH — no verification evidence
Prompt: "autofocus missed subject with camera locking onto background,
        subject soft while environment sharp"
Token: [FAIL_AUTOFOCUS_MISS]
```

**FAIL_18: FOCUS HUNT**
```
Cause: Camera still searching when shutter fired
Visual: Multiple focal planes, inconsistent sharpness across frame
Authenticity: MEDIUM — impatient capture evidence
Prompt: "focus hunt with camera searching not settling before capture,
        multiple focal planes visible"
Token: [FAIL_FOCUS_HUNT]
```

### Failure Category E: Technical Artifact Failures

**FAIL_06: INCORRECT WHITE BALANCE**
```
Cause: Auto white balance confused by mixed lighting
Visual: Skin orange or blue, white objects carrying color cast, fluorescent flicker
Authenticity: LOW — consumer camera artifact
Prompt: "incorrect white balance with skin tones shifted orange or blue,
        mixed interior lighting confusion"
Token: [FAIL_WHITE_BALANCE]
```

**FAIL_10: ISO NOISE/GRAIN**
```
Cause: High ISO in low light situations
Visual: Visible grain throughout, color noise (red/blue specks), detail loss
Authenticity: MEDIUM-HIGH — real low light evidence
Prompt: "high ISO grain throughout entire frame, color noise,
        sensor struggling in low light"
Token: [FAIL_ISO_GRAIN]
```

**FAIL_19: COLOR FRINGING**
```
Cause: Lens chromatic aberration at high-contrast edges
Visual: Purple/green halos along edges, strongest at corners
Authenticity: LOW — lens quality signature
Prompt: "chromatic aberration with purple or green halos along edges,
        cheap smartphone lens failing"
Token: [FAIL_CHROMATIC_ABERRATION]
```

### Failure Category F: Lens/Optical Failures

**FAIL_07: EXTREME WIDE ANGLE DISTORTION**
```
Cause: Subject too close to wide-angle lens
Visual: Nose enlarged, face edges stretched, forehead extended, chin compressed
Authenticity: MEDIUM — specific smartphone failure
Prompt: "extreme wide angle lens distortion from subject too close,
        nose significantly larger, facial features stretched"
Token: [FAIL_WIDE_DISTORTION]
```

**FAIL_12: LENS FLARE/GHOST**
```
Cause: Light entered at angle creating internal reflections
Visual: Bright streak across diagonal, ghost image of light source
Authenticity: LOW — could be intentional
Prompt: "lens flare artifact with bright streak across diagonal,
        ghost image of sun, shooting toward light without shielding"
Token: [FAIL_LENS_FLARE]
```

**FAIL_20: DUST/SENSOR SPOT**
```
Cause: Dust on sensor creating dark circular spot
Visual: Dark spot at consistent position, same in every image
Authenticity: MEDIUM — maintenance failure
Prompt: "dust or sensor spot creating dark circular blemish,
        same position every image from device"
Token: [FAIL_SENSOR_SPOT]
```

### Failure Category G: Flash Failures

**FAIL_11: FLASH SYNC FAILURE**
```
Cause: Flash fired but shutter too slow
Visual: Dark image with bright strip where flash hit
Authenticity: MEDIUM — amateur flash use
Prompt: "flash sync failure with bright strip of flash across frame
        while rest remains dark, shutter too slow"
Token: [FAIL_FLASH_SYNC]
```

**FAIL_15: RED-EYE**
```
Cause: Flash reflects off dilated pupils
Visual: Eyes bright red, face otherwise normally lit
Authenticity: LOW-MEDIUM — fixable but endemic
Prompt: "flash red-eye with eyes showing bright red pupils,
        built-in flash in low light"
Token: [FAIL_RED_EYE]
```

### Failure Category H: Processing Failures

**FAIL_16: JPEG COMPRESSION ARTIFACTS**
```
Cause: Aggressive compression or social media pipeline
Visual: Blocky artifacts in uniform areas, mosquito noise, color banding
Authenticity: MEDIUM — social media transit evidence
Prompt: "JPEG compression artifacts with blocky artifacts in sky/walls,
        evidence of social media upload/download pipeline"
Token: [FAIL_JPEG_COMPRESSION]
```

**FAIL_17: DEPTH MAP FAILURE**
```
Cause: Portrait mode edge detection failed
Visual: Hair merges with background, shoulder blends, halos at edges
Authenticity: MEDIUM — computational photography only
Prompt: "portrait mode depth map failure with hair merging into background,
        smartphone computational failure only"
Token: [FAIL_PORTRAIT_MODE_FAILURE]
```

### Failure Category I: Other Failures

**FAIL_08: FINGER BLOCKING LENS**
```
Cause: Finger/thumb accidentally covered part of lens
Visual: Curved finger pad shape at corner/edge, in focus (at lens distance)
Authenticity: VERY HIGH — requires human hold
Prompt: "finger accidentally blocking portion of lens creating dark curved shape,
        purely amateur artifact"
Token: [FAIL_FINGER_BLOCK]
```

**FAIL_13: DOUBLE EXPOSURE/GHOST**
```
Cause: Two images captured in one frame
Visual: Subject appears twice, semi-transparent overlay
Authenticity: MEDIUM — malfunction evidence
Prompt: "double exposure ghost overlap with subject appearing twice,
        semi-transparent overlay of two captures"
Token: [FAIL_DOUBLE_EXPOSURE]
```

**FAIL_14: TILTED HORIZON**
```
Cause: Camera held at angle
Visual: Horizon not level, architectural features angle, diagonal tension
Authenticity: MEDIUM — could be intentional
Prompt: "tilted horizon with camera held at angle making nothing level,
        amateur hold with no level indicator"
Token: [FAIL_TILTED_HORIZON]
```

### HK-Specific Failures

**FAIL_23: NEON SIGN REFLECTION** `[HK]`
```
Cause: Dense HK neon signage in wet conditions
Visual: Pink/blue/green neon reflections bleeding onto subjects, puddle doubling
Authenticity: HIGH — location-specific
Prompt: "Hong Kong neon sign reflection contamination with pink blue green neon
        from dense signage reflecting on wet street, authentic 夜市 atmosphere"
Token: [FAIL_NEON_HK]
```

**FAIL_24: HUMIDITY HAZE/HEAT DISTORTION** `[HK]`
```
Cause: HK summer humidity + temperature differential
Visual: Distant buildings washed out, heat shimmer, wavy distortion
Authenticity: HIGH — environment-specific
Prompt: "humidity haze and heat distortion specific to Hong Kong summer,
        distant buildings washed out, heat shimmer visible"
Token: [FAIL_HUMIDITY_HAZE_HK]
```

**FAIL_25: WET MARKET FLUORESCENT** `[HK]`
```
Cause: Mixed fluorescent/sodium vapor in 街市
Visual: Extreme green-yellow cast, fish/water reflections, skin unrecognizable
Authenticity: HIGH — location-specific
Prompt: "wet market fluorescent contamination specific to Hong Kong 街市,
        extreme green-yellow color cast, fish water wet floor reflections"
Token: [FAIL_WET_MARKET_HK]
```

**FAIL_26: DENSE BUILDING BACKGROUND CLASH** `[HK]`
```
Cause: HK extreme building density confuses portrait mode
Visual: Multiple bokeh sizes indicating multiple distance layers
Authenticity: HIGH — density-specific
Prompt: "dense building background clash specific to Hong Kong urban environment,
        multiple building layers at different distances, bokeh confusion"
Token: [FAIL_DENSE_BUILDING_HK]
```

---

## COMBINED FAILURE PATTERNS

**PATTERN_01: THE NIGHT OUT SEQUENCE**
```
Failures: ISO grain + red-eye + motion blur + camera shake + accidental crop + color fringing + JPEG artifacts
Context: Low light bar/club, alcohol impairment
Prompt: "night out sequence with high ISO grain throughout, flash red-eye
        in dark bar, motion blur from unsteady hands, camera shake rotation,
        accidental face crops, JPEG artifacts from social upload"
Token: [PATTERN_NIGHT_OUT]
```

**PATTERN_02: THE BATHROOM MIRROR SELFIE**
```
Failures: Beauty mode over-smoothing + chin-up distortion + nose enlargement + finger blocking + phone in frame
Context: Front camera, intimate space
Prompt: "bathroom mirror selfie with beauty mode aggressive smoothing,
        extreme chin-up angle distorting proportions, nose enlarged,
        mirror reflection capturing phone in frame"
Token: [PATTERN_BATHROOM_SELFIE]
```

**PATTERN_03: THE TOURIST GROUP SHOT**
```
Failures: Face crops + extreme wide angle + someone blinking + horizon tilt + background chaos + flash washout
Context: Stranger with camera
Prompt: "tourist group shot with face crops from stranger not knowing
        who to include, extreme wide angle from close proximity,
        someone blinking from countdown, horizon tilted"
Token: [PATTERN_TOURIST_GROUP]
```

**PATTERN_04: THE HK NIGHT MARKET SEQUENCE** `[HK]`
```
Failures: Neon contamination + humidity haze + wet market fluorescent + high ISO + motion blur
Context: Mong Kok/LKF night market
Prompt: "Hong Kong night market sequence with neon pink blue green reflections
        on wet pavement, humidity haze reducing distant contrast,
        fluorescent green-yellow skin cast from market lighting"
Token: [PATTERN_HK_NIGHT_MARKET]
```

**PATTERN_05: THE HK TRANSIT SEQUENCE** `[HK]`
```
Failures: Escalator motion blur + passenger heads + fluorescent + train blur + glass reflection
Context: MTR/Escalator
Prompt: "Hong Kong transit sequence with escalator motion blur on steps,
        other passenger heads visible above shoulder, MTR platform
        fluorescent green cast, train motion blur through window"
Token: [PATTERN_HK_TRANSIT]
```

---

## SMARTPHONE_ERROR_LIBRARY

### Sensor Limitations
```
[ROLLING_SHUTTER] — CMOS skew in fast motion, vertical lines slanted
[HEAT_BUILDP] — Extended capture increases noise, sensor gives up
[FIXED_APERTURE] — No mechanical control, low light fixed
[NO_OPTICAL_ZOOM] — Digital zoom interpolation, soft images
```

### Processing Failures
```
[MULTI_FRAME_ERROR] — HDR/Night Mode ghosting when subject moves
[SEMANTIC_SEG_FAIL] — AI misidentifies fence as hair, cloud as subject
[OVER_SMOOTHING] — Aggressive noise reduction removes pores, plastic skin
[COLOR_BOOSTING] — Blues/greens oversaturated, cartoonish
```

### Physical Failures
```
[CRACKED_LENS] — Light scatters, haze/flare/color shifts
[FINGER_GREASE] — Soft blobs, warm cast, reduced sharpness
[WATER_INTERNAL] — Internal fogging, overall haze
[DIRTY_SENSOR_CORNERS] — Consistent dark spots at small apertures
```

### Capture Timing Errors
```
[SHUTTER_LAG] — Subject moved between press and capture
[PRE_CAPTURE_BUFFER] — May capture 0.5s before press
[POST_CAPTURE_PROCESS] — Gallery image different from captured
```

---

## MODERATION PROFILE

**Authenticity Weighting:**
```
VERY HIGH: [FAIL_FINGER_BLOCK] — requires human hold
HIGH: [FAIL_MOTION_BLUR_SUBJECT] [FAIL_MOTION_BLUR_CAMERA] [FAIL_CAMERA_DROP]
       [FAIL_NEON_HK] [FAIL_HUMIDITY_HAZE_HK] [FAIL_WET_MARKET_HK] [FAIL_DENSE_BUILDING_HK]
MEDIUM-HIGH: [FAIL_AUTOFOCUS_MISS] [FAIL_ISO_GRAIN]
MEDIUM: [FAIL_ACCIDENTAL_CROP] [FAIL_UNDEREXPOSURE] [FAIL_OVEREXPOSURE] [FAIL_PORTRAIT_MODE_FAILURE]
LOW-MEDIUM: [FAIL_RED_EYE]
LOW: [FAIL_WHITE_BALANCE] [FAIL_CHROMATIC_ABERRATION] [FAIL_LENS_FLARE]
```

**Quality Thresholds:**
- Perfect images (no failures) = suspicious
- Single failure = may be staged intentionally
- Multiple failures (3+) in different categories = genuine amateur
- Specific failure clusters = strong authenticity signals

---

## TOKEN LIBRARY

```
FAILURE TYPES:
[FAIL_ACCIDENTAL_CROP] [FAIL_OUT_OF_FRAME]
[FAIL_MOTION_BLUR_SUBJECT] [FAIL_MOTION_BLUR_CAMERA] [FAIL_CAMERA_DROP]
[FAIL_UNDEREXPOSURE] [FAIL_OVEREXPOSURE]
[FAIL_AUTOFOCUS_MISS] [FAIL_FOCUS_HUNT]
[FAIL_WHITE_BALANCE] [FAIL_ISO_GRAIN] [FAIL_CHROMATIC_ABERRATION]
[FAIL_WIDE_DISTORTION] [FAIL_LENS_FLARE] [FAIL_SENSOR_SPOT]
[FAIL_FLASH_SYNC] [FAIL_RED_EYE]
[FAIL_JPEG_COMPRESSION] [FAIL_PORTRAIT_MODE_FAILURE]
[FAIL_FINGER_BLOCK] [FAIL_DOUBLE_EXPOSURE] [FAIL_TILTED_HORIZON]
[FAIL_NEON_HK] [FAIL_HUMIDITY_HAZE_HK] [FAIL_WET_MARKET_HK] [FAIL_DENSE_BUILDING_HK]

PATTERNS:
[PATTERN_NIGHT_OUT] [PATTERN_BATHROOM_SELFIE] [PATTERN_TOURIST_GROUP]
[PATTERN_HK_NIGHT_MARKET] [PATTERN_HK_TRANSIT]

SMARTPHONE ERRORS:
[ROLLING_SHUTTER] [HEAT_BUILDP] [FIXED_APERTURE] [NO_OPTICAL_ZOOM]
[MULTI_FRAME_ERROR] [SEMANTIC_SEG_FAIL] [OVER_SMOOTHING] [COLOR_BOOSTING]
[CRACKED_LENS] [FINGER_GREASE] [WATER_INTERNAL] [DIRTY_SENSOR_CORNERS]
[SHUTTER_LAG] [PRE_CAPTURE_BUFFER] [POST_CAPTURE_PROCESS]
```

---

## PROMPT GRAMMAR

```
Base: authentic bad smartphone photo not professional
Failure: [failure_type_token] [visual_signature]
Combined: [pattern_token] for context-specific clustering
HK: Add [HK_location_token] for environment verification
Example: "authentic bad smartphone photo, motion blur from real movement,
         camera shake from handheld not tripod, ISO grain throughout,
         finger accidentally blocking lens corner"
```

---

*V15 Module: ENGINE_V15_BAD_PHOTO_REALISM_SYSTEM.md*
*Status: READY FOR INTEGRATION*
*Cross-ref: ENGINE_V15_SOCIAL_CAMERA_SYSTEM (operator + failure injection)*
