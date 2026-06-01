---
name: ENGINE_V20_OBJECT_LOGIC_V2_SYSTEM
description: Runtime system for everyday objects as lived-in evidence, not AI props.
areas: OBJECTS / ENVIRONMENT / STAGED AUTHENTICITY
version: V20
status: ACTIVE — AUTO-MERGED
---

# ENGINE_V20_OBJECT_LOGIC_V2_SYSTEM

## Core Philosophy

Objects should explain life, not decorate the image.

```
Bad AI: objects are clean, centered, unrelated props.
Good V20: objects have timing, owner, wear, lighting, and narrative reason.
```

Every object must answer:

```
Whose object is it?
Was it just used, being used, or forgotten?
Why is it physically there?
Does it share the scene lighting and shadow logic?
```

---

## Object Reason Hierarchy

1. `ACTIVITY_EVIDENCE` — object proves what is happening now.
2. `PERSONAL_BELONGING` — object belongs to her and marks presence.
3. `ENVIRONMENTAL_DEFAULT` — object naturally belongs in the space.
4. `SYMBOLIC_OBJECT` — works only with in-world justification.
5. `ENVIRONMENTAL_DECOR` — weakest; never primary reason.

---

## Object Timing States

| Token | Meaning | Example |
|---|---|---|
| `IN_USE` | actively handled | phone in hand, drink lifted |
| `JUST_USED` | residue of recent action | cup condensation, screen still lit indoors |
| `ABOUT_TO_USE` | hand/body moving toward it | fingers reaching for Octopus card |
| `BEEN_THERE` | settled into scene | bag beside chair, jacket draped |
| `FORGOTTEN` | out of place, uncured | phone on towel corner |
| `ABANDONED` | left behind accidentally | umbrella on MTR seat |
| `BORROWED` | social object | friend's jacket, charger, drink |
| `MULTI_USE` | object repurposed | bag as pillow, phone as mirror |

---

## Object Density Rule

Object count depends on shot type and environment.

- Close-up: 0-2 objects is fine.
- Social medium shot: 3-6 objects is natural.
- HK cafe/MTR/market: 4-8 objects can be normal.
- Beach minimalist shot: 2-4 objects max.
- Market/wet market: high density expected.

Only count **visible non-environmental objects**. Walls, rails, tables, lamps are environmental defaults.

---

## Object Interaction Roles

| Token | Meaning | Prompt Use |
|---|---|---|
| `OBJECT_AS_SHIELD` | phone/bag guards torso | shy, crowded, defensive |
| `OBJECT_AS_EXTENSION` | object used to gesture | pointing with phone, swinging bag |
| `OBJECT_AS_BARRIER` | object creates distance | drink between subject and camera |
| `OBJECT_AS_INVITATION` | subject shares object | showing screen, offering drink |
| `OBJECT_AS_TIME_MARKER` | object signals day rhythm | coffee morning, milk tea afternoon, cocktail night |
| `STAGED_AUTH_OBJECT` | deliberately casual KOL object | frame-edge cup, branded bag, curated clutter |

---

## HK Object Library

### Transit
- Octopus card, MTR Mobile screen, crossbody bag, earbuds, mask in pocket, water bottle, folded umbrella.

### Cafe / Cha Chaan Teng
- iced milk tea metal cup/glass, receipt, tissue packet, plastic menu, napkin dispenser, phone, friend's drink.

### Street / Market
- red-white-blue bag, Mannings/Wellcome/ParknShop bag, egg waffle paper bag, fish-ball stick, coin purse, umbrella.

### Home / Apartment
- rice cooker, kettle, floor fan, drying rack, slippers at entrance, skincare bottle, laptop with stickers, power bank.

### Night
- phone screen, cigarette/lighter if appropriate, convenience-store drink, cocktail, taxi receipt, umbrella with rain droplets.

---

## Lighting / Shadow / Reflection Checks

Objects must obey the same physics as subject.

- Same color temperature as nearby subject surface.
- Shadow direction matches key light.
- Reflective surfaces show plausible reflection.
- Hot drinks show steam when environment supports it.
- Cold drinks show condensation in HK humidity.
- Phone screen visible only in low-light / indoor / shade.

---

## Staged Authenticity Rule

KOLs stage objects to look candid. This is not failure. It is a production technique.

Good staged authenticity:
```
phone + iced milk tea + receipt + tissue packet casually clustered on formica table,
not centered, one item cropped by frame edge, condensation and tiny spill visible
```

Bad staged authenticity:
```
perfect branded coffee cup centered beside perfect phone and perfect bag, all equally lit
```

---

## Anti-Patterns

- `PROP_PARADE`: too many objects without hierarchy.
- `PERFECT_OBJECTS`: new, clean, centered, untouched.
- `OBJECT_LIGHTING_MISMATCH`: object lit differently from subject.
- `OBJECT_SHADOW_FAIL`: no contact shadow or wrong direction.
- `WRONG_OBJECT_CONTEXT`: snow boots on HK beach, handbag on MTR floor in rush hour without reason.
- `BRIGHT_FRAME_EDGE_DISTRACTION`: cropped object steals attention.
- `NO_OBJECT_HISTORY`: no wear, no use, no residue.

---

## Production Example

```
cha chaan teng friend-shot, OBJECT_LOGIC_V2: iced milk tea glass in use with condensation,
phone face-down as politeness signal, receipt and tissue packet at table edge, friend's drink partly cropped,
all objects sharing warm fluorescent cafe light and small contact shadows, not prop-styled
```
