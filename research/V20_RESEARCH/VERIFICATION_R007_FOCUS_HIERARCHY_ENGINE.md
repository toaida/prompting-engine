# Verification & Extension: R007_FOCUS_HIERARCHY_ENGINE

## Verification Notes

**Strengths Confirmed:**
- Core diagnosis ("equal importance") is correct and matches observed production failures
- Focus budget concept is production-viable and reduces prompt bloat
- Taxonomy (FH-01 through FH-06) covers the main failure modes
- Failure cases table is accurate and actionable

**Gaps Identified:**

1. **No metric for "how much softer"** — The engine says "background lower contrast" but doesn't specify how much. In production, this leads to inconsistent results across models.

2. **Missing: depth-of-field realism rules** — Real photobooks use specific aperture-equivalent behaviors (e.g., f/2.8 on 35mm gives ~2-3 stops of falloff). The engine doesn't specify focal length or distance relationships.

3. **No suppression priority order** — When multiple suppression targets conflict (e.g., "soft background" vs. "readable sign"), there's no rule for which wins.

4. **Missing: color temperature hierarchy** — Real gravure often uses warmer skin tones vs. cooler backgrounds. This is a cheap, reliable way to create hierarchy without sharpness changes.

5. **No handling of motion blur** — Street photography often uses subject motion (hair, hand, clothing) as a hierarchy tool. The engine only discusses static focus.

6. **Missing: frame-edge treatment** — Real photobooks often let edges go soft or dark. The engine mentions "dead zones" but doesn't specify how to prompt them reliably.

---

## Corrections

### Correction 1: Focus Budget Rule — Add Distance Relationship

**Original:**
```
1 sharp emotional anchor
+ 1 readable story cue
+ 2-4 low-contrast local atmosphere cues
+ explicit suppression of everything else
```

**Corrected:**
```
1 sharp emotional anchor (within 1-2m of camera)
+ 1 readable story cue (within same plane or slightly behind)
+ 2-4 low-contrast local atmosphere cues (3m+ distance)
+ explicit suppression of everything else (edges, deep background, non-essential foreground)
```

**Why:** Real depth-of-field physics means distance from camera is the primary hierarchy driver. The engine was missing this spatial constraint.

### Correction 2: FH-01 FACE_LOCK — Add Skin Tone Priority

**Original:**
`face is the only fully resolved focus plane, eyes and mouth carry the emotional read, background falls into lower-contrast street texture`

**Corrected:**
`face is the only fully resolved focus plane, skin tone slightly warmer than environment, eyes and mouth carry the emotional read, background falls into lower-contrast street texture with cooler color cast`

**Why:** Color temperature difference is a reliable hierarchy tool that works even when sharpness is similar.

### Correction 3: Failure Case — Add "Soft Background But No Anchor"

**New row in failure table:**

| Failure | Why It Happens | Prevention Rule |
|---|---|---|
| Soft background but subject also soft | "soft focus" applied globally without specifying anchor | always pair soft background with `face or hand-action slightly clearer` |

---

## Extensions

### Extension 1: Depth Budget Rule (New)

Add to Part 2:

```
DEPTH BUDGET:
- Near plane (0-1.5m): subject + one story cue, fully resolved
- Mid plane (1.5-4m): atmosphere cues, 40-60% contrast reduction
- Far plane (4m+): texture only, 70-80% contrast reduction, no readable text
- Edges: 10-15% vignette or soft falloff
```

**Production impact:** Prevents the "everything at f/8" look that makes AI images feel like real estate photography.

### Extension 2: Color Hierarchy Rules (New section after Part 3)

```
COLOR HIERARCHY:
- Subject skin: +5-10% warmth vs. environment
- Story cue object: neutral or slightly saturated
- Atmosphere: -10-15% saturation, cooler white balance
- Suppressed areas: -20% saturation, +5% black point

Rule: Never let background colors be more saturated than skin.
Exception: Neon signs at night (but keep them small in frame).
```

**Production impact:** Cheap, reliable way to create hierarchy without fighting model sharpness defaults.

### Extension 3: Motion Hierarchy (New FH-07)

```
FH-07 MOTION_LOCK
Subject movement creates hierarchy through blur contrast.

Prompt language:
`her hair and clothing show motion blur from walking, face remains sharp enough to read expression, background has directional motion blur matching her speed`

Use for: street crossing, MTR platform, escalator, walking through market.

Failure prevented: static-looking street photos.
```

