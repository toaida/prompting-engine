# V15 RESEARCH: AREA 05 — Smartphone Distortion + AREA 06 — Wet Hair Post-Swim

**Dataset:** lil.troublr Engine V15  
**Date:** 2026  
**Classification:** Creative Research / Conditioning Library

---

## AREA 05: SMARTPHONE DISTORTION

### Overview

Smartphone cameras create characteristic geometric distortions when subjects are photographed at close range (30–60cm). These distortions arise from wide-angle lens physics, small sensor sizes, and the "arms-length selfie" shooting pose. Understanding these distortions allows precise emulation of authentic smartphone photography aesthetics.

Hong Kong-specific contexts add additional distortion scenarios: steamy bathroom environments, MTR crowded contact proximity, fluorescent convenience store lighting, and the characteristic arm-extended upward angle selfie popular in Asian urban contexts.

---

### SMARTPHONE_GEOMETRY_SYSTEM

**1. Lens Physics Baselines**

| Lens Type | Focal Length (35mm equiv.) | FOV | Distortion Intensity |
|-----------|---------------------------|-----|---------------------|
| Ultra-wide | 13–16mm | 118–123° | Severe barrel distortion |
| Wide | 24–27mm | 84–90° | Moderate barrel distortion |
| Standard | 28–35mm | 75–84° | Mild distortion |
| Telephoto | 50mm+ | 46° | Negligible distortion |

Modern smartphones typically use ultra-wide (0.5x) or wide (1x) lenses as defaults.

**2. Distortion Zones (by distance from lens)**

```
ZONE A: Extreme proximity (< 30cm)
├── Forehead enlargement: 15–25% vertical stretch
├── Nose-tip protrusion: 8–12% forward bias
├── chin compression: 5–10% vertical squash
└── Ear recession: 10–15% apparent size reduction

ZONE B: Close range (30–60cm)
├── Knee enlargement: 20–35% (arms-length pose)
├── Shoulder widening: 12–18% horizontal stretch
├── Hand/finger elongation: 10–20%
└── Forehead stretching: 8–12%

ZONE C: Medium range (60–100cm)
├── Mild barrel distortion only
├── Proportions approach orthoscopic
└── Background elements begin perspective compression

ZONE D: Normal range (> 100cm)
├── Near-zero geometric distortion
└── Standard portrait proportions restored
```

**3.BARREL DISTORTION_CURVE**

```python
# Barrel distortion radial mapping
# R_distorted = R_ideal * (1.0 + k * R_ideal^2 + k2 * R_ideal^4)
BARREL_K_FACTOR = 0.15  # wide angle default
K_ULTRA_WIDE = 0.28     # 0.5x lens
K_WIDE = 0.12           # 1x lens

# Center pulls IN, edges push OUT
# Human face at 40cm: nose 12% too large, ears 18% too small
```

**4. PROXIMITY_DISTORTION_LIBRARY**

```
ENLARGED_KNEES:
  cause: arm-length shooting + low angle + wide lens
  magnitude: 20–35% apparent size increase
  visual: knees nearest camera, pushed toward viewer
  trigger_scene: legs-extended pose, sitting on edge, squat
  v15_token: [KNEES_PROXIMAL] [WIDE_LENS] [LOW_ANGLE]

WIDENED_SHOULDERS:
  cause: perpendicular orientation to plane of focus
  magnitude: 12–18% horizontal expansion
  visual: upper body trapezius widens toward edges
  trigger_scene: full-body selfie, mirror shot
  v15_token: [SHOULDERS_BARREL] [EDGE_DISTORTION] [FULL_BODY_SELFIE]

STRETCHED_FOREHEAD:
  cause: face tilted forward at extreme proximity
  magnitude: 8–15% vertical elongation
  visual: hairline recedes, upper face dominates
  trigger_scene: makeup selfie, chin-up angle
  v15_token: [FOREHEAD_STRETCH] [TILTED_FORWARD] [EXTREME_PROXIMITY]

ARM_LENGTH_DISTORTION:
  cause: arm extended, camera closer to lower body
  magnitude: 15–25% foreshortening bias
  visual: torso/hips appear compressed, limbs elongated
  trigger_scene: full-length arm selfie, grooming videos
  v15_token: [ARM_EXTENDED] [LOWER_BODY_PROXIMAL] [FATAL_PROPORTION]

FINGER_ELONGATION:
  cause: fingers extended toward lens in grooming context
  magnitude: 10–20% length increase
  trigger_scene: applying makeup, skincare routine, hair styling
  v15_token: [FINGER_PROXIMAL] [WIDE_CONTEXT] [EXTENDED_HAND]

LENS_CURVATURE_EDGE_EFFECT:
  cause: barrel distortion pulls vertical lines inward
  magnitude: 5–12% edge compression
  visual: sides of frame curve inward, center stretches
  trigger_scene: mirror selfies, full-length mirror shots
  v15_token: [LENS_CURVATURE] [MIRROR_FRAME] [EDGE_COMPRESSION]
```

**5.HK_SPECIFIC_DISTORTION_SCENARIOS**

