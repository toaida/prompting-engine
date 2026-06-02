# R008_PHYSICAL_INTERACTION_ENGINE
### V20.1 — Research #008
### Status: PRODUCTION-GUIDED RESEARCH PHASE

---

## RESEARCH SOURCE
- **Trigger:** P004 generation showed hand passing through refrigerator glass.
- **Date:** 2026-06-02
- **Agent:** Lucy (Hermes)
- **Priority:** P1
- **Production Failure:** realism-breaking physical interaction between hand, glass door, and object boundary.

## RESEARCH GOAL
Develop prompt-level rules to enforce believable physical contact between hands, objects, doors, containers, barriers, furniture, and transportation environments. The engine must make physical relationships explicit: what is touched, what blocks movement, where contact happens, where shadows/reflections appear, and what cannot pass through what.

## CORE QUESTION
**How do we stop AI from treating glass, doors, containers, seats, handles, and furniture as decorative surfaces instead of physical barriers?**

---

# PART 1: FINDINGS — AI FAILS WHEN OBJECTS HAVE NO BOUNDARY ROLE

AI often understands objects as visual labels, not as physical systems. A refrigerator door becomes "glass texture" instead of a hinged barrier. A hand becomes "near fridge" instead of gripping a handle outside the glass. A train pole becomes "metal line" instead of a weight-bearing object.

Real photography gives physical relationships through:

1. **Contact point** — where skin/object/furniture meet.
2. **Barrier plane** — what surface separates inside/outside.
3. **Occlusion order** — what appears in front of what.
4. **Shadow / reflection evidence** — contact has optical consequences.
5. **Weight / resistance** — body posture changes because objects push back.
6. **Affordance** — hands use handles, straps, edges, buttons, seats, rails, lids.

If prompt only says "hand near refrigerator glass", the model may put the hand through the glass. If prompt says "fingertips wrap around the vertical handle outside the closed glass door; palm is reflected faintly on the glass; drink cans remain behind the barrier", the model gets a boundary map.

---

# PART 2: ENGINE PROPOSAL — PHYSICAL INTERACTION ENGINE

## Core Philosophy

Every object interaction must specify a **physical contract**:

```
ACTOR: which body part moves
TARGET: what exact object part is used
CONTACT: where touch occurs
BARRIER: what cannot be crossed
OCCLUSION: what is in front / behind
EVIDENCE: shadow, reflection, compression, grip, weight shift
```

## Runtime Activation

Activate when image includes:
- hand touching glass / mirror / window / fridge door
- hand holding object, bag, phone, drink, umbrella, rail
- opening door / cabinet / container / car door / MTR door
- sitting / leaning on furniture
- using transportation handles, poles, seats, turnstiles
- body near barriers: railings, counters, tables, doors, bus windows

## Boundary Contract Rule

Never write only:
`hand near glass`, `touching door`, `leaning on table`, `holding bag`

Always write:
`which surface, which side, exact contact point, physical effect, shadow/reflection/occlusion`

---

# PART 3: PHYSICAL INTERACTION TAXONOMY

## PI-01 HANDLE_GRIP_CONTRACT
Use when doors / fridge / drawers / cabinets / luggage handles are involved.

Prompt language:
`fingers wrap around the outside vertical handle, thumb visible on near side, palm does not touch the glass panel, handle casts a small contact shadow on her knuckles`

Prevents: hand through glass / hand glued flat to door / missing handle.

## PI-02 GLASS_BARRIER_CONTRACT
Use for fridge doors, shop windows, bus/MTR glass, mirrors.

Prompt language:
`glass is a solid transparent barrier between her hand and the objects behind it; her hand is outside the glass, drink shelves are behind the glass, faint reflection overlaps but skin does not pass through`

Prevents: impossible penetration, objects merging with hand.

## PI-03 SURFACE_SUPPORT_CONTRACT
Use for leaning on tables, counters, railings, sink edges.

Prompt language:
`forearm rests on the table edge with slight skin compression, wrist angle changes because the surface supports weight, contact shadow directly under arm`

Prevents: floating limbs / weightless lean.

## PI-04 SEAT_WEIGHT_CONTRACT
Use for sofa, chair, MTR seat, stair, curb, bed edge.

Prompt language:
`hips sink slightly into the cushion, shorts fabric creases where seated weight meets surface, thighs follow seat plane, feet grounded`

Prevents: hovering body / impossible sitting.

## PI-05 CONTAINER_OPENING_CONTRACT
Use for bags, wallets, bottles, food containers, drawers.

Prompt language:
`one hand holds the bag body steady while the other pulls the zipper tab; opening edge bends around the fingers, contents partly occluded inside`

Prevents: hand inside closed object / floating items.

## PI-06 TRANSPORT_CONTACT_CONTRACT
Use for MTR/bus/minibus/taxi/ferry environments.

Prompt language:
`right hand grips the overhead strap with visible finger curl, shoulder lifted slightly by arm tension, strap is in front of her wrist, background passengers blurred behind`

Prevents: disconnected hands / rail passing through palm.

## PI-07 DOOR_SWING_CONTRACT
Use for doors, car doors, fridge doors, shop doors.

Prompt language:
`door is partly open on hinge side, her hand pulls the handle from the outside edge, gap visible between door and frame, interior visible only through the opening`

Prevents: door plane inconsistency, hand on wrong side.