### Extension 4: Frame Edge Treatment (Add to Part 3)

Add to all FH types:

```
FRAME EDGE RULE:
- Bottom 5-10% of frame: allow darkening, blur, or crop
- Top 5-10%: allow highlight blowout or soft falloff
- Left/right edges: one side slightly darker or softer than center
- Never center the subject with equal sharpness to all edges
```

**Production impact:** Prevents the "centered subject, everything equally sharp" look that screams AI.

### Extension 5: Suppression Priority Order (New section after Part 5)

```
SUPPRESSION PRIORITY (when conflicts arise):
1. Face/emotion always wins (never suppress expression)
2. Story cue readability second (must be legible enough to understand action)
3. Atmosphere texture third (can be partially suppressed)
4. Deep background last (most aggressively suppressed)

If model cannot do all: sacrifice deep background first, then atmosphere, never face.
```

---

## Production Tests

### Test 1: Baseline vs. Hierarchy

**Prompt A (baseline):**
```
lil.troublr in a cha chaan teng, holding iced milk tea, wet street visible through window, traditional signs, neon glow, detailed interior, sharp everywhere
```

**Prompt B (with R007):**
```
lil.troublr in a cha chaan teng, holding iced milk tea
FOCUS HIERARCHY: primary focus = her face and near hand on glass; secondary cue = condensation on glass; atmosphere = soft warm interior, window street blur; suppression = no sharp signs, no HDR interior, no equal-detail background
DEPTH BUDGET: near plane sharp, mid plane 50% contrast, far plane texture only
COLOR HIERARCHY: skin +5% warmth, atmosphere -10% saturation
FRAME EDGE: bottom 10% darker, right edge soft falloff
```

**Expected result:** B should show stronger emotional connection to subject, less "location showcase" feel.

### Test 2: Suppression Language Comparison

Compare:
- Negative-only: `no HDR background, no sharp signs, no equal-detail passersby`
- Positive-only: `background lower contrast, signs softened into color blocks, passersby not resolved`
- Combined: both

**Expected result:** Combined should work best; positive-only may be ignored by some models; negative-only may create artifacts.

### Test 3: Color Hierarchy Test

Same scene, two versions:
- Version A: no color hierarchy specified
- Version B: `skin +5% warmth, atmosphere -10% saturation, cooler background`

**Expected result:** B should show better subject separation even if sharpness is similar.

### Test 4: Frame Edge Test

Compare:
- Centered subject, equal sharpness to edges
- Subject slightly off-center, bottom 10% darker, right edge soft

**Expected result:** Second version should feel more photobook-like and less synthetic.

### Test 5: Motion Hierarchy Test

Prompt:
```
lil.troublr walking through Mong Kok market, evening
FOCUS HIERARCHY: primary focus = her face turning back; secondary cue = hand holding phone; atmosphere = blurred market stalls, motion-blurred passersby; suppression = no sharp background details
MOTION: her hair and clothing show walking blur, face sharp, background has directional blur
```

**Expected result:** Should feel like a real street photo, not a staged shot.

---

## Confidence Adjustment

**Original confidence: 0.86 / 1.00**

**Adjusted confidence: 0.78 / 1.00**

**Reason for downgrade:**
- Missing spatial constraints (distance relationships) means the engine may produce inconsistent results across different scenes
- No color hierarchy rules means the engine relies entirely on sharpness, which is the most model-dependent variable
- No motion hierarchy means the engine misses a key real-photography tool
- No frame edge treatment means the engine may still produce centered, evenly-lit images
- Suppression priority was undefined, which will cause conflicts in complex scenes

**To reach 0.90+:** Production validation of Tests 1-5, plus integration of Depth Budget, Color Hierarchy, and Frame Edge rules into the core engine.

---

## Summary of Changes Needed

| Item | Type | Priority |
|---|---|---|
| Add distance relationship to Focus Budget | Correction | High |
| Add skin tone warmth to FH-01 | Correction | Medium |
| Add "soft background no anchor" failure case | Correction | Medium |
| Add Depth Budget Rule | Extension | High |
| Add Color Hierarchy Rules | Extension | High |
| Add FH-07 Motion Hierarchy | Extension | Medium |
| Add Frame Edge Treatment | Extension | Medium |
| Add Suppression Priority Order | Extension | High |
| Run Production Tests 1-5 | Validation | Critical |

**Recommendation:** Implement corrections and extensions, run Tests 1-5, then re-evaluate confidence before canon promotion.