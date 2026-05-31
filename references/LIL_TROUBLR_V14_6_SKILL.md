# LIL_TROUBLR V14.6 — MEMORY REALISM PHASE
### Quick Reference Skill for lil.troublr Engine V14.6
### Status: ACTIVE — Primary Prompting Reference

---

## WHAT IS V14.6

**One-liner:** Generate images that feel recovered, not rendered — emotionally remembered human moments, not designed aesthetic content.

**Core philosophy shift:**
```
OLD: " girl's posture + environment backdrop + good lighting"
NEW: "Environment creates conditions → body responds → camera intercepts moment → image feels like memory fragment"
```

**V14.6 priority hierarchy (HIGH → LOW):**
1. Motion — partial blur, shutter lag, turning-body softness
2. Interruption — incomplete frame, environmental obstacle
3. Environmental Influence — weather physically causes fabric/body changes
4. Emotional Timing — expression caught before/after/during formation
5. Imperfect Framing — accidental crop, horizon tilt, off-composition
6. Environmental Memory — emotional color encoding, memory-not-accurate

**Attraction mechanics shift:**
- V14.5: aesthetic-admiration (viewer wants TO BE subject)
- V14.6: proximity-desire (viewer wants TO BE WITH subject)

---

## 8-LAYER PROMPT STRUCTURE

Use this for EVERY generation. All 8 layers required.

### LAYER 1 — IDENTITY LOCK
```
"Create a photorealistic image of lil.troublr: stable facial geometry, soft oval face, slight apple-cheek fullness, expressive almond-shaped eyes, chestnut-dark layered hair, softly full lips, realistic warm East Asian skin texture, tiny faint beauty mark beside left eye near outer corner, 170cm mature hourglass silhouette expressed through fabric behavior and posture, not anatomy-first framing. No face drift, no generic influencer face."
```
**Trigger:** ALL generation sessions. Re-anchor every 20-30 generations.

---

### LAYER 2 — ENVIRONMENT CAUSATION FIRST ⭐ V14.6 NEW PRIORITY
```
"[ENVIRONMENT TYPE]: [specific location from families A-E]
— [weather type if present: rain/wind/humidity/heat/cool]
— [physical causation chain visible in scene]
— [environment-specific HK texture]"
```
**Families:**
- A (Transitional): MTR corridor, ferry boarding, airport, elevator, parking garage stairwell
- B (Micro-destinations): Bowling shoe rental, photo booth, laundromat, karaoke waiting, badminton bench
- C (Domestic): Apartment entrance, bathroom mirror after shower, kitchen late-night, couch after nap, balcony
- D (Weather-dominated): Typhoon shelter, humid bus stop, post-rain reflections, windy harbor, overcast ferry terminal
- E (Transportation): Late-night taxi, ferry window seat, MTR peak hour, bus upper deck corner

**Weather trigger examples:**
- "Rain just stopped outside MTR exit" → FABRIC wet + HAIR humidity + PAVEMENT reflections
- "HK summer midnight humid heat" → HUMIDITY hair + FABRIC soft + SWEAT skin
- "Strong wind on harbor walkway" → WIND hair blown back + FABRIC billowing + BODY lean into wind

---

### LAYER 3 — CAMERA AWARENESS (Level 3 = PRIMARY)
```
"[AWARENESS LEVEL]: [choose one]
— Level 1 = influencer (performative, knowingly documented)
— Level 2 = friend-shot (acknowledged but casual)
— Level 3 = forgotten PRIMARY (in her moment, camera intercepted) ⭐
— Level 4 = documentary (observer at distance, subject unaware)"
```
**Rule:** Level 3 or 4 for 80%+ of generations. Level 1 only with non-revealing content.

---

### LAYER 4 — MEMORY CAPTURE (imperfect by design)
```
"[MEMORY CAPTURE TYPE]: [minimum 1, combine 2-3 for compound]
— [INCOMPLETE FRAMING]: body partly leaving frame, accidental crop, horizon tilt
— [MOTION CONTAMINATION]: slight blur from walking, shutter lag softness
— [EMOTIONAL TIMING]: before smile apex, eye contact reconnecting, interrupted laugh
— [ENVIRONMENTAL INTERRUPTION]: umbrella edge, wind blur, obstructed object
— [CAMERA MEMORY BEHAVIOR]: imperfect focus, uneven exposure, slow shutter"
```
**Rule:** Expression must be IN-PROCESS, not at apex. Camera chose moment over composition.

---

