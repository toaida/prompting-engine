---
name: ENGINE_V20_FOCUS_HIERARCHY_SYSTEM
description: Runtime system for reducing HDR/global sharpness and controlling visual competition.
areas: FOCUS / VISUAL PRIORITY / ANTI-HDR / PHOTOBOOK REALISM
version: V20.1
status: PRODUCTION-GUIDED DRAFT — NOT CANON UNTIL VALIDATED
---

# ENGINE_V20_FOCUS_HIERARCHY_SYSTEM

## Core Philosophy

A believable photobook image does not render everything with equal importance. It gives the viewer one primary emotional anchor, one secondary story cue, and lets the environment support the image as atmosphere.

## Activate When

- generated image feels HDR, globally sharp, or over-rendered
- background competes with face/body action
- HK details become tourist/location inventory
- fabric / shelf / sign / pavement micro-detail steals attention
- prompt contains many environment nouns

## Focus Budget

```
PRIMARY FOCUS: one emotional or action anchor
SECONDARY CUE: one object / local signifier that explains the moment
ATMOSPHERE: low-contrast HK texture, soft local cues, mood field
SUPPRESSION: no HDR, no equal-sharp background, no over-detailed props
```

## Runtime Tokens

### FH-01 FACE_LOCK
`face is the only fully resolved emotional focus plane; eyes and mouth carry the read; background lower contrast / cooler / less saturated`

### FH-02 HAND_ACTION_LOCK
`near hand and object contact are sharp enough to explain the action; face remains emotional destination; surrounding objects softened`

### FH-03 SILHOUETTE_LOCK
`overall silhouette and weight shift are readable; fabric texture secondary, not micro-detailed`

### FH-04 LOCAL_CUE_LOCK
`one local HK cue establishes place; other signs dissolve into soft color blocks`

### FH-05 MEMORY_SOFT_FIELD
`soft photobook focus, low global contrast, only expression/gesture slightly cleaner than environment`

### FH-06 BACKGROUND_SUPPRESSION
`background is not a showcase: no crisp poster wall, no HDR storefronts, no equal-detail passersby`

### FH-07 MOTION_LOCK
`hair / clothing / background carry slight directional motion blur while face remains sharp enough to read; movement creates hierarchy without HDR crispness`

## Depth + Color Budget

```
Near plane (0-1.5m): subject + one story cue, fully resolved
Mid plane (1.5-4m): atmosphere cues, 40-60% contrast reduction
Far plane (4m+): texture only, 70-80% contrast reduction, no readable text
Edges: 10-15% vignette or soft falloff
Skin: +5-10% warmer than environment
Background: -10-20% saturation, cooler / darker than subject
```

## Suppression Priority

If instructions conflict, protect hierarchy in this order:
1. face / hand-action emotional readability
2. physical interaction legibility
3. one local cue
4. atmospheric texture
5. suppress all remaining detail

## Prompt Grammar

```
FOCUS HIERARCHY: primary focus = [anchor]; secondary cue = [one object/local cue];
atmosphere = [soft environmental field]; suppression = [what must not compete].
```

## Production Fragment

```
FOCUS HIERARCHY: primary focus = her face turning back mid-step; secondary cue = red taxi reflection under her shoes;
atmosphere = softened Traditional Chinese signs, wet pavement glow, umbrella edge blur;
suppression = signs not readable, storefronts not HDR, passersby not sharp, no global micro-detail.
```

## Anti-Patterns

- global `ultra-detailed` language
- crisp shelves, signs, posters, product labels everywhere
- every HK cue rendered as a landmark
- fabric folds more detailed than face
- no dark/blown/soft dead zones

## Production Validation Needed

Test against next 10-20 outputs. Promote to canon only if it visibly reduces HDR/global-sharp/background competition without making images muddy.
