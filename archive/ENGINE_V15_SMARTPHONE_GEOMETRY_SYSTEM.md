# ENGINE_V15_SMARTPHONE_GEOMETRY_SYSTEM.md

## V15 Core Module — Smartphone Distortion + Geometry
### AREA: 05 (Smartphone Distortion) | Status: READY FOR INTEGRATION

---

## PURPOSE

Smartphone cameras create characteristic geometric distortions at close range (30-60cm). These arise from wide-angle lens physics, small sensors, and the "arms-length selfie" pose. Understanding these distortions allows precise emulation of authentic smartphone photography aesthetics.

---

## KEY CONCEPTS

**Distortion Zones**: A (Extreme <30cm), B (Close 30-60cm), C (Medium 60-100cm), D (Normal >100cm)

**Proximity Gradient**: Inverted from natural vision — closer parts appear LARGER

**HK-Specific Scenarios**: Steam bathrooms, MTR crowded contact, convenience store fluorescent, arm-extended upward angle

---

## SMARTPHONE_GEOMETRY_SYSTEM

### Lens Physics Baselines

```
| Lens Type    | Focal Length | FOV      | Distortion |
|--------------|--------------|----------|------------|
| Ultra-wide   | 13-16mm      | 118-123° | Severe     |
| Wide         | 24-27mm      | 84-90°   | Moderate   |
| Standard     | 28-35mm      | 75-84°   | Mild       |
| Telephoto    | 50mm+        | 46°      | Negligible |

Modern smartphones: Ultra-wide (0.5x) or Wide (1x) as defaults
```

### Distortion Zones

**ZONE A: EXTREME PROXIMITY** (< 30cm)
```
Forehead enlargement: 15-25% vertical stretch
Nose-tip protrusion: 8-12% forward bias
Chin compression: 5-10% vertical squash
Ear recession: 10-15% apparent size reduction
Token: [ZONE_A_EXTREME]
```

**ZONE B: CLOSE RANGE** (30-60cm)
```
Knee enlargement: 20-35% (arms-length pose)
Shoulder widening: 12-18% horizontal stretch
Hand/finger elongation: 10-20%
Forehead stretching: 8-12%
Token: [ZONE_B_CLOSE]
```

**ZONE C: MEDIUM RANGE** (60-100cm)
```
Mild barrel distortion only
Proportions approach orthoscopic
Background elements begin perspective compression
Token: [ZONE_C_MEDIUM]
```

**ZONE D: NORMAL RANGE** (> 100cm)
```
Near-zero geometric distortion
Standard portrait proportions restored
Token: [ZONE_D_NORMAL]
```

### Barrel Distortion Curve

```
BARREL_K_FACTOR = 0.15 (wide angle default)
K_ULTRA_WIDE = 0.28 (0.5x lens)
K_WIDE = 0.12 (1x lens)

Center pulls IN, edges push OUT
Human face at 40cm: nose 12% too large, ears 18% too small
```

---

## PROXIMITY_DISTORTION_LIBRARY

**ENLARGED_KNEES**
```
Cause: Arm-length shooting + low angle + wide lens
Magnitude: 20-35% apparent size increase
Visual: Knees nearest camera pushed toward viewer
Trigger: legs-extended pose, sitting on edge, squat
Token: [KNEES_PROXIMAL] [WIDE_LENS] [LOW_ANGLE]
```

**WIDENED_SHOULDERS**
```
Cause: Perpendicular orientation to plane of focus
Magnitude: 12-18% horizontal expansion
Visual: Upper body trapezius widens toward edges
Trigger: Full-body selfie, mirror shot
Token: [SHOULDERS_BARREL] [EDGE_DISTORTION] [FULL_BODY_SELFIE]
```

**STRETCHED_FOREHEAD**
```
Cause: Face tilted forward at extreme proximity
Magnitude: 8-15% vertical elongation
Visual: Hairline recedes, upper face dominates
Trigger: Makeup selfie, chin-up angle
Token: [FOREHEAD_STRETCH] [TILTED_FORWARD] [EXTREME_PROXIMITY]
```

**ARM_LENGTH_DISTORTION**
```
Cause: Arm extended, camera closer to lower body
Magnitude: 15-25% foreshortening bias
Visual: Torso/hips compressed, limbs elongated
Trigger: Full-length arm selfie, grooming videos
Token: [ARM_EXTENDED] [LOWER_BODY_PROXIMAL] [FATAL_PROPORTION]
```

**FINGER_ELONGATION**
```
Cause: Fingers extended toward lens in grooming context
Magnitude: 10-20% length increase
Trigger: Applying makeup, skincare, hair styling
Token: [FINGER_PROXIMAL] [WIDE_CONTEXT] [EXTENDED_HAND]
```

