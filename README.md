# lil.troublr Prompting Engine

A research-driven prompting system for generating photorealistic, emotionally authentic virtual KOL content that simulates human social existence — not perfect AI beauty rendering.

**GitHub:** https://github.com/toaida/prompting-engine

---

## What Is This?

The lil.troublr engine generates images of a consistent virtual character (a 24-year-old Hong Kong woman) inside believable social moments. The system prioritizes:

- **Environmental causation** — world creates conditions, body responds
- **Camera authenticity** — bad photo realism, social documentation behavior
- **Emotional timing** — expressions as transitional states, not frozen poses
- **Anti-formula diversity** — 打破重複模式，模擬真實人類社交存在
- **Life entropy** — non-photo-worthy moments, failed beauty, ugly-cute
- **Continuity persistence** — objects and beauty states carry across sessions

This is NOT:
- Anime prompting
- Generic beauty rendering
- Over-polished glamour photography
- Cyberpunk character design

---

## Quick Start — Load This First

**→ [core/ENGINE_MASTER.md](core/ENGINE_MASTER.md)**

The consolidated master file contains all V16 systems in one place:
- 7 streetwear categories (35+ architectures)
- 5 posture categories (35+ silhouettes)
- 8 camera distances
- 5 emotional rhythm categories
- Daily entropy tokens
- Failed beauty tokens
- Object memory tokens
- Social chaos tokens
- Weather temperature tokens
- Beauty degradation tokens
- Low-stakes photo tokens
- Platform ecology tokens
- Full prompt inject string

**For GPT/AI use**: Load `core/ENGINE_MASTER.md` only. This is the definitive source.

---

## Version History

| Version | Date | Key Features |
|---------|------|--------------|
| V14 | ~2024 | World-coherent social photography, memory realism, V14.6 upgrade |
| V15 | 2025 | Bad photo realism (26 failure types), continuity persistence, photodump rhythm |
| V16 | May 31, 2026 | Anti-formula diversity, life entropy, object memory, social chaos, beauty degradation |

---

## Directory Structure

```
/Engine/
├── core/
│   └── ENGINE_MASTER.md          ← DEFINITIVE SOURCE (load this)
│
├── modules/
│   ├── ENGINE_V16_ANTI_FORMULA_STREETWEAR_SYSTEM.md
│   ├── ENGINE_V16_ANTI_FORMULA_EMOTIONAL_SYSTEM.md
│   ├── ENGINE_V16_DAILY_ENTROPY_SYSTEM.md
│   ├── ENGINE_V16_OBJECT_SOCIAL_SYSTEM.md
│   ├── ENGINE_V16_PHOTO_WEATHER_SYSTEM.md
│   └── ENGINE_V16_BEAUTY_PLATFORM_SYSTEM.md
│
├── archive/                      ← OLDER VERSIONS (do not load)
│   ├── V14_RESEARCH_*/
│   ├── V15_RESEARCH/
│   ├── V16_ANTI_FORMULA_RESEARCH/
│   ├── V16_LIFE_ENTROPY_RESEARCH/
│   ├── ENGINE_V14_*/
│   ├── ENGINE_V15_*/
│   └── [other old files]
│
├── ENGINE_V14_WORLD_COHERENT_SOCIAL_PHOTOGRAPHY_SYSTEM.md   ← V14 core (still valid)
├── ENGINE_V15_BAD_PHOTO_REALISM_SYSTEM.md                  ← V15 core (still valid)
└── [other V14/V15 support modules]
```

---

## Usage with AI Models

1. **Load the consolidated master:**
   ```
   Load core/ENGINE_MASTER.md
   ```
   This contains all V16 systems (~650 tokens) organized for AI consumption.

2. **For specialized needs**, load specific module from `/modules/`:
   - Need streetwear/outfit → `modules/ENGINE_V16_ANTI_FORMULA_STREETWEAR_SYSTEM.md`
   - Need emotional variation → `modules/ENGINE_V16_ANTI_FORMULA_EMOTIONAL_SYSTEM.md`
   - Need bad photo realism → `ENGINE_V15_BAD_PHOTO_REALISM_SYSTEM.md`
   - Need world coherence → `ENGINE_V14_WORLD_COHERENT_SOCIAL_PHOTOGRAPHY_SYSTEM.md`

3. **Apply anti-repetition rules** before generating (see ENGINE_MASTER.md)

4. **Generate** using the Full Prompt Inject String at the bottom of ENGINE_MASTER.md

---

## Example Prompt Flow

```
Create a photorealistic image of lil.troublr.

[Load core/ENGINE_MASTER.md — full V16 system]

Before generating, verify:
□ No repeated silhouette in 10 images
□ 3+ different camera distances
□ 2+ different outfit families
□ ≤2 hero shots per 10 images
□ 3+ "not-a-photo" moments
□ Object continuity maintained
□ 1+ ugly-cute moment

Generate using tokens from ENGINE_MASTER.md.
Apply NOT_PHOTO_MOMENT_GRAMMAR for entropy shots.
Apply UGLY_CUTE_GRAMMAR for failed beauty moments.
```

---

## Character Identity

**lil.troublr** is a 24-year-old Hong Kong woman:
- 170cm tall, mature hourglass silhouette
- Soft oval face, almond eyes, chestnut-dark layered hair
- Tiny beauty mark beside left eye
- Realistic East Asian skin texture with natural pores
- Warm, natural attractiveness — not optimized beauty

**Identity must be preserved** across all generations.

---

*V16: Anti-formula, anti-perfection, anti-optimization. Simulate human existence.*