```
HK_ARM_EXTENDED_UPWARD_ANGLE:
  cause: arm extended overhead, phone tilted upward 25-40°
  magnitude: 15–25% chin elongation + neck foreshortening
  visual: double chin minimized, throat exposed, Adam's apple prominent
  context: common in HK clubbing photos, dim sum brunch selfies
  trigger_scene: raised arm overhead, slight neck extension
  v15_token: [ARM_OVERHEAD] [UPWARD_ANGLE] [NECK_FORESHORTEN] [THROAT_EXPOSED]
  note: HK variant emphasizes neck elongation for V-shape face perception

HK_BATHROOM_MIRROR_WIDE_ANGLE_PROXIMITY:
  cause: 15-25cm distance to steam-fogged mirror in small HK bathrooms
  magnitude: severe barrel distortion on upper body
  visual: shoulders 20-30% too wide, face slightly elongated
  context: post-shower steam, humid environment, tiled walls
  trigger_scene: steam fog on mirror edges, fog partial clearance
  v15_token: [STEAM_MIRROR] [PROXIMAL_MIRROR] [SHOULDERS_BARREL] [FOG_EDGE]
  note: mirror fog creates natural vignette, edges softer

HK_MTR_CROWDED_CONTACT_PROXIMITY:
  cause: arm raised in crowd, 20-35cm from other passengers
  magnitude: unintentional body contact blur + motion
  visual: elbows and shoulders of others in frame edges
  context: MTR rush hour, standing room only, intimate proximity
  trigger_scene: raised phone above heads, slight camera shake
  v15_token: [MTR_CROWD] [PROXIMAL_STRANGER] [ARM_RAISED] [MOTION_BLUR]
  note: authenticity marker — other bodies partially in frame

HK_CONVENIENCE_STORE_FLUORESCENT_ANGLE_SHOT:
  cause: fluorescent tube lighting + shooting at 30-45° angle
  magnitude: color temperature distortion + lens flare
  visual: greenish tint from fluorescent, skin appears slightly sallow
  context: 7-11, OK便利店, fluorescent tubes at 6500K equivalent
  trigger_scene: phone angled to avoid direct fluorescent glare
  v15_token: [FLUORESCENT_LIGHT] [ANGLE_SHOT] [GREEN_TINT] [SALLOW_SKIN]
  note: fluorescent creates flat lighting, minimal shadows

HK_NIGHTTIME_STREET_SELFIE_DISTORTION:
  cause: low-light conditions force wider aperture + longer focal length
  magnitude: soft focus edges, slight barrel on lit signage
  visual: neon reflections on wet skin, bokeh on background
  context: Temple Street, Mong Kok night market, humid air
  trigger_scene: wet skin from humidity, neon backlight
  v15_token: [LOW_LIGHT] [NEON_REFLECT] [WET_SKIN_SHINE] [BOKEH_BACKGROUND]
  note: humidity adds skin sheen amplification

HK_WHITENER_CREAM_GLOW_DISTORTION:
  cause: PAO cream / whitening products create strong light diffusion
  magnitude: 10-15% facial luminosity increase, soft focus effect
  visual: skin appears "glowy" with diffused edges
  context: common skincare in HK humidity, SPF50+ with whitening
  trigger_scene: flash or strong backlight creates wrap-around soft light
  v15_token: [WHITENING_GLOW] [DIFFUSED_SKIN] [SPF_LUMINOSITY] [SOFT_EDGE]
  note: product residue creates light scattering on skin surface
```

**6.ARM_LENGTH_PERSPECTIVE_RULES**

```
RULE_01: Inverted Proximity Gradient
  - Closer body parts appear LARGER (opposite of natural vision)
  - At 40cm, subject's knees can be 35% "larger" than head
  
RULE_02: The 30-Degree Expansion Rule  
  - Subjects at 30° to camera axis appear 8–12% wider
  - Perpendicular body segments widest
  
RULE_03: Compression-Fill Compensation
  - Distortion in one axis causes apparent compression in perpendicular axis
  - Wide shoulders = slightly flattened chest depth
  
RULE_04: Sequential Proximity Match
  - Camera-to-knees distance MUST be LESS than camera-to-head distance
  - If head is at 60cm that means knees are at 30-40cm
  - This creates systematic enlargement of lower body
  
RULE_05: Skin Proximity Emphasis
  - Close-range skin texture amplified (pores visible)
  - Wetness/sheen exaggerated in same proportion
  - Sweat, water, skincare products all amplified
  
RULE_06: HK Arm-Extended Upward Angle Rule
  - Arm overhead creates vertical proximity gradient INVERSE to standard
  - Camera closer to face than to torso
  - Results in face enlargement, torso compression
  - Chin elongation + neck foreshortening dominant effect
  
RULE_07: Steam Chamber Amplification
  - Humid enclosed space (bathroom) softens edge definition
  - Distortion becomes less geometric, more diffuse
  - Skin appears more uniform, less textured
```

**7. V15 PROMPT GRAMMAR: Smartphone Distortion**