### LAYER 5 — COLOR MEMORY (emotionally encoded, not accurate)
```
"[COLOR MEMORY SYSTEM]: [film stock or behavior]
— Kodak Gold 200: warm golden nostalgia (late afternoon)
— Fuji Pro 400H: cool dreamy memory (cloudy/overcast)
— CineStill 800T: tungsten night street magic (orange/blue war)
— Disposable Camera: harsh flash social doc (party/concert)
— CCD (Y2K lo-fi): warm imperfect realism (early 2000s casual)
— Smartphone HDR: too-detailed slightly uncanny (phone documentation)
— HK Humidity Tungsten: yellow haze summer night HK ⭐
— Mixed Light: orange tungsten + blue daylight warring
— Moonlight: cool blue preservation (clear night outdoor)
— Shadow Color: blue shadows, sky reflected in dark
— Low-Cost Lens: soft center, warm, imperfect optical"
```
**Anti-AI critical:** Preserving mixed-light OR CineStill orange/blue war OR shadow-blue retention = specific anti-corrections that stop AI's color-correction tendency.

---

### LAYER 6 — DISTANCE + PERSPECTIVE
```
"[DISTANCE SYSTEM]: [emotional contract]
— Close (DIS-01): intimacy "I am near her" — skin texture, shallow DOF
— Friend-shot (DIS-02): belonging "I could be in this photo" — group present
— Observational (DIS-03): voyeur tension "watching from outside" — 20-40% frame
— Forgotten-camera (DIS-05) ⭐ PRIMARY: "memory fragment" — 15-35% frame, imperfections
— Close Overhead (DIS-06): tender softness — morning/domestic intimacy
— Disposable Flash (DIS-09) ⭐ SOCIAL: "real night" — harsh flash, oversaturated, chaotic grain
— Group (DIS-10): belonging "these are my friends" — social warmth

"[PERSPECTIVE if applicable]:
— Eye-level: neutral friend-shot realism
— Slight high: cute vulnerability, selfie realism
— Ground-level ⭐: ankle-knee height, environment dominant, sky 40-70% ⭐V14.6 SPECIAL
— Worm-eye ONLY if: environment scale emphasis, human small, atmospheric presence"
```

---

### LAYER 7 — PHYSICAL FEEDBACK (environment-to-body causation)
```
"[HUMIDITY HAIR]: flyaways expanding, hair clumping near temple, strand to cheek
"[AIR-CON STATIC]: hair lifting then settling, slight cling to body
"[WET FABRIC]: heavier, clings, darker, more transparent (light fabric especially)
"[HUMID FABRIC]: softness, different drape, body contour more visible
"[SWEAT]: neck/back/under-bust sheen through fabric, humidity response
"[BODY CONSEQUENCE]: gravity compression, surface contact points"
```
**Rule:** Hair behavior = environment-caused, NOT aesthetic choice.
**Rule:** Wet fabric = weather-caused physics, NOT wet-looking styling.

---

### LAYER 8 — EXPRESSION + NARRATIVE RESIDUE
```
"[FACS EXPRESSION]: cheek raise unevenly → mouth corner lifts one side first
— [EYE DIRECTION]: off-camera listening, reconnection after laugh
— [ASYMMETRY]: smile forming on one side, imperfect and real
— [TRANSITIONAL]: recovered from laugh, mid-thought pause
"[NARRATIVE RESIDUE]: half-drunk drink, receipt folded under phone
"[DISCOVERY MOMENT]: one small detail noticed 1 second after first look
```

---

## FILE REFERENCE LIST

All V14.6 core modules in `/Engine/`:

| File | Purpose |
|------|---------|
| `ENGINE_V14_...SYSTEM.md` | Master file (start here, contains appendices) |
| `MEMORY_CAPTURE_SYSTEM.md` | 5 imperfect memory systems |
| `CAMERA_AWARENESS_SYSTEM.md` | 4 awareness levels (Level 3 = primary) |
| `ENVIRONMENT_EXPANSION_SYSTEM.md` | 50+ specific environment spaces (A-E) |
| `ENVIRONMENTAL_COLOR_MEMORY_SYSTEM.md` | 11 film stock memory systems |
| `WORM_EYE_ENVIRONMENT_SYSTEM.md` | 7 ground-level environmental immersion |
| `CAMERA_DISTANCE_PSYCHOLOGY.md` | 10 distance systems |
| `HUMIDITY_HAIR_BEHAVIOR_SYSTEM.md` | Humidity + air-con hair physics |
| `FABRIC_CAUSALITY_SYSTEM.md` | Weather → fabric → body causation |
| `COMPOUND_LAYER_SYSTEM.md` | Compound anti-AI layer combinations |
| `REALISM_PHILOSOPHY_V14_6.md` | Full architecture evolution + anti-AI logic |

---

## QUICK GENERATE CHEAT SHEET

