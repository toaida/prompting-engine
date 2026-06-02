---
name: ENGINE_V20_PHYSICAL_INTERACTION_SYSTEM
description: Runtime system for physically believable hand/object/barrier/furniture/transport interaction.
areas: OBJECT PHYSICS / CONTACT / BARRIERS / OCCLUSION / REALISM
version: V20.1
status: PRODUCTION-GUIDED DRAFT — NOT CANON UNTIL VALIDATED
---

# ENGINE_V20_PHYSICAL_INTERACTION_SYSTEM

## Core Philosophy

Every physical interaction needs a contract: actor, target, contact, barrier, occlusion, and evidence. If the prompt does not define the physical relationship, the model may let hands pass through glass, rails cut through palms, objects float, or bodies hover above furniture.

## Activate When

- hand touches glass, mirror, window, fridge, door, cabinet
- body leans on table/counter/rail
- subject sits on sofa/chair/MTR seat/stair/curb
- hand grips MTR strap, pole, umbrella, bag, phone, drink
- object opens/closes: bag, zipper, bottle, drawer, door
- transport environment contains straps, poles, doors, windows, turnstiles

## Interaction Contract

```
ACTOR: body part
TARGET: exact object part
CONTACT: grip/rest/pinch/press/pull/hook/support
BARRIER: what cannot be crossed
OCCLUSION: what appears in front/behind
EVIDENCE: contact shadow, reflection, compression, weight shift
```

## Runtime Tokens

### PI-01 HANDLE_GRIP_CONTRACT
`fingers wrap around the outside vertical handle, thumb visible near side, palm does not touch glass panel, small contact shadow`

### PI-02 GLASS_BARRIER_CONTRACT
`glass remains a solid transparent barrier; hand outside, objects behind glass, faint reflection overlaps but skin does not pass through`

### PI-03 SURFACE_SUPPORT_CONTRACT
`forearm rests on table edge, slight skin compression, wrist angle changed by support, contact shadow underneath`

### PI-04 SEAT_WEIGHT_CONTRACT
`hips sink slightly into cushion/seat, fabric creases at contact, thighs follow seat plane, feet grounded`

### PI-05 CONTAINER_OPENING_CONTRACT
`one hand steadies container, other pulls zipper/lid/tab, opening bends around fingers, contents partly occluded inside`

### PI-06 TRANSPORT_CONTACT_CONTRACT
`hand grips strap/pole with visible finger curl, shoulder/wrist tension responds to support, correct front/behind occlusion`

### PI-07 DOOR_SWING_CONTRACT
`door partly open on hinge side, hand pulls exterior handle, gap visible between door and frame, interior visible only through opening`

### PI-08 MIRROR_REFLECTION_CONTRACT
`real phone/hand in front of mirror; reflected phone inside mirror plane; foreground phone occludes part of cheek`

### PI-09 FINGER_DENSITY_CONTRACT
`exactly five fingers: thumb on one side of object, four fingers curl on the other side; no extra digits; knuckle creases align with grip direction`

### PI-10 PRESSURE_GRADIENT_CONTRACT
`body part applies light/moderate/heavy pressure; skin/fabric compresses at contact point; shadow density increases at pressure center`

### PI-11 TEMPORAL_CONTACT_CONTRACT
`state the contact timing: reaching / mid-grip / steady hold / releasing; finger curl and body tension match the timing`

### PI-12 MULTI_LAYER_TRANSPARENCY_RULE
`depth layers are ordered: foreground hand/phone, glass surface reflection, objects behind glass, distant background; layers stay distinct and do not merge`

## Orientation Rule

For handles, always state orientation:
- vertical handle: thumb on near side, four fingers behind
- horizontal handle: thumb wraps over top, fingers curl underneath
- angled handle: wrist angle follows handle direction

## Prompt Grammar

```
PHYSICAL INTERACTION: actor = [body part]; target = [exact object part + orientation]; contact = [verb + finger count + timing];
barrier = [what cannot be crossed]; occlusion = [front/behind order]; evidence = [shadow/reflection/compression].
```

## Production Fragment — Fridge Door

```
PHYSICAL INTERACTION: right hand wraps around the exterior vertical fridge handle;
fingers curl around the handle outside the closed glass door, thumb visible on near side;
glass remains a continuous barrier between her hand and drink shelves behind it;
faint reflection of knuckles appears on glass, skin does not enter fridge interior;
small contact shadow along handle, product labels softened behind glass.
```

## Anti-Patterns

- `hand near glass` without barrier role
- `touching door` without handle/contact point
- seated pose without seat compression / foot grounding
- rail/pole without finger curl and occlusion order
- mirror selfie without real vs reflected plane distinction
- object opening without inside/outside logic

## Production Validation Needed

Test fridge glass, MTR strap, café table lean, bag zipper, mirror selfie, taxi/bus window separately. Promote to canon only after interaction failures visibly decrease.