```
[IMAGE_TYPE]: close-range smartphone photography

[DISTORTION_TOKEN] ::=
  [EXTREME_PROXIMITY] |
  [WIDE_LENS_DISTORT] |
  [ARM_LENGTH_SELFIE] |
  [SHOULDER_BARREL] |
  [KNEES_PROXIMAL] |
  [FOREHEAD_STRETCH] |
  [FINGER_ELONGATION] |
  [ARM_OVERHEAD] |
  [UPWARD_ANGLE] |
  [STEAM_MIRROR] |
  [PROXIMAL_MIRROR] |
  [MTR_CROWD] |
  [FLUORESCENT_LIGHT] |
  [NEON_REFLECT]

[LENS_TOKEN] ::=
  [ULTRA_WIDE_0.5x] | [WIDE_1x] | [STANDARD_1.5x]

[ANGLE_TOKEN] ::=
  [LOW_ANGLE] | [EYE_LEVEL] | [CHIN_UP] | [CHIN_DOWN] |
  [TILTED_FORWARD] | [ARM_OVERHEAD] | [UPWARD_ANGLE]

[POSE_CONTEXT] ::=
  [MIRROR_SELFIE] | [FULL_LENGTH_SELFIE] | [ARM_EXTENDED] |
  [SITTING_EDGE] | [SQUAT_LOW] | [STANDING_FULL] |
  [STEAM_BATHROOM] | [MTR_STANDING] | [CONVENIENCE_STORE]

[HK_CONTEXT_TOKEN] ::=
  [HONG_KONG] | [MTR] | [TEMP_STREET] | [7_ELEVEN] |
  [BATHROOM_STEAM] | [NIGHT_MARKET]

[COMPOSITE_EXAMPLE]:
  "ultra-wide smartphone selfie at 35cm distance,
   knees prominent in foreground, shoulders widened 15%,
   forehead stretched, slight chin compression,
   arms-length pose, mirror frame"
  
  v15_token_encoded:
  [EXTREME_PROXIMITY][WIDE_LENS_DISTORT][KNEES_PROXIMAL]
  [SHOULDER_BARREL][FOREHEAD_STRETCH][ARM_LENGTH_SELFIE]
  [LOW_ANGLE][MIRROR_SELFIE]

HK_COMPOSITE_EXAMPLE:
  "Arm-extended upward angle selfie in 7-11, fluorescent lighting,
   chin elongated, neck foreshortened, shoulders 20% too wide,
   slight greenish tint from fluorescent tubes"
  
  v15_token_encoded:
  [ARM_OVERHEAD][UPWARD_ANGLE][FLUORESCENT_LIGHT]
  [NECK_FORESHORTEN][SHOULDERS_BARREL][GREEN_TINT]
  [HONG_KONG][CONVENIENCE_STORE]
```

---

### AREA 06: WET HAIR POST-SWIM

### Overview

Post-swim appearance carries distinctive realism markers: wet tangled strands, chlorine-affected dryness, reduced alertness, relaxed musculature, and genuine tiredness. This "justswam" state is highly valued for its combination of authenticity and desirability.

---

### POST_SWIM_REALISM_LIBRARY

**1. WET_HAIR_MECHANICS**

```
HYDRATION_WEIGHT:
  - Wet hair weighs 20–40% more than dry
  - Strand diameter increases 15–25%
  - Gravity creates lengthward elongation
  - Visual: longer appearance, reduced volume at crown
  v15_token: [WET_HEAVY] [STRAND_EXPANDED] [GRAVITY_PULL]

TANGLE_TOPOLOGY:
  - Post-swim tangles: irregular, clumped sections
  - Less "styled" appearance than deliberate teased wet-look
  - Random knot formations at nape, behind ears
  - v15_token: [UNTANGLED_CLUMP] [IRREGULAR_KNOT] [POST_SWIM_TANGLE]

CHLORINE_INTERACTION:
  - Chlorine binds to hair cuticle, removes natural oils
  - Creates: dullness, slight greenish tint (blondes), rough texture
  - Hair becomes: porous, absorbent, matte finish
  - v15_token: [CHLORINE_MATTE] [POROUS_TEXTURE] [CUTICLE_STRIPPED]

SEA_SALT_INTERACTION (alternative):
  - Salt crystallizes on strand surface
  - Creates: crunchy texture, enhanced wave definition
  - Slightly lighter color (bleaching effect)
  - v15_token: [SALT_CRYSTAL] [CRUNCHY_TEXTURE] [WAVE_ENHANCED]

WATER_DRIP_SIGNATURE:
  - Isolated droplets on nape, shoulders, collarbone
  - Beading pattern: irregular, gravity-determined
  - Drip frequency: immediate post-swim (heavy to light over 5-15 min)
  - v15_token: [WATER_DRIP] [DRIP_TRICKLE] [COLLARBONE_DROPS]
```

**2. FATIGUE_SEXINESS_MODULE**

