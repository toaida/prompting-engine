# ENGINE_V15_CONTINUITY_PERSISTENCE_SYSTEM.md

## V15 Core Module — Continuity Object Library + Outfit Repeat
### AREA: 03 (Continuity Persistence) | Status: READY FOR INTEGRATION

---

## PURPOSE

Recurring visual objects create the feeling of continuous life. The same bikini across summers. The pendant never removed. The tote bag with fraying straps. These objects function as life timestamps — evidence that this is a real person existing in real time, accumulating wear, returning to places.

---

## KEY CONCEPTS

**Personal Item Chronology**: 3-7 recurring objects per character across sessions

**Temporal Signatures**: Wear patterns that allow viewer to place object on timeline

**Diegetic Continuity**: Same object appearing in same physical world across sessions

---

## CONTINUITY_OBJECT_LIBRARY

### Category A: Apparel Repeat Items

**A1: STATEMENT BIKINI**
```
Description: Brand-specific bikini appearing across 2-4 summers
Continuity Markers:
  - Fade: vibrant → slightly faded → noticeably faded
  - Elastic: band stretched, straps slightly slack
  - Hardware: clasp dulled, underwire possibly warped
  - Tanning lines: strap marks intensifying across years
Wear Tier:
  T0: crisp vibrant no fade
  T1: minimal fade still supportive
  T2: elastic relaxed color mildly diminished
  T3: faded elastic clearly stretched wire possibly poking
Prompt: "same [brand_color] bikini from [year_1/year_2/year_3] beach photos,
        fade level [light/medium/heavy], elastic wear on [straps/band/underwire],
        tanning lines from previous summers visible"
Token: [CONT_BIKINI_YEAR_1-4]
```

**A2: SIGNATURE NECKLACE/PENDANT**
```
Description: Chain/pendant worn consistently, accumulates skin oils/scratches
Continuity Markers:
  - Metal oxidation: bright → dulled → green tarnish at connections
  - Chain links: subtle kinks from repeated wear
  - Clasp: slightly worn, easier to open than original
  - Skin contact: chain stained from lotion/sweat
Prompt: "[metal_type] [pendant_style] necklace worn daily for [years],
        patina accumulation, chain flexibility reduced,
        clasp slightly worn from repeated opening"
Token: [CONT_NECKLACE_WORN]
```

**A3: EMOTIONAL HOODIE**
```
Description: Favorite hoodie worn repeatedly, appears in informal sessions
Continuity Markers:
  - Pilling: fabric pills at cuffs/pockets/hem
  - Color degradation: particularly at elbows
  - Shape memory: molded slightly to body shape
  - Lint accumulation: around pocket and hem
  - Zipper: slider slightly stiff or teeth misaligned
Prompt: "[color] supremel-branded hoodie worn for 18+ months,
        fabric pilling at [cuffs/pockets/hem], color fade at stress points,
        shape molded to body, lint accumulation in pocket"
Token: [CONT_HOODIE_WORN]
```

**A4: ROTATIONAL TOTE BAG**
```
Description: Canvas/leather tote for shopping/daily/beach trips
Continuity Markers:
  - Handle wear: one handle more worn if single-hand bias
  - Body shape: loses structure, bottom stress, corners rub
  - Interior: liner with pen marks, lip gloss exploded, old receipts
  - Hardware: metal studs on bottom dulled/scratched
Prompt: "[material] canvas tote bag with [single_hand_bias/symmetric] handle wear,
        body slightly sagged, corner rub [mild/noticeable],
        interior contents [detail_level], bottom studs dulled"
Token: [CONT_TOTE_WORN]
```

**A5: SPECIFIC UNDERWEAR SET**
```
Description: Bra/panties visible at edges through sheer/low-back clothing
Continuity Markers:
  - Elastic degradation: band less supportive, straps widened
  - Color: slight migration/staining from daily wear
  - Fabric texture: lived-in rather than new crispness
  - Hook-and-eye: closure points worn
Prompt: "same bra/panties set visible at edges, slight elastic degradation,
        band less supportive, straps slightly widened,
        fabric texture lived-in not new"
Token: [CONT_UNDERWEAR_SET]
```

