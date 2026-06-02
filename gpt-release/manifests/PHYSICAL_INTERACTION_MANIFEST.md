# PHYSICAL_INTERACTION_MANIFEST.md

## Purpose

Use this whenever the prompt includes hands, objects, glass, mirrors, doors, containers, furniture, seats, bags, straps, poles, railings, windows, vehicles, public transport, or any body part touching something.

The goal is to make physical contact believable. The image must clearly show what is being touched, which side of the object the hand or body is on, what blocks movement, what appears in front or behind, and what visual evidence proves contact.

This prevents common image-generation failures: hands passing through glass, fingers merging with handles, objects floating, rails cutting through palms, bodies hovering above seats, impossible mirror reflections, or bags and props merging with clothing.

## Prompt Instructions

Insert this into the prompt whenever physical contact matters:

```text
Make all physical interaction realistic and physically consistent. Clearly define the body part, exact object part, contact type, barrier, occlusion order, and contact evidence.

The interacting body part is [right hand / left hand / forearm / hip / shoulder / foot]. It contacts [exact object part: exterior vertical handle / table edge / bag zipper tab / MTR strap loop / glass door handle / chair seat]. The contact action is [gripping / resting / pinching / pressing / pulling / leaning / sitting / hooking].

Show contact evidence: finger curl, thumb placement, contact shadow, faint reflection, skin or fabric compression, weight shift, wrist angle, shoulder tension, seat compression, or object deformation.

If glass, mirror, window, or transparent material appears, keep depth layers separate: foreground hand or phone, glass surface reflection, objects behind glass, and distant background. The hand must stay on the correct side of the glass. Skin must not pass through glass or merge with objects behind it.

If a hand grips something, show exactly five fingers: thumb on one side, four fingers on the other side, no extra digits, no fused fingers, no missing thumb. Finger curl must match the object shape and handle direction.

If the body rests on furniture or a surface, show weight: compression, contact shadow, changed posture, grounded feet, fabric creases at the contact point.
```

### Fill-in Template

```text
Physical contact is realistic: actor = [body part]; target = [exact object part and orientation]; contact = [grip/rest/pinch/press/pull/sit/lean + finger count or weight effect]; barrier = [what cannot be crossed]; occlusion = [what is in front / behind]; evidence = [shadow/reflection/compression/tension/weight shift].
```

### Contact Checklist

For every interaction, specify:

1. Which body part is acting
2. Exact object part being touched
3. Contact verb: grip, rest, pinch, press, pull, hook, support, sit, lean
4. Side of the object: outside, inside, in front, behind, above, underneath
5. Barrier rule if glass, mirror, door, window, container, or vehicle is involved
6. Occlusion order: what appears in front and what appears behind
7. Evidence: shadow, reflection, compression, tension, deformation, weight shift
8. Finger count and thumb placement for hands

## Positive Examples

### Refrigerator Glass Door

```text
Realistic physical contact: her right hand wraps around the exterior vertical fridge handle. Exactly five fingers: thumb visible on the near side, four fingers curling behind the handle. The palm stays outside the closed glass door. The glass remains a continuous transparent barrier between her hand and the drink shelves behind it. Faint reflection of her knuckles appears on the glass surface. Drink cans and product labels behind glass are softer and separate from the hand. Small contact shadow along the handle. Skin does not enter the fridge interior.
```

### MTR Strap

```text
Realistic physical contact: her left hand grips the overhead MTR strap loop. Exactly five fingers visible: thumb wraps over the top, four fingers curl through the loop. Strap is in front of part of her wrist, not cutting through the palm. Shoulder lifts slightly from arm tension. Forearm tendons show a steady hold. Train window and passengers behind are softer and separate layers. No extra fingers, no fused strap, no floating hand.
```

### Café Table Lean

```text
Realistic physical contact: her right forearm rests on the café table edge with moderate pressure. Skin and sleeve compress slightly where the arm meets the table. Contact shadow directly under the forearm, darkest at the pressure point. Iced milk tea glass sits beside her wrist but does not intersect it. Phone lies flat on the table plane with perspective matching the tabletop. No floating objects, no merged wrist and glass.
```

### Bag Zipper

```text
Realistic physical contact: left hand steadies the crossbody bag body while right hand pinches the zipper tab. Right hand has exactly five fingers: thumb on top of the zipper tab, index and middle finger underneath, ring and pinky curled away naturally. The zipper opening bends in the pull direction. Bag strap presses diagonally into shoulder fabric, creating small fabric wrinkles. Contents remain partly hidden inside the bag, not floating outside.
```

### Mirror Selfie

```text
Realistic mirror geometry: physical phone and hand are in front of the mirror, partially blocking one side of her face in the real foreground. The reflected phone appears inside the mirror plane. Real foreground edge is sharper than the reflection. Reflected background stays behind her in the mirror, not mixed with the real hand. No duplicate impossible hand, no phone floating inside the face.
```

### Sitting on Sofa or MTR Seat

```text
Realistic seated weight: hips sink slightly into the seat cushion, thighs follow the seat plane, feet touch the floor. Shorts fabric creases where seated weight meets the surface. Contact shadow under thighs and along the seat edge. Body does not hover above the chair. Seat is supporting her weight.
```

## Negative Examples

Avoid prompts like these:

```text
Her hand is near the fridge glass, reaching through the door toward drinks.
```

Why it fails: the glass is not defined as a solid barrier, so the hand may pass through it.

```text
She touches the door with her hand.
```

Why it fails: no handle, side, contact point, finger placement, or door geometry is specified.

```text
She holds the MTR strap.
```

Why it fails: no finger curl, no thumb placement, no tension, no occlusion order; strap may cut through the hand.

```text
She leans on the table with a drink and phone nearby.
```

Why it fails: no pressure, shadow, surface plane, or object separation; objects may float or merge with the arm.

```text
Mirror selfie with phone in hand and reflection behind her.
```

Why it fails: real phone, reflected phone, foreground hand, and mirror plane are not separated.

```text
She sits on a chair, cute pose.
```

Why it fails: no seat compression, grounded feet, thigh contact, or fabric creases; the body may hover.

## Failure Prevention Rules

- Never write only `hand near glass`, `touching door`, `holding strap`, `leaning on table`, or `sitting on chair`. Always define exact contact.
- For glass, mirrors, windows, and transparent doors, clearly state which side the hand or phone is on.
- For glass barriers, separate depth layers: foreground hand, glass surface/reflection, objects behind glass, distant background.
- For grips, specify exactly five fingers, thumb placement, four-finger curl, and no extra digits.
- For handles, state orientation:
  - vertical handle: thumb on near side, four fingers behind
  - horizontal handle: thumb over top, fingers underneath
  - angled handle: wrist follows the handle direction
- For furniture contact, show weight: compression, creases, contact shadows, grounded feet, posture change.
- For leaning, show pressure and support. The surface should visibly affect the arm, wrist, shoulder, or torso angle.
- For containers and bags, define inside/outside. Contents should remain partly occluded inside, not floating outside.
- For doors, define hinge side, opening gap, frame, and whether the hand pulls from inside or outside.
- For mirrors, distinguish real foreground objects from reflected objects.
- For transport, straps and poles should have correct occlusion: fingers wrap around or through them; rails must not cut through palms.
- Contact should create evidence: shadow, reflection, skin compression, fabric wrinkle, object bend, shoulder tension, or weight shift.
- If contact evidence is missing, the interaction will look staged, floating, or physically impossible.