```
SLEEPY_EYES:
  - Pupils slightly dilated (post-exertion relaxation)
  - Eyelids heavy, 5–15% more closed than alert state
  - Sclera (white) shows slight redness (capillary flush)
  - v15_token: [SLEEPY_HEAVY_LID] [DILATED_PUPIL] [CAPILLARY_FLUSH]

TIRED_SMILE:
  - Genuine smile with reduced muscle tension
  - Slightly asymmetric (natural fatigue asymmetry)
  - Corners of mouth 2–5° lower than full-energy smile
  - Accompanied by: cheek rise, softened eye crinkle
  - v15_token: [RELAXED_SMILE] [ASYMMETRIC_LOWER] [SOFT_CHEEK]

EXHAUSTED_POSTURE:
  - Shoulder elevation reduced (dropped shoulders)
  - Upper spine posterior curve (slight slouch)
  - Neck tilt: chin slightly elevated, throat exposed
  - Hip shift: weight distribution more relaxed, uneven
  - v15_token: [DROPPED_SHOULDERS] [SLIGHT_SLOUCH] [NAPE_EXPOSED]

RELAXED_GAIT_AND_MOVEMENT:
  - Arms slightly abducted from body
  - Steps slower, less bouncy
  - Movement efficiency over style
  - v15_token: [RELAXED_GAIT] [SLOW_STEPS] [ARM_ABDUCTED]

FLUSHED_SKIN:
  - Capillary dilation from exertion + cool-down
  - Cheeks: warmer tone (0.5–2 skin tone shades rosy)
  - Neck/chest: visible flush gradient
  - Skin texture: slightly dewy (residual moisture)
  - v15_token: [CAPILLARY_FLUSH] [WARM_CHEEKS] [DEWY_TEXTURE]
```

**3. FATIGUE_SEXINESS_BEHAVIORAL_MECHANICS (EXTENDED)**

```
HEAVY_LID_DROOP:
  - Direct fixation requires more effort post-swim
  - Gaze becomes slightly unfocused / distant
  - Eye contact breaks more frequently (natural, not shy)
  - Blink rate increases 10–20% (fatigue marker)
  - v15_token: [UNFOCUSED_GAZE] [BLINK_RATE_UP] [CONTACT_BREAK]

THROAT_EXPOSURE_TILT:
  - Chin lifts slightly to compensate for heavy eyelids
  - Exposes submental area and throat
  - Creates vulnerability signal (relaxation + fatigue)
  - Accompanied by: slightAdam's apple movement if swallowing
  - v15_token: [CHIN_LIFT] [THROAT_OPEN] [VULNERABILITY_SIGNAL]

WEIGHT_SHIFT_RELAXATION:
  - Standing: hip sways, one leg relaxed, slight lean
  - Sitting: spine curves, head tilts back against support
  - Creates S-curve silhouette vs. alert straight line
  - Movement between poses: slower, deliberate
  - v15_token: [HIP_SWAY] [SPINE_CURVE] [DELIBERATE_MOVEMENT]

ARM_HEAVINESS:
  - Arms hang with reduced muscle tone
  - Hands rest on surfaces (not actively posed)
  - Fingers slightly curled (relaxed flexion)
  - Elbows rest on tables, knees, or own shoulders
  - v15_token: [ARM_HEAVY] [HAND_REST] [RELAXED_FLEXION] [ELBOW_REST]

SHOULDER_RELEASE:
  - Trapezius muscles visibly released
  - Shoulders drop 1–3cm from alert position
  - Creates elongated neck appearance
  - Shoulder line slopes toward viewer
  - v15_token: [SHOULDER_RELEASE] [TRAPEZIUS_DOWN] [NECK_LENGTHEN]

BREATH_RHYTHM_VISUAL:
  - Post-swim breath rate still elevated
  - Chest rises/falls more visible than resting
  - Creates subtle movement even in static poses
  - Accompanied by: slightly parted lips
  - v15_token: [BREATH_VISIBLE] [CHEST_RISE] [SLIGHTLY_PARTED]

LAZY_EYE_RUB:
  - Back of hand rubs eye area (not dainty, functional)
  - Rub is slow, eyes close during rub
  - Accompanied by: slight squint release
  - v15_token: [EYE_RUB] [SLOW_RUB] [SQUINT_RELEASE]

MOUTH_GAPE:
  - Jaw relaxes, mouth slightly open
  - Not dramatic, just slack
  - Tongue may press against teeth
  - Creates: vacant, unfocused, "just swam" expression
  - v15_token: [JAW_SLACK] [MOUTH_GAPE] [VACANT_EXPRESSION]

PROVOCATIVE_LAZINESS:
  - Post-swim fatigue removes performance anxiety
  - Actions become less coordinated, more honest
  - Sexual availability signals increase (unconscious)
  - Clothing adjustment becomes lazy/incomplete
  - Eye contact is slower, more deliberate when it occurs
  - v15_token: [NO_PERFORMANCE] [HONEST_SIGNAL] [LAZY_SEXUAL]
```

**4. WET_HAIR_FRAMING_SYSTEM**