### Category B: Personal Possessions

**B1: PHONE CASE WITH DAMAGE**
```
Description: Phone case carried everywhere, impact damage accumulates
Continuity Markers:
  - Case corners: impact damage from drops
  - Screen protector: bubbles, edge scratches, yellowing
  - USB port: slight tilt from repeated plugging
  - Button areas: heavily worn smooth at volume/power
Prompt: "[brand_model] phone case with [corners_damaged/screen_bubbles],
        button areas smooth from wear, USB port misalignment,
        case clearly matched to [1-2+] year old phone purchase"
Token: [CONT_PHONE_CASE]
```

**B2: HOME SCATTER OBJECTS**
```
Description: Objects on bedroom shelf/desk/nightstand appearing in backgrounds
Types: half-empty perfume, protein powder, coral vase, worn paperback,
       medication blister pack, charging cable brand
Continuity: Appear inconsistently across sessions creating diegetic density
Prompt: "bedroom shelf scatter: [specific_object] visible in background,
        same object appears across multiple sessions inconsistent between shots"
Token: [CONT_SCATTER_OBJECT]
```

**B3: JEWELRY STACK**
```
Description: Rings/bracelets/anklets consistently stacked in same combinations
Continuity Markers:
  - Metal pairing: matching patina/oxidation levels
  - Sizing: rings slightly loose (worn for years)
  - Stack order: character's consistent pattern
Prompt: "[metal_combo] jewelry stack [number] pieces,
        matching patina across pieces, rings slightly loose,
        stack order [consistent/variable], [anklet_present/absent]"
Token: [CONT_JEWELRY_STACK]
```

**B4: REPEATED EYEGLASSES**
```
Description: Specific pair worn in daily-life shots, not just posed
Continuity Markers:
  - Nose pad: marks on bridge from daily wear
  - Temple tips: slightly bent from removal/placement
  - Lens: micro-scratches from cleaning
  - Case: possibly more worn than glasses
Prompt: "same eyeglasses worn consistently in daily shots,
        nose pad marks on bridge, temple tips slightly bent,
        lens micro-scratches visible, case worn"
Token: [CONT_EYEGLASSES]
```

### Category C: Environmental Continuity

**C1: SPECIFIC BEDDING SET**
```
Description: Same sheets/pillowcases/blanket in bedroom over months/years
Continuity Markers:
  - Wrinkle patterns: consistent placement creating baseline
  - Light staining: subtle pillowcase discoloration at mouth
  - Fabric softener: slightly built-up texture
  - Tear progression: small tear possibly visible in later sessions
Prompt: "same [color/material] bedding set appearing in bedroom portraits over months,
        consistent wrinkle placement, subtle skincare product staining on pillowcase,
        fabric softener buildup texture, [small_tear_progressing]"
Token: [CONT_BEDDING_SET]
```

**C2: ROOM SLIPPERS (拖鞋)**
```
Description: Indoor slippers worn at home, visible in floor-level shots
Continuity Markers:
  - Insole compression: permanent foot-shape depression
  - Outside sole: wear pattern from specific floor types
  - Material: slight separation at seam if daily wear
Prompt: "same indoor [material] slippers with foot-shape sole impression,
        wear pattern from walking on [specific_floor], [slight_separation_at_seam]"
Token: [CONT_ROOM_SLIPPERS]
```

**C3: SPECIFIC TOWEL/HAIR TOWEL**
```
Description: Same towel in bathroom selfies, post-shower shots
Continuity Markers:
  - Slight discoloration: rust-tint at hem from water exposure
  - Fabric softening: subsequent washes creating worn softness
  - Hanging wear: towel rod discoloration if consistent spot
Prompt: "same [color] towel appearing in bathroom selfies over months,
        rust-tint at hem, fabric softened from multiple washes,
        [towel_rod_discoloration_present]"
Token: [CONT_TOWEL]
```

### Category D: Situational Repeat Items