### Recipe 1: TYPICAL HK SCENE
```
Layer 1: lil.troublr identity
Layer 2: A/B-family environment + weather present
Layer 3: Level 3 forgotten
Layer 4: Emotional timing + incomplete framing
Layer 5: HK Humidity (COL-07) or Mixed Light (COL-08)
Layer 6: Friend-shot (DIS-02) or Forgotten (DIS-05)
Layer 7: Humidity hair + fabric causal
Layer 8: FACS expression in-process + narrative residue
```

### Recipe 2: SOCIAL PARTY
```
Layer 1: lil.troublr identity
Layer 2: Indoor late-night B-family micro-destination
Layer 3: Level 3 forgotten
Layer 4: Emotional timing + motion contamination
Layer 5: Disposable Camera (COL-04) ⭐
Layer 6: Disposable Flash (DIS-09) ⭐
Layer 7: Warm fabric + sweat evidence
Layer 8: Suppressed laugh recovery + discovery moment
COMPOUND: PARTY_SOCIAL_AUTHENTICITY
```

### Recipe 3: RAIN HK NIGHT
```
Layer 1: lil.troublr identity
Layer 2: D-family weather-dominated environment
Layer 3: Level 3 forgotten (weather-caught)
Layer 4: Environmental interruption (rain) + emotional timing
Layer 5: CineStill 800T (col-03) + HK Humidity (col-07) ⭐
Layer 6: Close distance (DIS-01)
Layer 7: WET FABRIC + wet hair ⭐⭐⭐ weather-caused
Layer 8: Physical rain reaction + half-drunk shelter moment
COMPOUND: WEATHER_PHYSICAL_CAUSATION
```

### Recipe 4: DOCUMENTARY STREET
```
Layer 1: lil.troublr identity
Layer 2: A-family transitional OR D-family weather
Layer 3: Level 4 documentary (max camera absence)
Layer 4: Imperfect focus + incomplete framing
Layer 5: Shadow color (COL-11) + mixed light
Layer 6: Ground level (WRM-01) + observational (DIS-03) ⭐
Layer 7: Wind hair + fabric billowing (if weather present)
Layer 8: Transitional behavior + environment dominant
COMPOUND: GROUND_LEVEL_DOCUMENTARY
```

---

## MODERATION RULES (6 HARD RULES)

1. **No glamour framing** — worm-eye = environmental immersion (human small + environment dominant), NEVER = body elongation for display
2. **Physical causation required with revealing content** — wet fabric = weather-caused, not stylistic wet-look
3. **Camera awareness Level 3/4 required for intimate distances** — no Level 1 with proximate distance + exposure
4. **Incomplete frame = accident, not display** — camera chose moment, never intentional reveal crop
5. **Disposable compound = PRESERVE ALL FLAWS** — harsh flash, oversaturation, chaotic grain, off-composition. DO NOT CORRECT.
6. **Emotional depth replaces visual intensity** — attraction from proximity-desire, not aesthetic-admiration

---

## ANTI-AI COMPOUND QUICK REFERENCE

| Scene | Compound Layers | Anti-AI Level |
|-------|----------------|--------------|
| Social party | DIS-09 + CAM-03 + MEM-03 + MEM-01 + COL-04 | EXTREME |
| Tender domestic | DIS-01 + CAM-03 + MEM-03 + MEM-01 + COL-01 | HIGH |
| Rain HK night | FAB-01 + MEM-04 + MEM-03 + COL-03 + COL-07 | EXTREME |
| Ground documentary | WRM-01 + DIS-03 + COL-11 + MEM-01 + CAM-04 | HIGH |
| Ferry memory | DIS-05 + COL-01 + E-series + MEM-03 | HIGH |

---

## AVOID LIST (V14.6 SPECIFIC)

❌ Subject-first framing
❌ Environment-as-backdrop
❌ Perfect color correction (leave emotional contamination)
❌ Peak expression (must be in-process)
❌ Rule-of-thirds (imperfect composition)
❌ Clean technical quality (noise/grain/soft focus = assets)
❌ Designed composition (accidental = authentic)
❌ Glamour low-angle (body elongation for display)
❌ Weather as aesthetic (must be causal physics)
❌ Wet fabric without weather (if wet, must be weather-caused)
❌ Disposable without SOCIAL context (party/friends ganging)
❌ Forgotten-camera without ENVIRONMENT dominant

---

## V14.6 STATUS

**Version:** lil.troublr Engine V14 — Memory Realism Phase — V14.6
**Philosophy:** Emotionally remembered human existence
**Architecture:** Environment → Causation → Body → Camera → Image as Memory Fragment
**Anti-AI:** Compound layers (multiple markers simultaneously unreplicable)
**Attraction:** Proximity-desire not aesthetic-admiration

**All modules:** `~/Documents/lil.troublr/Engine/`
**Master file:** `ENGINE_V14_WORLD_COHERENT_SOCIAL_PHOTOGRAPHY_SYSTEM.md`
**Research archive:** `V14_RESEARCH_v14_6/`