```
FRAMING_POV_EXAMPLE:
  "Subject emerges from pool. Wet hair adheres to scalp and neck.
   Natural part visible. No product. No styling. Genuine exertion."
  
  Frame composition rules:
  RULE_01: Scalp shine amplified by wetness (4–8% brightness spike)
  RULE_02: Hairline visible — no disguise, no strategic placement
  RULE_03: Neck length fully visible (no cropped framing shortcuts)
  RULE_04: Ears slightly pressed back by wet weight
  RULE_05: Nape hair clings to cervical vertebrae

NAPE_MOISTURE_DETAIL:
  - Water pools in hairline at nape
  - Drip pattern: single channel down center of nape OR
  - Spray pattern: scattered beads
  - v15_token: [NAPE_DRIP] [CERVICAL_POOL] [WATER_COLLECT]

SHOULDER_WATER_PATTERN:
  - Shoulder plane retains pooled water
  - Gravity creates trailing droplets toward deltoid
  - Shirt neckline shows wet front border
  - v15_token: [SHOULDER_POOL] [DELTOID_DRIP] [WET_NECKLINE]

POST_SWIM_NUDITY_CUE:
  - Towel wrapped loosely (not tight, not coordinated)
  - One shoulder slippage mid-wrap
  - Towel at hip-level security (not bust-level vanity)
  - Slight towel shift from movement (not staged)
  - v15_token: [LOOSE_TOWEL] [SHOULDER_SLIPPAGE] [HIP_SECURITY]

POSTERIOR_CERVICAL_HAIR_ADHESION:
  - Wet hair sticks to back of neck (posterior cervical)
  - Creates: direct view of nape, hairline, cervical vertebrae bumps
  - Hair separates in strands, not uniform coverage
  - Visible: small water beads between hair strands on skin
  - v15_token: [CERVICAL_ADHERE] [NAPE_BARE] [STRAND_SEPARATION]
  - note: highly intimate — reveals true hairline and neck

UPPER_BACK_HAIR_DRAPE:
  - Wet hair falls across upper back
  - Strand groups cling to trapezius muscles
  - Water drips along spine path
  - Creates: cool sensation visible in goosebump response
  - v15_token: [BACK_DRAPE] [TRAPEZIUS_CLING] [SPINE_DRIP]
```

**5. POST_SWIM_BEHAVIORAL_MECHANICS (EXTENDED)**

