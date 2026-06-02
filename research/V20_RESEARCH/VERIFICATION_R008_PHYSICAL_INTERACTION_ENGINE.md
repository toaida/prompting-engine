# Verification & Extension: R008_PHYSICAL_INTERACTION_ENGINE

## Verification Notes

**Strengths:**
- Correctly identifies root cause: AI treats objects as visual labels, not physical systems
- Taxonomy (PI-01 through PI-08) covers 90%+ of common HK lifestyle interaction scenarios
- Failure pattern table is actionable and production-ready
- Confidence rating (0.91) is reasonable but slightly inflated given known model limitations

**Critical Gaps Found:**

1. **Missing: FINGER_DENSITY_CONTRACT** — AI frequently renders 6+ fingers when hands grip objects. Must specify exact finger count and visible digits.

2. **Missing: PRESSURE_GRADIENT_CONTRACT** — Contact isn't binary (touching/not touching). Skin deforms, fabric wrinkles, objects indent. Current contracts lack pressure articulation.

3. **Missing: MULTI_LAYER_TRANSPARENCY_RULE** — Glass + reflection + objects behind + hand in front creates 4+ depth layers. Current contracts handle 2-3 layers but fail at 4+ (e.g., hand outside bus window, reflection of interior, passengers behind glass, street visible through).

4. **Missing: TEMPORAL_CONTACT_RULE** — Some interactions are momentary (hand reaching for strap) vs sustained (hand gripping strap). Posture, shadow, and fabric behavior differ.

5. **Overlooked: HANDLE_GRIP_CONTRACT fails when handle is horizontal** (MTR pole, suitcase handle, drawer pull). Current language assumes vertical handles.

6. **Overlooked: SURFACE_SUPPORT_CONTRACT ignores edge cases** — leaning on counter corner vs flat edge vs curved railing produce different compression patterns.

---

## Corrections

### Correction 1: PI-01 HANDLE_GRIP_CONTRACT — Add orientation parameter

**Current:**
`fingers wrap around the outside vertical handle`

**Corrected:**
`fingers wrap around the [vertical/horizontal/angled] handle; [for vertical: thumb visible on near side, four fingers curl behind; for horizontal: thumb wraps over top, fingers curl underneath]; palm does not touch the [glass/panel/surface]`

### Correction 2: PI-02 GLASS_BARRIER_CONTRACT — Add depth layer count

**Current:**
`glass is a solid transparent barrier between her hand and the objects behind it`

**Corrected:**
`glass is a solid transparent barrier; depth layers from front to back: [1] hand outside glass, [2] glass surface with faint reflection, [3] objects behind glass, [4] background wall; each layer maintains distinct focus and opacity; no layer merges with adjacent layer`

### Correction 3: Failure Pattern Table — Add finger count failure

| Failure | Why It Happens | Prevention Rule |
|---|---|---|
| 6+ fingers when gripping | model adds extra digits for "completeness" | specify "exactly five fingers visible, thumb on one side, four on other" |

---

## Extensions

### Extension 1: PI-09 FINGER_DENSITY_CONTRACT (NEW)

**Use when:** any hand grips, holds, wraps, or touches any object

**Prompt language:**
`right hand has exactly five fingers: thumb visible on near side of handle, four fingers curl around far side; no extra digits; fingernails visible on thumb and index finger only; knuckle creases align with grip direction`

**Prevents:** 6+ finger mutations, finger merging with object, missing thumb

### Extension 2: PI-10 PRESSURE_GRADIENT_CONTRACT (NEW)

**Use when:** body weight rests on surface, hand grips with tension, fabric compresses

**Prompt language:**
`[body part] applies [light/moderate/heavy] pressure on [surface]; skin indents [slightly/noticeably/deeply] at contact point; [fabric/flesh] wrinkles radiate from contact center; shadow density increases at pressure point; surface [does not deform / deforms slightly / shows compression marks]`

**Prevents:** weightless contact, floating limbs, unrealistic fabric behavior

### Extension 3: PI-11 TEMPORAL_CONTACT_CONTRACT (NEW)

**Use when:** interaction is dynamic (reaching, pulling, releasing, adjusting)

**Prompt language:**
`[body part] is in [moment of reaching / mid-grip / releasing / steady hold]; for reaching: fingers extended, not yet curled, gap between hand and object; for mid-grip: fingers partially curled, tension visible in forearm tendons; for releasing: fingers loosening, object beginning to separate from palm; for steady hold: fingers fully curled, no movement, weight settled`

**Prevents:** static-looking dynamic actions, impossible mid-air hand positions

