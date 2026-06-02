# R007_FOCUS_HIERARCHY_ENGINE
### V20.1 — Research #007
### Status: PRODUCTION-GUIDED RESEARCH PHASE

---

## RESEARCH SOURCE
- **Trigger:** V20 real-world production testing revealed recurring HDR / globally sharp / micro-detail-heavy outputs.
- **Date:** 2026-06-02
- **Agent:** Lucy (Hermes)
- **Priority:** P1
- **Production Failure:** background competes with subject; environment becomes equally sharp and equally important.

## RESEARCH GOAL
Study how Japanese gravure photobooks, lifestyle photobooks, and casual social photography make the subject visually dominant without making the environment empty. The goal is not "blur everything". The goal is controlled visual competition: the world remains believable, but only one or two elements are allowed to carry priority.

## CORE QUESTION
**How do we make lil.troublr feel like the clear emotional subject of the image while keeping Hong Kong life visible but not visually noisy?**

---

# PART 1: FINDINGS — THE REAL FAILURE IS EQUAL IMPORTANCE

AI often treats every noun as a render target. If the prompt says "wet pavement, signs, shop lights, tiles, posters, passersby, bag, drink, hair, face", the model makes all of them equally crisp and saturated. That produces a technically impressive but emotionally flat image.

Real photobooks avoid this through hierarchy:

1. **Primary anchor** — usually face, eyes, hand-action, or silhouette.
2. **Secondary story cue** — object, gesture, or one local environmental signifier.
3. **Atmospheric field** — softened, darker, lower-contrast environmental support.
4. **Dead zones** — areas intentionally allowed to be boring, dark, blown, cropped, or soft.

Japanese gravure and lifestyle photobook logic often works because the environment is not absent; it is demoted. Rooms, beaches, streets, vending machines, cafés, and train platforms exist as emotional texture, not equal actors.

## Key Observations

- **Subject contrast is relational.** The subject does not need extreme sharpness; she only needs to be sharper / warmer / more emotionally readable than the rest.
- **Background detail should be legible in clusters, not everywhere.** One menu board can be readable-ish; twenty signs should dissolve into texture.
- **Skin and face usually carry the cleanest tonal transition.** The background can be harsher, grainier, cooler, or flatter.
- **Photobook images often use low global contrast but high local emotional contrast.** The photo feels soft, but the expression still lands.
- **Foreground obstruction helps hierarchy.** Door frames, curtain edges, glass reflection, chair backs, or phone blur can reduce environmental competition.
- **Over-sharp clothing texture can steal attention from face.** Fabric folds should explain posture, not become the hero.
- **HDR is the enemy of memory.** Memory photos contain underexposed corners, blown windows, flattened backgrounds, and missing information.

---

# PART 2: ENGINE PROPOSAL — FOCUS HIERARCHY ENGINE

## Core Philosophy

Every prompt must declare a **focus budget**. The image is allowed one primary focus, one secondary support, and the rest becomes atmosphere.

```
PRIMARY FOCUS: what the viewer must read first
SECONDARY SUPPORT: what explains why the photo exists
ATMOSPHERE: what confirms place / mood without competing
SUPPRESSION: what must be soft, dark, blown, cropped, or low-detail
```

## Runtime Activation

Activate when:
- image looks HDR / globally sharp
- background competes with face
- too many HK details become equal priority
- fashion texture becomes more important than expression
- production prompt contains 5+ environment nouns
- generated image feels like a location showcase instead of a person moment

## Focus Budget Rule

```
1 sharp emotional anchor
+ 1 readable story cue
+ 2-4 low-contrast local atmosphere cues
+ explicit suppression of everything else
```

Do not ask for "ultra-detailed" globally. Attach detail only to the anchor:

- good: `her face and near hand are the clearest emotional focus`
- bad: `ultra-detailed skin, fabric, city background, signs, pavement, storefronts`

---

# PART 3: HIERARCHY TAXONOMY

## FH-01 FACE_LOCK
Face / eyes / expression are the only crisp emotional destination.

Prompt language:
`face is the only fully resolved focus plane, eyes and mouth carry the emotional read, background falls into lower-contrast street texture`

Use for: café, bedroom, mirror, friend-shot, waiting moments.

Failure prevented: background signs and objects stealing attention.

## FH-02 HAND_ACTION_LOCK
Hand-object interaction leads attention, then face confirms emotion.

Prompt language:
`near hand and object contact are sharp enough to explain the action, face remains the emotional destination, surrounding objects softened`

Use for: phone, drink, fridge door, umbrella, bag, transit handles.

Failure prevented: object floats or interaction unreadable.

## FH-03 SILHOUETTE_LOCK
Body outline / posture is the read, not fabric micro-detail.

Prompt language:
`overall silhouette and weight shift are readable, fabric texture is secondary and not over-rendered`

Use for: walking, stair landing, MTR platform, rooftop, street crossing.

Failure prevented: clothing folds become noisy hero texture.

## FH-04 LOCAL_CUE_LOCK
One local cue establishes Hong Kong; all other local cues become atmosphere.

Prompt language:
`one Traditional Chinese shop sign is the main location cue, other signs dissolve into soft colored blocks`

Use for: dai pai dong, cha chaan teng, MTR exit, wet street, minibus stop.

Failure prevented: image becomes tourist/location content.

## FH-05 MEMORY_SOFT_FIELD
The whole photo is soft-memory coded, but emotional anchor remains legible.

Prompt language:
`soft photobook focus, low global contrast, only her expression and hand gesture slightly cleaner than the room`

Use for: photobook, morning room, low-stakes domestic scenes.

Failure prevented: AI studio crispness.