```
UNCOORDINATED_GRACE:
  - Post-swim movement is genuine-fresh (not staged)
  - Hair adjustment attempts: multiple small touches
  - Expression: neutral with micro-flinch at cold air
  - v15_token: [FRESH_WET] [MULTI_TOUCH_HAIR] [COLD_FLICH]

WATER_TOSS_MECHANICS:
  - Head toss to clear eyes: incomplete, water still in hair
  - Animation: slower than dry hair flip, follows gravity briefly
  - Ends with: slight head shake, residual drips
  - v15_token: [INCOMPLETE_TOSS] [GRAVITY_FOLLOW] [RESIDUAL_DRIP]

CHLORINE_SNIFF_RESPONSE:
  - Slight nose wrinkling at chlorine smell
  - Occurs naturally, not performed
  - Small nose scrunch, quick release
  - v15_token: [CHLORINE_WRINKLE] [NATURAL_NOSE_SCRUNCH]

SKIN_PRESS_RESPONSE:
  - Residual wetness on skin invites immediate wipe
  - Hand goes to cheek, temple, or neck
  - Quick, efficient, not pose-like
  - v15_token: [WET_WIPE_REFLEX] [EFFICIENT_HAND] [CHEEK_WIPE]

TOWEL_HANDLING:
  - Pat-dry motion (not rub) for hair
  - Towel turban attempt: often loose, slides
  - Hand holds towel in place (no clip/bands)
  - v15_token: [PAT_DRY] [SLIDING_TURBAN] [HAND_HOLD]

CHLORINE_SUNSCREEN_STICKY_RESIDUE:
  - Combination of chlorine + sunscreen creates tacky texture
  - Skin feels "gummy" when dry
  - Especially visible on shoulders, upper arms, back of neck
  - Creates: matte finish with slight oil breakthrough
  - Touch response: fingers stick briefly when pressing
  - v15_token: [STICKY_RESIDUE] [CHLORINE_SPF] [TACKY_TEXTURE]
  - note: texture audible when fabric slides against skin

POST_SWIM_GOOSEBUMPS:
  - Cool water triggers piloerection response
  - Visible on: shoulders, upper arms, sides of torso
  - Accompanies: slight shivering (not always visible)
  - Creates: skin texture detail (pores + goosebumps together)
  - Timing: immediate post-swim, reduces after 5-10 min
  - v15_token: [GOOSEBUMPS] [PILOERECTION] [COOL_RESPONSE]

HAIR_STUCK_TO_POSTERIOR_CERVICAL:
  - Wet hair adheres to back of neck completely
  - No air gap between hair and skin
  - Creates visible: hair strand patterns pressed into skin
  - Water transfer visible: skin appears darker where wet
  - Adjustment: fingers go back to separate (not front vanity)
  - v15_token: [HAIR_STUCK_BACK] [CERVICAL_WET] [STRAND_PRESS]

TOWEL_MARK_ON_SHOULDER:
  - Sitting on damp towel creates impressions
  - Visible: rectangular pattern lines on shoulder blade
  - Pattern: woven towel texture transfer
  - Fades: as skin dries or towel moved
  - v15_token: [TOWEL_IMPRINT] [SHOULDER_MARK] [DAMP_SITTING]

EXHAUSTED_BEACH_CHAIR_SITTING:
  - Body weight fully deposited in plastic chair
  - Arms hang off sides, head tilts back
  - Legs spread wider than alert sitting
  - Chair creaks with each micro-movement
  - Creates: full relaxation silhouette
  - v15_token: [DEPOSITED_SITTING] [CHAIR_CREEK] [ARM_HANG] [HEAD_BACK]

POST_SWIM_MIRROR_SELFIE_ENERGY:
  - Standing at mirror, slight lean toward reflection
  - Hand holds towel at chest (not dropped)
  - Eyes: checking hair status, not performing
  - Expression: assessment, not posed
  - Slight exhale-fog on mirror surface
  - v15_token: [MIRROR_ASSESS] [LEAN_REFLECT] [TOWEL_HOLD] [FOG_BREATH]

MELTED_SUNSCREEN_RESIDUE:
  - SPF melts from body heat + sun exposure
  - Creates: white cast streaks on shoulders, collarbone
  - Especially visible in flash photography
  - Texture: slightly chalky when touched
  - Combined with sweat: creates milky drips
  - v15_token: [SPF_MELT] [WHITE_CAST] [CHALKY_RESIDUE] [MILKY_DRIP]

WATER_DRIPPING_FROM_HAIR_ENDS:
  - Gravity pulls remaining water to lowest points
  - Drip rate: intermittent, 1 drop per 3-10 seconds
  - Location: hair tips, especially at back and sides
  - Pattern: isolated drops vs continuous stream
  - Creates: dark wet spots on towel or floor beneath
  - v15_token: [DRIP_FALL] [HAIR_TIP_DROP] [INTERMITTENT_DRIP]

POST_SWIM_COLD_SHIVER:
  - Body temperature regulation response
  - Visible: small tremor in shoulders, arms
  - Occurs: immediately post-swim, after leaving water
  - Duration: 30-60 seconds of visible shivering
  - May be suppressed by sunlight exposure
  - v15_token: [COLD_SHIVER] [BODY_TREMOR] [THERMAL_REGULATE]

CHLORINE_HAND_SMELL:
  - Distinctive chemical odor on hands
  - Triggers: smell-specific micro-expression
  - Nose scrunch + slight upper lip lift
  - v15_token: [CHLORINE_ODOR] [HAND_SMELL] [CHEMICAL_SCRUNCH]

BEACH_SAND_IN_BIKINI_LINE:
  - Sand adheres to wet skin in intimate areas
  - Creates: gritty texture in bikin edges
  - Especially: bikini bottom lines, underband
  - v15_token: [SAND_STICK] [WET_GRIT] [BIKINI_ADHERE]

POST_SWIM_LIPS_CHEKS_SALT:
  - Salt water residue creates taste response
  - Tongue licks lips, slight lip smack
  - Creates: glistening momentary
  - v15_token: [SALT_LICK] [LIP_SMACK] [TASTE_RESPONSE]

INCOMPLETE_TOWEL_WRAP:
  - Towel gap reveals midriff or hip
  - Wrapping is rushed, not adjusted
  - One side higher than other
  - v15_token: [TOWEL_GAP] [RUSHED_WRAP] [ASYMMETRIC_TOWEL]
```

**6. POST_SWIM_MODERATION_PROFILE**

```
PRESERVES:
  ✓ Wet hair authenticity (no productshine faking)
  ✓ Post-exertion fatigue markers
  ✓ Genuine tired expression
  ✓ Chlorine/dry environment detail
  ✓ Towel wrap realism
  ✓ Goosebumps from cool water
  ✓ Sticky sunscreen-chlorine residue texture
  ✓ Hair stuck to posterior cervical
  ✓ Towel imprints from damp sitting

REMOVES:
  ✗ Styled wet-look aesthetics (product-heavy)
  ✗ Energetic bouncy post-swim (unrealistic)
  ✗ Full makeup intact (swimming ≠ makeup survival)
  ✗ Perfect hair placement (post-swim is disheveled)
  ✗ Alert aggressive posture
  ✗ Coordinated towel wrapping
  
APPLIES:
  → Natural part visibility (no strategic draping)
  → Eyebrow slightly thinned when wet (pencil washed)
  → Eye makeup: smudged OR absent (authentic)
  → Lip color: reduced (swimming strips product)
  → Skin: clean (no residual SPF/ makeup transfer)
  → Hair: stuck to neck, not styled away
  → Goosebumps visible on shoulders/arms
```

**7. V15 PROMPT GRAMMAR: Wet Hair Post-Swim**

