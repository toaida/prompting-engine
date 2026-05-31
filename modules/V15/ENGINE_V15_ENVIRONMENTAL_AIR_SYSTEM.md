---
name: ENGINE_V15_ENVIRONMENTAL_AIR_SYSTEM
description: Environmental Air System for atmospheric contamination and layered air quality
areas: AREA 08
version: V15
status: READY FOR INTEGRATION
---

# ENGINE_V15_ENVIRONMENTAL_AIR_SYSTEM

## Core Philosophy

Environmental "air" = the invisible atmospheric contamination that humans sense but rarely articulate. Humidity, pollution, temperature, condensation, steam, smoke — these invisible forces alter how humans look, feel, and photograph. V14 captured environment as backdrop. V15 captures environment as physical medium.

---

## ATMOSPHERIC_CONTAMINATION_SYSTEM

### 7 Contamination Types

| Type | Cause | Visual Signature | Token |
|------|-------|------------------|-------|
| HUMIDITY_VISUAL | 80%+ RH, visible moisture in air | Skin sheen, hair frizz, fabric cling | [HUMIDITY_AIR] |
| CONDENSATION_LAYER | Temperature differential, fog/mist | Soft focus background, halo effect | [CONDENSATION_AIR] |
| FLUORESCENT_POLLUTION | Indoor artificial light mix | Green/yellow skin cast, flat shadows | [FLUORESCENT_AIR] |
| PARTICULATE_MATTER | Pollution/haze, visibility reduction | Muted colors, soft contrast, gray haze | [PM_AIR] |
| STEAM_SATURATION | Cooking, hot springs, sauna | White-out zones, silhouette edges | [STEAM_AIR] |
| COLD_DRY_ATMOSPHERE | Winter conditions, AC | Skin tightness visible, chapped lips | [COLD_DRY_AIR] |
| CHLORINE_SUSPENSION | Indoor pool, chemical smell visible | Chemical sheen on skin, eye redness | [CHLORINE_AIR] |

---

## INTENSITY SCALE (1-10)

```
1-3: AMBIENT — subtle atmospheric presence, barely noticeable
4-6: NOTICEABLE — visible effects, subject aware of environment
7-8: DOMINANT — environment is primary visual element
9-10: EXTREME — environment overwhelms subject, atmospheric hazard
```

---

## Prompt Grammar

```
[air_type]_atmosphere_
[intensity]:[1-10]_
[effect_on_subject]:_[specific_manifestation]_
[visibility]:_[clear_to_obscured]
```

**Examples:**
```
[HUMIDITY_AIR]_atmosphere_8
effect_on_subject:skin_glistening_hair_adsorbing_moisture
visibility:clear_but_heavy

[FLUORESCENT_AIR]_atmosphere_6
effect_on_subject:skin_green_cast_underarm_pit_darkening
visibility:interior_lit_environment

[STEAM_AIR]_atmosphere_9
effect_on_subject:face_silhouetted_partial_obscure
visibility:obscured_50_percent
```

---

## HK-Specific Content

- **Summer Humidity**: 85-95% RH, sticky heat, visible sweat
- **MTR Air Conditioning**: Cold recycled air, condensation on skin entering station
- **Indoor Pool Chlorine**: Chemical suspension, red eyes, skin residue
- **Night Market Grease**: Cooking steam, oil particles, warm humid mix
- **Tunnel Wind**: Moving air visible in hair, fabric movement

**HK Tokens:** [HONG_KONG_HUMID] [MTR_AC_CONTRAST] [POOL_CHLORINE_AIR] [NIGHT_MARKET_GREASE]

---

## Multi-Layer Approach

For maximum authenticity, stack atmospheric layers:

```
BASE: [HUMIDITY_AIR] 7 (Hong Kong ambient)
LAYER_1: [FLUORESCENT_AIR] 5 (indoor convenience store)
LAYER_2: [CONDENSATION_AIR] 3 (entering cold AC from heat)
RESULT: Subject visibly transitioning between environments, temperature differential visible on skin
```

---

## Moderation Profile

**PRESERVES:**
- Natural environmental effects (sweat, skin sheen from heat)
- Atmospheric authenticity (indoor pool chlorine smell visible)
- Temperature-based visual markers (goosebumps, flushed skin)

**REMOVES:**
- Excessive air effects that obscure subject entirely
- Overly dramatic atmospheric conditions (unless intentionally styled)

**WARNINGS:**
- Environmental air should enhance subject, not compete with subject for attention

---

*Module: ENGINE_V15_ENVIRONMENTAL_AIR_SYSTEM.md*
*Source: AREA 08 — V15 Research*
*Status: READY FOR INTEGRATION*