**D1: TRAVEL BAG**
```
Description: Specific bag for beach trips/weekend getaways
Continuity Markers:
  - Duffel crease: specific crease lines from folding
  - Interior: possibly old sunscreen, sand residue, not cleaned between trips
  - Strap wear: specific hand-carry pattern
Prompt: "same [style] travel bag appearing across [number] beach trips,
        duffel crease from storage, interior sand residue in corners,
        strap wear pattern, [water_bottle_moisture_damage]"
Token: [CONT_TRAVEL_BAG]
```

**D2: SPECIFIC BEACH TOWEL**
```
Description: Distinctive towel in beach/shore shots
Continuity Markers:
  - Sand staining: bottom of towel consistently shows sand
  - Bleaching: chlorine/salt fade on colorful towel
  - Fold memory: wants to fold certain ways
  - Fringe fray: edges progressively fraying
Prompt: "same [color] beach towel with sand staining at bottom,
        [chlorine/salt] bleaching creating inconsistent fade,
        fold memory visible, fringe [fraying_progression]"
Token: [CONT_BEACH_TOWEL]
```

**D3: WATER BOTTLE ROUTINE**
```
Description: Reusable bottle in fitness/street/home contexts
Continuity Markers:
  - Beverage residue: internal staining if unwashed
  - Cap wear: O-ring degrading, cap not threading smoothly
  - Dents/dings: if metal, accumulated impacts
  - Label state: scratched/peeling from extensive use
Prompt: "same [material] water bottle with [residue_staining/dents/label_peeling],
        cap O-ring [degrading/smooth], threads [catching/smooth]"
Token: [CONT_WATER_BOTTLE]
```

### Category E: Footwear Persistence

**E1: DAILY WEAR SNEAKERS**
```
Description: Sneakers for regular daily use, not special occasion
Continuity Markers:
  - Outsole wear: specific walk patterns in heel/toe
  - Upper creasing: horizontal creases at flex point
  - Tongue stain: lace grooves visible in padding
  - Collar deformation: ankle collar deformed from insertion
  - Insole: darkened from sweat absorption
Prompt: "same [brand/color] sneakers worn daily for [months],
        outsole [heel_toe_wear_pattern], upper creasing at flex points,
        tongue stain from lace pressure, collar deformed from ankle insertion,
        insole darkened from sweat"
Token: [CONT_SNEAKERS_DAILY]
```

**E2: BATHROOM SLIPPERS (Shower)**
```
Description: Rubber slippers worn in shower
Continuity Markers:
  - Bottom tread: possible mold in grooves if not dried
  - Sole flexibility: becoming more flexible from water cycles
  - Color fading: rubber degrading
Prompt: "same [color] rubber shower slippers with [mold_in_tread/sol_flexible],
        color [faded/consistent], [not_fully_dried_moisture]"
Token: [CONT_SHOWER_SLIPPERS]
```

---

## OBJECT-TIME MAPPING

### Tier System

```
TIER_0: NEW/FRESHLY ACQUIRED
  - Crisp, no wear, tags possibly visible
  - "first wear tag visible"

TIER_1: 3-6 MONTHS REGULAR USE
  - New-product feel gone, early wear visible
  - "3-6 months regular use, early wear markers"

TIER_2: 1 YEAR REGULAR USE
  - Full break-in, meaningful wear, character mold developing
  - "1 year of daily wear, meaningful wear visible"

TIER_3: 2+ YEARS REGULAR USE
  - Visible degradation, possibly seeking replacement
  - "2+ years heavy use, elastic degraded, fading visible"

TIER_4: VINTAGE/SENTIMENTAL
  - Old but maintained past normal replacement point
  - "vintage worn, maintained past replacement necessity"
```

### Moderation Profile

- Each character: 3-7 persistent items across categories
- No more than 2 items TIER_0 in use at once
- TIER_3+ items need narrative explanation (sentimental, financial constraint, loyalty)
- Correlated wear: objects worn together should age together

---

## OUTFIT-REPEAT SYSTEM

### Rotation Frequency Model