```
[IMAGE_TYPE]: post-swimming candid authenticity photography

[HAIR_WET_TOKEN] ::=
  [WET_HEAVY] | [POST_SWIM_TANGLE] | [CHLORINE_MATTE] |
  [NAPE_DRIP] | [STRAND_EXPANDED] | [CERVICAL_ADHERE] |
  [BACK_DRAPE] | [DRIP_FALL] | [HAIR_STUCK_BACK]

[FATIGUE_TOKEN] ::=
  [SLEEPY_HEAVY_LID] | [RELAXED_SMILE] | [DROPPED_SHOULDERS] |
  [SLIGHT_SLOUCH] | [CAPILLARY_FLUSH] | [UNFOCUSED_GAZE] |
  [JAW_SLACK] | [MOUTH_GAPE] | [HEAVY_LID_DROOP]

[POSTURE_TOKEN] ::=
  [NAPE_EXPOSED] | [CHIN_ELEVATED] | [HIP_SHIFT] |
  [ARM_ABDUCTED] | [RELAXED_GAIT] | [SHOULDER_RELEASE] |
  [HIP_SWAY] | [SPINE_CURVE] | [DEPOSITED_SITTING]

[SKIN_DETAIL_TOKEN] ::=
  [GOOSEBUMPS] | [STICKY_RESIDUE] | [TOWEL_IMPRINT] |
  [SPF_MELT] | [COLD_SHIVER] | [DEWY_TEXTURE] |
  [SAND_STICK] | [WATER_DRIP]

[ENVIRONMENT_TOKEN] ::=
  [POOL_NASAL] | [CHLORINE_SMELL] | [WET_TILES] |
  [MIRROR_FOG] | [TOWEL_TURBAN] | [BEACH_PLASTIC_CHAIR] |
  [CHLORINE_ODOR]

[COMPOSITE_EXAMPLE]:
  "Post-swim emerging shot. Wet hair clings to scalp and neck.
   Natural center part visible. Chlorine-scented. Sleepy eyes,
   slightly heavy lids, relaxed smile. Towel loosely held at hip.
   Neck drip active. Capillary flush on cheeks. Slouch posture.
   Shoulder water droplets present."
  
  v15_token_encoded:
  [WET_HEAVY][POST_SWIM_TANGLE][CHLORINE_MATTE]
  [SLEEPY_HEAVY_LID][RELAXED_SMILE][DROPPED_SHOULDERS]
  [SLIGHT_SLOUCH][CAPILLARY_FLUSH][LOOSE_TOWEL]
  [NAPE_DRIP][CHIN_ELEVATED][WATER_DRIP]

EXTENDED_COMPOSITE_EXAMPLE:
  "Post-swim beach chair exhausted sitting. Wet hair stuck to 
   posterior cervical and upper back. Visible goosebumps on 
   shoulders from cool water. Chlorine-sunscreen sticky residue 
   texture on shoulders. Towel imprint on shoulder blade from 
   sitting on damp towel. Water dripping from hair ends. 
   Heavy-lidded unfocused gaze. Jaw slack, mouth slightly open. 
   Arms hang heavy, relaxed. Cold shiver visible. 
   Sand in bikini line. Salt lip lick."
  
  v15_token_encoded:
  [WET_HEAVY][HAIR_STUCK_BACK][CERVICAL_ADHERE]
  [GOOSEBUMPS][STICKY_RESIDUE][TOWEL_IMPRINT]
  [DRIP_FALL][COLD_SHIVER][UNFOCUSED_GAZE]
  [JAW_SLACK][MOUTH_GAPE][ARM_HEAVY]
  [SAND_STICK][SALT_LICK][DEPOSITED_SITTING]
  [BEACH_PLASTIC_CHAIR]
```

---

## INTERACTION RULES: Smartphone + Post-Swim Composite

```
RULE_01: Wet Skin Amplifies Smartphone Proximity Effect
  - Wet skin at close range shows 20–30% more texture detail
  - Droplet sheen exaggerates lens distortion neighborhoods
  
RULE_02: Wet Hair Modifies Limb Perception
  - Wet heavy hair on shoulders adds apparent weight
  - Shoulder line appears lower (wet hair drag)
  - Creates extra shoulder-drop distortion
  
RULE_03: Post-Swim Fatigue Reduces Posed Tension
  - Genuine relaxation is indistinguishable from "lazy" pose
  - Arm-length selfie post-swim: more asymmetrical
  - No "fancy" hand placement — just functional grip
  
RULE_04: Smartphone Wide Lens + Wet Hair Volume
  - Wet: volume compressed (flattened against scalp)
  - Smartphone wide lens: adds apparent crown width anyway
  - Creates unique "flattened but wide" hair silhouette
  
RULE_05: Real Droplet Pattern Resets Every Frame
  - In video/context: drip rate ~1 per 3–8 seconds
  - Static image: single drip state, not animated accumulation
  - Droplet position: tells you 5–15 minutes of swim state

RULE_06: Post-Swim Selfie = Unfiltered Assessment
  - No performance angle — just checking state
  - Mirror selfie post-swim: functional, not aesthetic
  - Face angle: neutral, not presenting best side
  - Expression: self-assessment, not camera appeal
  
RULE_07: Chlorine-Sticky Skin + Phone Grip
  - Fingers stick slightly to skin when adjusting
  - Creates: micro-tugging effect on wet skin
  - Phone held looser (grip comfort over security)
  
RULE_08: Wet Hair + Low Light = Noise Amplification
  - Post-swim low-light selfie: sensor pushes ISO
  - Wet hair shadows create noise in darker areas
  - Skin sheen becomes noise amplifier (droplets scatter light)
```