**LENS_CURVATURE_EDGE_EFFECT**
```
Cause: Barrel distortion pulls vertical lines inward
Magnitude: 5-12% edge compression
Visual: Sides of frame curve inward, center stretches
Trigger: Mirror selfies, full-length mirror shots
Token: [LENS_CURVATURE] [MIRROR_FRAME] [EDGE_COMPRESSION]
```

---

## HK_SPECIFIC_DISTORTION_SCENARIOS

**HK_ARM_EXTENDED_UPWARD_ANGLE** `[HK]`
```
Cause: Arm extended overhead, phone tilted upward 25-40°
Magnitude: 15-25% chin elongation + neck foreshortening
Visual: Double chin minimized, throat exposed, Adam's apple prominent
Context: HK clubbing photos, dim sum brunch selfies
Token: [ARM_OVERHEAD] [UPWARD_ANGLE] [NECK_FORESHORTEN] [THROAT_EXPOSED]
Note: HK variant emphasizes neck elongation for V-face perception
```

**HK_BATHROOM_MIRROR_WIDE_ANGLE_PROXIMITY** `[HK]`
```
Cause: 15-25cm distance to steam-fogged mirror in small HK bathrooms
Magnitude: Severe barrel distortion on upper body
Visual: Shoulders 20-30% too wide, face slightly elongated
Context: Post-shower steam, humid environment, tiled walls
Token: [STEAM_MIRROR] [PROXIMAL_MIRROR] [SHOULDERS_BARREL] [FOG_EDGE]
Note: Mirror fog creates natural vignette, edges softer
```

**HK_MTR_CROWDED_CONTACT_PROXIMITY** `[HK]`
```
Cause: Arm raised in crowd, 20-35cm from other passengers
Magnitude: Unintentional body contact blur + motion
Visual: Elbows and shoulders of others in frame edges
Context: MTR rush hour, standing room only, intimate proximity
Token: [MTR_CROWD] [PROXIMAL_STRANGER] [ARM_RAISED] [MOTION_BLUR]
Note: Authenticity marker — other bodies partially in frame
```

**HK_CONVENIENCE_STORE_FLUORESCENT_ANGLE_SHOT** `[HK]`
```
Cause: Fluorescent tube lighting + shooting at 30-45° angle
Magnitude: Color temperature distortion + lens flare
Visual: Greenish tint from fluorescent, skin appears slightly sallow
Context: 7-11, OK便利店, fluorescent tubes at 6500K equivalent
Token: [FLUORESCENT_LIGHT] [ANGLE_SHOT] [GREEN_TINT] [SALLOW_SKIN]
Note: Fluorescent creates flat lighting, minimal shadows
```

**HK_NIGHTTIME_STREET_SELFIE_DISTORTION** `[HK]`
```
Cause: Low-light forces wider aperture + longer focal length
Magnitude: Soft focus edges, slight barrel on lit signage
Visual: Neon reflections on wet skin, bokeh on background
Context: Temple Street, Mong Kok night market, humid air
Token: [LOW_LIGHT] [NEON_REFLECT] [WET_SKIN_SHINE] [BOKEH_BACKGROUND]
Note: Humidity adds skin sheen amplification
```

**HK_WHITENER_CREAM_GLOW_DISTORTION** `[HK]`
```
Cause: PAO cream / whitening products create strong light diffusion
Magnitude: 10-15% facial luminosity increase, soft focus effect
Visual: Skin appears "glowy" with diffused edges
Context: Common skincare in HK humidity, SPF50+ with whitening
Token: [WHITENING_GLOW] [DIFFUSED_SKIN] [SPF_LUMINOSITY] [SOFT_EDGE]
Note: Product residue creates light scattering on skin surface
```

---

## ARM_LENGTH_PERSPECTIVE_RULES

**RULE_01: INVERTED PROXIMITY GRADIENT**
```
Closer body parts appear LARGER (opposite of natural vision)
At 40cm: subject's knees can be 35% "larger" than head
```

**RULE_02: 30-DEGREE EXPANSION RULE**
```
Subjects at 30° to camera axis appear 8-12% wider
Perpendicular body segments widest
```

**RULE_03: COMPRESSION-FILL COMPENSATION**
```
Distortion in one axis causes apparent compression in perpendicular axis
Wide shoulders = slightly flattened chest depth
```

**RULE_04: SEQUENTIAL PROXIMITY MATCH**
```
Camera-to-knees distance MUST BE LESS than camera-to-head distance
If head is at 60cm → knees at 30-40cm → systematic lower body enlargement
```

**RULE_05: SKIN PROXIMITY EMPHASIS**
```
Close-range skin texture amplified (pores visible)
Wetness/sheen exaggerated in same proportion
Sweat, water, skincare products all amplified
```

