# AREA 06: AI NOISE REDUCTION SYSTEM

## The Problem

Current engine occasionally produces:
- Crunchy skin (over-sharpened pores)
- Oversharpened details (fake microdetail)
- Noisy fabric texture (hallucinated texture)
- HDR contamination (overprocessed highlights)
- Overprocessed skin (too much "detail")
- Texture hallucination (AI tries to show texture, creates noise)

Research: **Why too much "detail" creates AI feeling.**
Real cameras preserve softness. Real detail has hierarchy — some things sharp, some soft.

---

## OPTICAL_SOFTNESS_LIBRARY

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

## Natural Detail Hierarchy

### Principle

Real images have **detail hierarchy** — some things detailed, some soft. AI makes everything equally detailed = uncanny.

### Hierarchy Rules

```
DETAIL_HIERARCHY_MATRIX:

HIGHEST DETAIL: Face (especially eyes, mouth)
HIGH DETAIL: Skin (subject's)
MEDIUM DETAIL: Immediate clothing (subject's)
LOW DETAIL: Background props
LOWEST DETAIL: Background environment (far)
NEAR-ZERO: Extreme edges

ANTI-AI RULE: If background is as sharp as face = AI
```

### Prompt Grammar

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

## Anti-Crunch Realism System

### Crunchy Skin Causes

AI skin looks "crunchy" when:
1. Over-sharpened individual pores
2. Noise added to skin texture
3. Every pore equally visible
4. Skin has "texture" without softness
5. Edge enhancement on skin

### Solutions

```
ANTI_CRUNCH_PRESCRIPTION:

1. Use: [SENSOR_SMOOTH_SKIN] — sensor NR softens skin
2. Use: [WIDE_APERTURE_SOFT] — shallow DOF de-focuses skin edges
3. Use: [LOW_LIGHT_SOFT] — natural grain masks AI texture
4. Avoid: Detail emphasis on skin
5. Avoid: Pore visibility as "detail"
6. Rule: Skin should look like skin, not pore map
```

### Texture Density Balancing

| Scene Type | Texture Level | Reason |
|-----------|---------------|--------|
| Close-up face | LOW texture | Skin softness, intimacy |
| Medium shot body | MEDIUM texture | Visible but not crunchy |
| Wide environmental | LOW texture | Background fades |
| Night/low light | VERY LOW | Grain dominates texture |
| Flash | VERY LOW | Flattened, soft |

---

## HK-Specific Optical Situations (EXPANDED)

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

**ANTI-AI Rule Correction:** "If background is as sharp as face = AI" is slightly wrong. Modern smartphone Portrait mode achieves sharp backgrounds. Correct rule: "If background has AI-like uniform sharpness (no lens falloff, no optical aberration) = AI."

---

*Research: AREA 06 — AI Noise Reduction System*
*Status: IN PROGRESS — Ready for DeepSeek verification + extension*