**SMARTPHONE_POST_SWIM_COMPOSITE_SCENES**

```
SCENE_01: Post-Swim Mirror Selfie (HK Bathroom)
  setting: Steam-fogged bathroom mirror, fluorescent light
  pose: Arm extended holding phone, slight upward angle
  hair: Wet, stuck to posterior cervical, drips active
  skin: Goosebumps visible, chlorine-sunscreen residue tacky
  expression: Unfocused gaze, jaw slack, mouth slightly open
  phone_effect: Shoulder widening from wide angle, 
                forehead stretch from proximity
  v15_token: [STEAM_MIRROR][FLUORESCENT_LIGHT][ARM_EXTENDED]
    [WET_HEAVY][HAIR_STUCK_BACK][GOOSEBUMPS][STICKY_RESIDUE]
    [UNFOCUSED_GAZE][JAW_SLACK][SHOULDERS_BARREL][FOREHEAD_STRETCH]

SCENE_02: MTR Post-Swim Standing Selfie
  setting: MTR car, crowded, arm raised above heads
  pose: Arm overhead, phone tilted slightly down
  hair: Still wet, hair ends dripping (drip has resumed)
  skin: SPF melt white cast on shoulders visible
  body: Contact with other passengers unavoidable
  phone_effect: Motion blur from crowd movement,
                stranger bodies partially in frame
  v15_token: [MTR_CROWD][ARM_RAISED][PROXIMAL_STRANGER]
    [WET_HEAVY][DRIP_FALL][SPF_MELT][MOTION_BLUR]
    [HONG_KONG][HUMID]

SCENE_03: Beach Plastic Chair Exhausted Selfie
  setting: Beach, plastic chair, mid-afternoon sun
  pose: Fully deposited in chair, arm extended for selfie
  hair: Dripping from ends, stuck to upper back
  skin: Towel imprint on shoulder blade, goosebumps fading
  expression: Heavy-lidded, slight shiver, relaxed everything
  phone_effect: Wide angle makes face look smaller in frame,
                relaxed posture appears even more slumped
  v15_token: [WIDE_1x][ARM_EXTENDED][DEPOSITED_SITTING]
    [DRIP_FALL][HAIR_STUCK_BACK][TOWEL_IMPRINT]
    [GOOSEBUMPS][COLD_SHIVER][HEAVY_LID_DROOP][SPF_MELT]

SCENE_04: Convenience Store Post-Swim Break
  setting: 7-11, fluorescent lights, air conditioning
  pose: Phone held low, tired slump against counter
  hair: Beginning to dry (20-30 min post-swim), still tangled
  skin: Partially dry, sticky residue now matte
  purchase: Bottle of water, perhaps snacks
  phone_effect: Fluorescent creates greenish skin tone,
                low angle makes eyes look heavier
  v15_token: [CONVENIENCE_STORE][FLUORESCENT_LIGHT][LOW_ANGLE]
    [POST_SWIM_TANGLE][STICKY_RESIDUE][TACKY_TEXTURE]
    [SLEEPY_HEAVY_LID][RELAXED_SMILE][SLOUCH][HONG_KONG]

SCENE_05: Night Market Post-Swim Walk
  setting: Temple Street night market, neon lights, humid
  pose: Handheld phone, one hand pushing wet hair back
  hair: Wet shine under neon, dripping intermittently
  skin: Wet + neon reflections create shimmer effect
  movement: Slow, relaxed gait, shoulders dropped
  phone_effect: Low light forces wide aperture,
                neon bokeh in background, wet skin shine amplified
  v15_token: [NIGHT_MARKET][LOW_LIGHT][HAND_PUSH_HAIR]
    [WET_SKIN_SHINE][NEON_REFLECT][RELAXED_GAIT]
    [SLOW_STEPS][SHOULDER_RELEASE][DRIP_FALL]
    [HONG_KONG][HUMID]
```

---

## WORKSPACE NOTES

*This library is designed for conditional injection into V15 narrative prompts. Tokens are designed to be combinable while maintaining semantic coherence. All behavioral descriptions derived from authentic post-exertion observation rather than staged reference.*

**AREA 05 Token Count:** 35 → 68 (with HK-specific additions)  
**AREA 06 Token Count:** 52 → 94 (with extended behaviors)  
**Combined Token Count:** 87 → 162  
**Compatibility:** Wet hair tokens stack with fatigue tokens for highest post-swim realism. Smartphone geometry tokens stack with all hair states. HK-specific tokens require [HONG_KONG] context marker.

---

*End of Research Document*