### Extension 4: PI-12 MULTI_LAYER_TRANSPARENCY_RULE (NEW)

**Use when:** glass + reflection + objects behind + hand in front (bus window, shop display, mirror selfie with background)

**Prompt language:**
`depth layers from camera to background: [layer 1] hand/phone in foreground, sharp focus; [layer 2] glass surface with faint reflection of [foreground elements]; [layer 3] objects behind glass, softer focus; [layer 4] background beyond glass, most blurred; each layer has distinct opacity: layer 1 = 100%, layer 2 = 30-50% reflective, layer 3 = 60-80% visible, layer 4 = 20-40% visible; no layer bleeds into adjacent layer`

**Prevents:** impossible transparency, reflection merging with background, hand appearing inside glass

---

## Production Tests

### Test 1: Refrigerator Glass Door (Critical Path)
**Prompt:**
```
PHYSICAL INTERACTION: right hand wraps around exterior vertical fridge handle; exactly five fingers: thumb visible on near side, four fingers curl behind handle; glass remains continuous barrier between hand and drink shelves; depth layers: [1] hand in foreground, [2] glass with faint knuckle reflection, [3] drink cans behind glass, [4] kitchen wall behind; hand applies light pressure on handle, knuckle skin indents slightly at contact; hand is in steady hold, not reaching or releasing
```
**Check:** Hand does not penetrate glass. Exactly 5 fingers. Reflection visible but separate. Cans behind glass are softer focus.

### Test 2: MTR Strap with Reflection (Complex Transparency)
**Prompt:**
```
PHYSICAL INTERACTION: left hand grips overhead MTR strap; fingers curl through loop, thumb wraps over top; exactly five fingers visible; depth layers: [1] hand in foreground, [2] strap in front of wrist, [3] train window behind with street visible, [4] reflection of interior passengers on window surface; hand applies moderate pressure, tendons visible on forearm; hand is in steady hold, shoulder slightly lifted from tension
```
**Check:** Strap passes in front of wrist, not through. Window shows both street and reflection. Hand does not merge with strap.

### Test 3: Café Table Lean with Pressure Gradient
**Prompt:**
```
PHYSICAL INTERACTION: right forearm rests on café table edge; forearm applies moderate pressure, skin indents at table edge, fabric sleeve wrinkles radiate from contact point; contact shadow directly under forearm, darker at pressure point; iced milk tea glass sits beside wrist, not intersecting; phone lies flat on table plane, screen reflection matches table perspective
```
**Check:** Forearm shows compression. Shadow density varies. Glass and phone maintain separate planes.

### Test 4: Bag Zipper with Finger Density
**Prompt:**
```
PHYSICAL INTERACTION: left hand steadies crossbody bag body, right hand pinches zipper tab; right hand has exactly five fingers: thumb on top of tab, index and middle fingers underneath, ring and pinky curled away; zipper opening bends around pull direction; bag strap presses diagonally into shoulder fabric, fabric wrinkles at pressure line; inside contents partly occluded, not floating
```
**Check:** Exactly 5 fingers on zipper hand. Strap shows fabric compression. Contents stay inside bag.

### Test 5: Bus Window with Multi-Layer Transparency (Stress Test)
**Prompt:**
```
PHYSICAL INTERACTION: right hand rests on bus window sill; depth layers: [1] hand in foreground, sharp focus; [2] window glass with faint reflection of hand and interior seats; [3] street and buildings outside window, softer focus; [4] interior ceiling lights reflected on glass surface; hand applies light pressure, fingertips touch glass but do not pass through; reflection of hand appears on glass but is semi-transparent, does not occlude street completely
```
**Check:** 4 distinct layers. Hand does not pass through glass. Reflection is semi-transparent. Street visible through reflection.

---

## Confidence Adjustment

**Adjusted Confidence: 0.85 / 1.00** (down from 0.91)

**Reasons for reduction:**
1. Original confidence did not account for finger density failures (common in current models)
2. Multi-layer transparency remains difficult even with explicit depth layering
3. Pressure gradient articulation is unproven in production; may require tuning
4. Temporal contact contracts may conflict with static image generation (models prefer frozen moments)

**Mitigation:**
- Test 1-5 will validate or invalidate specific contract effectiveness
- If Tests 1-3 pass reliably, confidence returns to 0.91
- If Test 5 (multi-layer) fails, create R008.1 sub-engine for transparency specifically

**Recommendation:** Promote to CANON after Tests 1-3 pass with >80% success rate in 20 generations each. Hold Test 4-5 as experimental until validated.