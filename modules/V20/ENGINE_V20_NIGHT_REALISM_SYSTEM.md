---
name: ENGINE_V20_NIGHT_REALISM_SYSTEM
description: Runtime system for realistic night lighting, camera behavior, weather, and HK night atmosphere.
areas: LIGHTING / NIGHT / WEATHER / CAMERA QUALITY
version: V20
status: ACTIVE — AUTO-MERGED
---

# ENGINE_V20_NIGHT_REALISM_SYSTEM

## Core Philosophy

Night is not day with brightness turned down. Night is a different physics system.

AI night fails because it averages light. Real night has:
- visible light sources
- hard falloff
- deep shadows
- mixed color behavior
- noise, bloom, bokeh, motion blur
- human behavior shaped by safety, weather, and social context

---

## Light Source Selection Rule

Choose one dominant source and 1-2 modifiers.

| Source | Behavior |
|---|---|
| `NEON_LED_SIGN` | saturated color cast, directional, not full-scene light |
| `STREET_LAMP_TOP` | warm/orange top light, eye sockets can shadow |
| `PHONE_SCREEN_GLOW` | cool upward face light, intimate/private |
| `WINDOW_SPILL` | warm rectangle of interior light |
| `CAR_HEADLIGHTS` | moving white/yellow directional streaks |
| `TAXI_TAILLIGHT_RED` | red reflections on wet pavement |
| `CONVENIENCE_STORE_WHITE` | harsh white storefront spill |
| `FIRE_LIGHTER_CANDLE` | very warm small flickering source |
| `CITY_GLOW_AMBIENT` | diffuse low-level base, not directionless daylight |

Single-source scenes are allowed if light behavior is complex: fog, rain, reflections, or strong falloff.

---

## Night Skin Rendering

Skin must take color from the source.

| Light | Skin Effect | Shadow |
|---|---|---|
| Pink/magenta LED | flushed, romantic, saturated highlights | deep magenta |
| Blue LED / phone | cool, pale, private | blue-black |
| Orange street lamp | warm, golden, gritty | brown-orange |
| Window spill | soft warm patches | neutral dark |
| Moon / city haze | silver or grey-blue depending atmosphere | diffuse |

**Correction:** neon colors are spectral, not color-temperature values. Do not assign Kelvin to saturated pink/blue; describe color cast directly.

---

## Camera Settings for Prompt Realism

Use when prompt supports photography style:

```
wide aperture equivalent f/1.4-f/2.8, shallow depth of field,
ISO 800-6400 shadow grain, handheld shutter 1/30-1/125,
0.7-1.3 stops underexposed to preserve highlights,
small lens flare from bright sign, bokeh from distant lights
```

---

## Night Time Bands

| Time | Behavior | Visual |
|---|---|---|
| `BLUE_HOUR` | city lights turning on | sky still colored, mixed natural/artificial |
| `EARLY_NIGHT` | peak social activity | crowds, food, shops open |
| `LATE_NIGHT` | bars, taxis, tired transit | fewer people, more intimate |
| `DEEP_NIGHT` | minimal activity | street lamps, quiet, safety tension |
| `DAWN_TRANSITION` | artificial lights + brightening sky | exhausted, nostalgic, soft contrast |

---

## HK Night Signatures

- humidity haze around lights
- wet pavement/reflections after rain
- LED signs with traditional Chinese characters
- 7-Eleven / Circle K white glow
- red taxi lights and queue
- late-night noodles / dai pai dong steam
- MTR last-train fatigue
- narrow street light canyon
- umbrella behavior in rain

---

## Mood Tokens

| Token | Use |
|---|---|
| `NEON_NOIR_HK` | wet street, magenta/cyan, confidence |
| `WARM_NIGHT_FOOD` | street food, window spill, comfort |
| `LATE_NIGHT_ALONE` | phone glow, transit, quiet vulnerability |
| `NIGHT_SOCIAL` | friends, drinks, mixed light, movement |
| `RAIN_NIGHT_REFLECTION` | puddles, droplets, doubled lights |
| `FOG_MIST_NIGHT` | halos, softened signs, reduced contrast |

---

## Anti-Pattern Detection

1. Cover all visible lights. If subject still looks evenly lit → `AI_FLAT_NIGHT`.
2. Check shadows. If no near-black areas → overexposed night.
3. Check skin. If shadow skin equals lit skin → `DAY_FACE_AT_NIGHT`.
4. Check background. If as bright as foreground → no falloff.
5. Zoom shadows. If no grain/noise at all → too clean.
6. Check HK night. If no signage, humidity, crowd, reflection, or local behavior → generic.

---

## Production Example

```
HK late-night taxi queue, NIGHT_REALISM: convenience store white light from right, red taxi tail-light
reflection on wet pavement, phone screen glow under her chin as she checks WhatsApp, shallow depth of field,
ISO grain in shadows, 1 stop underexposed, Chinese LED signs blurred in background, tired but amused expression
```