## PI-08 MIRROR_REFLECTION_CONTRACT
Use for mirror selfies and glass reflections.

Prompt language:
`phone and hand are in front of mirror, reflected phone appears inside mirror plane, physical phone edge occludes part of her cheek in the real foreground`

Prevents: duplicate impossible hands / wrong reflection order.

---

# PART 4: PROMPT CHANGES

## Add Interaction Contract Block

```
PHYSICAL INTERACTION:
actor = [right hand / left forearm / hip / shoulder / foot]
target = [outside vertical fridge handle / table edge / MTR strap / bag zipper]
contact = [fingers curl around / forearm rests on / hip sinks into]
barrier = [glass remains between hand and shelf / door blocks interior]
occlusion = [hand in front of handle, objects behind glass]
evidence = [contact shadow, faint reflection, fabric compression, weight shift]
```

## Positive Wording Beats Negatives

Bad:
`hand not passing through glass`

Better:
`fingers wrap around the exterior handle; glass panel remains continuous and unbroken between her hand and the drink shelves behind it`

## Interaction Grammar

```
body part → exact object part → contact verb → resistance / weight effect → optical evidence → barrier rule
```

Example:
`left forearm rests along the table edge, elbow slightly compressed by the surface, contact shadow under wrist, phone sits in front of her hand not merging with it`

---

# PART 5: EXPECTED PRODUCTION IMPACT

## Immediate Impact

- Fewer hand-through-glass failures.
- Better object-body plausibility in convenience stores, cafés, transit, bedrooms.
- More believable contact shadows and reflections.
- Reduced AI prop floating.
- Stronger realism in action scenes because body posture reacts to resistance.

## Runtime Impact

This engine adds precision, so it should only activate around physical interactions. It should not be pasted into every prompt. Use a compact contract when hands/body/object relationships matter.

## Realism Impact

Viewers may not consciously notice correct contact, but they immediately notice impossible contact. R008 is a failure-prevention engine: it protects believability.

---

# PART 6: PRODUCTION EXAMPLES

## Example A — Refrigerator Glass Door

```
PHYSICAL INTERACTION: right hand wraps around the exterior vertical fridge handle;
fingers curl around the handle outside the closed glass door, thumb visible on near side;
glass remains a continuous barrier between her hand and the drink shelves behind it;
faint reflection of her knuckles appears on the glass, but skin does not enter the fridge interior;
small contact shadow along handle, product labels softened behind glass.
```

## Example B — MTR Strap

```
PHYSICAL INTERACTION: left hand grips the overhead strap, fingers visibly curled through the loop;
shoulder lifts slightly from arm tension, wrist is in front of the strap, strap blocks part of palm;
body weight balanced over one hip, train interior behind her softened by motion blur.
```

## Example C — Café Table Lean

```
PHYSICAL INTERACTION: right forearm rests on the table edge with slight skin compression;
iced milk tea glass sits beside but not intersecting the wrist; contact shadow under forearm;
phone lies flat on table plane, screen reflection follows same perspective as table.
```

## Example D — Bag Zipper

```
PHYSICAL INTERACTION: left hand steadies the crossbody bag body, right fingers pinch the zipper tab;
zipper opening bends around the pull direction, bag strap presses diagonally into shoulder fabric;
inside contents remain partly occluded, not floating outside the bag.
```

---

# PART 7: COMMON FAILURE PATTERNS

| Failure | Why It Happens | Prevention Rule |
|---|---|---|
| Hand passes through fridge glass | glass not declared as barrier | specify exterior handle + continuous glass barrier |
| Hand floats near object | no contact verb | use curl, rest, pinch, press, pull, hook, support |
| Limb has no weight | no resistance / support | add compression, shoulder tension, hip sink, foot grounding |
| Object floats | no surface plane | specify object resting on table/floor/hand with shadow |
| Reflection duplicates wrong | mirror/glass plane unclear | separate real foreground vs reflected plane |
| Door geometry impossible | hinge/gap not defined | specify partly open, hinge side, frame gap |
| Rail/pole cuts through hand | occlusion order absent | say hand in front/behind, fingers wrap around pole |
| Bag/object merges with body | no strap/contact logic | strap presses into fabric; bag rests against hip |
| Interior/exterior confused | container not defined | declare inside/outside, opening edge, occlusion |
| Labels over-sharp behind glass | model over-renders contents | use softened labels behind reflection/barrier |

---

# PART 8: CROSS-REFERENCE

- V20 Object Logic V2 explains why the object exists; R008 explains how the object physically interacts.
- V20 Body Language Attraction explains why posture exists; R008 explains support/contact constraints.
- R007 Focus Hierarchy can be paired with `HAND_ACTION_LOCK` so the interaction is legible without making every product shelf sharp.
- R009 Local Life will need R008 for MTR straps, minibus seats, café tables, shop doors, Octopus gates, umbrellas, escalator rails.

---

# PART 9: CONFIDENCE RATING

**Confidence: 0.91 / 1.00**

Reason: the failure is specific and the corrective grammar is concrete. Object-boundary errors are common in image generation, but explicit contact/barrier/occlusion/evidence language usually improves results. Main uncertainty: complex glass reflections may still fail; production should test fridge, mirror, bus window, and shop-door cases separately.

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

## Lucy Consolidation Note
DeepSeek verification is preserved as appendix. Corrections and extensions remain research-stage until production images validate them.