## FH-06 BACKGROUND_SUPPRESSION
Explicitly tells the model what not to resolve.

Prompt language:
`background is not a showcase: no readable poster wall, no crisp shelf items, no HDR storefronts, no equal-detail passersby`

Use whenever prompt includes rich environments.

---

# PART 4: PROMPT CHANGES

## Add Focus Budget Block

```
FOCUS HIERARCHY:
primary focus = [face / hand-action / silhouette]
secondary cue = [one object or local signifier]
atmosphere = [soft HK texture, low contrast, partial blur]
suppression = [no HDR background, no equal sharpness, no over-detailed objects]
```

## Replace Global Detail Language

Bad:
`ultra-detailed, sharp, high resolution, detailed city background, detailed fabric, detailed skin`

Better:
`selective detail only on her face and near hand, background lower contrast, distant signs softened, fabric folds readable but not micro-detailed`

## Depth-of-Field / Tonal Language

Use:
- `face plane slightly sharper than environment`
- `background texture readable as mood, not information`
- `one-stop darker background`
- `soft edge falloff around frame`
- `foreground blur partially covers lower corner`
- `window highlight slightly blown`
- `street signs softened into color blocks`
- `no HDR recovery in shadows`

## Negative Prompt / Prevention Language

- `not globally sharp`
- `no HDR clarity`
- `no equal-detail background`
- `no over-rendered fabric texture`
- `no crisp poster wall`
- `no landmark showcase`
- `no subject competing with ten bright objects`

---

# PART 5: EXPECTED PRODUCTION IMPACT

## Immediate Impact

- Fewer images where the background overpowers the subject.
- Less HDR / hyperreal digital crispness.
- Stronger first-glance subject recognition.
- More photobook-like softness without losing realism.
- Better HK locality because local cues become believable atmosphere instead of tourist inventory.

## Prompt Runtime Impact

This engine should reduce prompt bloat by forcing selection. Instead of listing every detail, prompt writer chooses:

- one focus anchor
- one story cue
- a small cluster of atmosphere
- explicit suppression

## Retention Impact

Viewer remembers:
- her expression
- her action
- the local mood

Viewer should not remember:
- every poster
- every object on a shelf
- every brick / tile / sign

---

# PART 6: PRODUCTION EXAMPLES

## Example A — Cha Chaan Teng Face Lock

```
FOCUS HIERARCHY: primary focus = her half-laughing face as she looks down at a message;
secondary cue = iced milk tea glass with condensation near her hand;
atmosphere = formica table edge, soft Traditional Chinese menu blur, warm fluorescent cafe color;
suppression = background diners and wall posters low contrast, no HDR clarity, no crisp menu wall.
```

## Example B — Fridge Hand Interaction

```
FOCUS HIERARCHY: primary focus = near hand gripping the refrigerator handle and her face reflected faintly in glass;
secondary cue = chilled drink shelf behind glass, softened by reflection;
atmosphere = convenience-store fluorescent spill and narrow aisle compression;
suppression = no sharp product labels, no fully detailed fridge interior, no equal-focus shelves.
```

## Example C — Wet Street Local Cue

```
FOCUS HIERARCHY: primary focus = her face turning back mid-step;
secondary cue = red taxi reflection under her shoes;
atmosphere = softened Traditional Chinese signs, wet pavement glow, umbrella edge blur;
suppression = signs not readable, storefronts not HDR, passersby not sharp.
```

---

# PART 7: FAILURE CASES

| Failure | Why It Happens | Prevention Rule |
|---|---|---|
| HDR city background | prompt asks for too many detailed environment cues | declare background lower contrast and non-showcase |
| Fabric steals attention | "detailed fabric folds" overused | make folds readable only where posture needs explanation |
| Face loses priority | bright signs / windows compete | one-stop darker background or blown window suppression |
| HK becomes touristy | too many landmarks / signs | one local cue only; others atmosphere |
| Photobook becomes blurry mess | soft focus applied globally without anchor | keep face or hand-action slightly clearer |
| Object clutter | too many props with equal importance | one secondary cue; remove rest or demote |
| Over-polished beauty shot | no dead zones | add dark corner, cropped foreground, soft background |
| AI micro-detail | model resolves every noun | use `not globally sharp`, `no HDR clarity`, `selective detail only` |

---

# PART 8: CROSS-REFERENCE

- V20 Attention Routing decides **why the viewer cares**.
- R007 Focus Hierarchy decides **what is allowed to visually compete**.
- V19 Visual Priority overlaps, but R007 is more production-specific: it targets HDR/global-sharp failures.
- R008 Physical Interaction benefits from `HAND_ACTION_LOCK` because interaction must be legible but not over-rendered.
- R009 Local Life benefits from `LOCAL_CUE_LOCK` because HK locality should feel lived-in, not destination-driven.

---

# PART 9: CONFIDENCE RATING

**Confidence: 0.86 / 1.00**

Reason: the failure mode is clear and prompt-level fixes are straightforward. Main uncertainty: some image models ignore negative suppression language; production testing must confirm whether positive hierarchy language (`primary focus`, `secondary cue`, `background lower contrast`) works better than negatives.

## RESEARCH STATUS
- ✅ Findings complete
- ✅ Engine proposal complete
- ✅ Prompt changes complete
- ✅ Expected production impact complete
- ✅ Failure cases complete
- ✅ DeepSeek V4 Pro verification + extension appended
- ⏳ Pending production validation before canon promotion


---

# PART 10: DEEPSEEK V4 PRO VERIFICATION & EXTENSION
### Consolidation Date: 2026-06-02

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

## Lucy Consolidation Note
DeepSeek verification is preserved as appendix. Corrections and extensions remain research-stage until production images validate them.