| Outfit Type | Repeat Cadence | Max Years | Wear Progression |
|-------------|----------------|-----------|------------------|
| Statement piece (bikini) | 2-4x per year | 3-4 | Slow |
| Daily wear (hoodie, tee) | 15-30x per year | Continuous | Fast (6mo) |
| Special occasion | 1x per year max | 5+ | None |
| Active/sports | 3-5x per month | 1-2 | Fast (sweat/salt) |

**Key**: "Times worn" to "times photographed" ratio should skew heavily toward times worn.

### Outfit-State Tracking

```
SAME OUTFIT (immediate): Worn within 48hrs, minimal laundering difference
SAME OUTFIT (contextual): Worn 2-4 weeks later, washed once, storage wrinkles
SAME ITEM DIFFERENT COMPLETION: Same top + different bottom/footwear
SAME ITEM WEAR PROGRESSION: Same bikini Year 2 vs Year 3 = visible age
```

### Prompt Grammar

```
SAME_ITEM_REPEAT:
[item_description] worn [frequency] wash_cycle [number]
wrinkle_storage_pattern [level] item_age [tier]

NEW_FROM_WARDROBE:
[item_description] first_wear tag_[visible/not_visible]
store_starch_[present/absent] size_label_[brand_size]

COMPLETE_OUTFIT_REPEAT:
[full_outfit_description] all_items_from_same_session_[date]
```

---

## TRAVEL CONTINUITY MODULE

### Travel Object Types

**Type 1: Packed-Luggage Items** (Identity Anchors)
- Same tote bag, water bottle, phone case in foreign context
- "carried_to_[destination]_from_[origin]"

**Type 2: Destination-Appropriate Items** (Location Markers)
- New purchases appearing only in travel context
- "acquired_at_[specific_location]_first_wear_[destination]"

**Type 3: Travel-Specific Items** (Departure/Arrival Signals)
- Passport, travel adapter, foreign currency
- Appear in departure shots, absent during domestic sessions

### Cross-Location Rules

1. No object in more than 2 dramatically different environment types without explanation
   - Exception: phone case, jewelry in ALL environments
2. Travel wear progression is compressed (1 week = 3-5 contexts)
3. Destination items accumulate wear independently

### Prompt Grammar

```
TRAVEL_OBJECT_PRESENT:
[item_description] carried_to_[destination]_from_[origin]
destination_context_[tourist/local/off-duty]

DESTINATION_PURCHASE:
[new_item] acquired_at_[specific_location]_first_wear_[destination]
return_wear_[origin_after_trip]

DEPARTURE_EVIDENCE:
passport_[character_name] travel_[destination] carry-on_items_[list]
```

---

## TOKEN LIBRARY

```
APPAREL:
[CONT_BIKINI_YEAR_1-4] [CONT_NECKLACE_WORN] [CONT_HOODIE_WORN]
[CONT_TOTE_WORN] [CONT_UNDERWEAR_SET]

PERSONAL:
[CONT_PHONE_CASE] [CONT_SCATTER_OBJECT] [CONT_JEWELRY_STACK] [CONT_EYEGLASSES]

ENVIRONMENTAL:
[CONT_BEDDING_SET] [CONT_ROOM_SLIPPERS] [CONT_TOWEL]

SITUATIONAL:
[CONT_TRAVEL_BAG] [CONT_BEACH_TOWEL] [CONT_WATER_BOTTLE]

FOOTWEAR:
[CONT_SNEAKERS_DAILY] [CONT_SHOWER_SLIPPERS]

TIERS:
[TIER_0_NEW] [TIER_1_6MONTHS] [TIER_2_1YEAR] [TIER_3_2YEAR+] [TIER_4_VINTAGE]

MODIFIERS:
[same_item_repeat] [new_from_wardrobe] [complete_outfit_repeat]
[wear_correlated] [destination_purchase] [departure_evidence]
```

---

*V15 Module: ENGINE_V15_CONTINUITY_PERSISTENCE_SYSTEM.md*
*Status: READY FOR INTEGRATION*
*Cross-ref: ENGINE_V15_EXPRESSION_TIMING_SYSTEM (residual expression markers)*