**RULE_06: HK ARM-OVERHEAD RULE**
```
Arm overhead creates vertical proximity gradient INVERSE to standard
Camera closer to face than torso → face enlargement, torso compression
Chin elongation + neck foreshortening dominant effect
```

**RULE_07: STEAM CHAMBER AMPLIFICATION**
```
Humid enclosed space (bathroom) softens edge definition
Distortion becomes less geometric, more diffuse
Skin appears more uniform, less textured
```

---

## PROMPT GRAMMAR

```
Base: close-range smartphone photography at [distance]cm

Distortion Token:
[EXTREME_PROXIMITY] | [WIDE_LENS_DISTORT] | [ARM_LENGTH_SELFIE]
[SHOULDER_BARREL] | [KNEES_PROXIMAL] | [FOREHEAD_STRETCH]
[FINGER_ELONGATION] | [ARM_OVERHEAD] | [UPWARD_ANGLE]
[STEAM_MIRROR] | [PROXIMAL_MIRROR] | [MTR_CROWD]
[FLUORESCENT_LIGHT] | [NEON_REFLECT]

Lens Token:
[ULTRA_WIDE_0.5x] | [WIDE_1x] | [STANDARD_1.5x]

Angle Token:
[LOW_ANGLE] | [EYE_LEVEL] | [CHIN_UP] | [CHIN_DOWN]
[TILTED_FORWARD] | [ARM_OVERHEAD] | [UPWARD_ANGLE]

HK Context:
[HONG_KONG] | [MTR] | [TEMP_STREET] | [7_ELEVEN]
[BATHROOM_STEAM] | [NIGHT_MARKET]

Composite Example:
"ultra-wide smartphone selfie at 35cm, knees prominent foreground,
 shoulders widened 15%, forehead stretched, slight chin compression,
 arm-length pose, mirror frame"
Token: [EXTREME_PROXIMITY][WIDE_LENS_DISTORT][KNEES_PROXIMAL]
        [SHOULDER_BARREL][FOREHEAD_STRETCH][ARM_LENGTH_SELFIE]
        [LOW_ANGLE][MIRROR_SELFIE]

HK Composite:
"arm-extended upward angle selfie in 7-11, fluorescent lighting,
 chin elongated, neck foreshortened, shoulders 20% too wide,
 slight greenish tint from fluorescent"
Token: [ARM_OVERHEAD][UPWARD_ANGLE][FLUORESCENT_LIGHT]
        [NECK_FORESHORTEN][SHOULDERS_BARREL][GREEN_TINT]
        [HONG_KONG][CONVENIENCE_STORE]
```

---

## TOKEN LIBRARY

```
DISTORTION ZONES:
[ZONE_A_EXTREME] [ZONE_B_CLOSE] [ZONE_C_MEDIUM] [ZONE_D_NORMAL]

PROXIMITY DISTORTION:
[KNEES_PROXIMAL] [SHOULDERS_BARREL] [FOREHEAD_STRETCH]
[ARM_EXTENDED] [LOWER_BODY_PROXIMAL] [FATAL_PROPORTION]
[FINGER_PROXIMAL] [WIDE_CONTEXT] [EXTENDED_HAND]
[LENS_CURVATURE] [MIRROR_FRAME] [EDGE_COMPRESSION]

LENS TYPES:
[ULTRA_WIDE_0.5x] [WIDE_1x] [STANDARD_1.5x]

ANGLES:
[LOW_ANGLE] [EYE_LEVEL] [CHIN_UP] [CHIN_DOWN]
[TILTED_FORWARD] [ARM_OVERHEAD] [UPWARD_ANGLE]

HK SCENARIOS:
[ARM_OVERHEAD] [UPWARD_ANGLE] [NECK_FORESHORTEN] [THROAT_EXPOSED]
[STEAM_MIRROR] [PROXIMAL_MIRROR] [SHOULDERS_BARREL] [FOG_EDGE]
[MTR_CROWD] [PROXIMAL_STRANGER] [ARM_RAISED] [MOTION_BLUR]
[FLUORESCENT_LIGHT] [ANGLE_SHOT] [GREEN_TINT] [SALLOW_SKIN]
[LOW_LIGHT] [NEON_REFLECT] [WET_SKIN_SHINE] [BOKEH_BACKGROUND]
[WHITENING_GLOW] [DIFFUSED_SKIN] [SPF_LUMINOSITY] [SOFT_EDGE]

HK CONTEXT:
[HONG_KONG] [MTR] [TEMP_STREET] [7_ELEVEN] [BATHROOM_STEAM] [NIGHT_MARKET]
```

---

*V15 Module: ENGINE_V15_SMARTPHONE_GEOMETRY_SYSTEM.md*
*Status: READY FOR INTEGRATION*
*Cross-ref: ENGINE_V15_POST_SWIM_SYSTEM (wet skin + humidity amplification)*
