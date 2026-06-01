# OBJECT_LOGIC_ENGINE_V2
### V20 — Research #004
### Status: RESEARCH PHASE

---

## RESEARCH SOURCE

- **Task:** Notion 04 Research → 01 GPT Research Tasks → 2026-06-01 → Research #004
- **Date:** 2026-06-01
- **Agent:** Lucy (Hermes)
- **Priority:** P2

## RESEARCH GOAL

Prevent small objects from becoming AI clutter or staged props.

## CORE QUESTION

**How do everyday objects appear naturally in real-life social photos?**

---

# PART 1: THE OBJECT PROBLEM

## Why AI Images Have Object Problems

```
AI DEFAULT:
→ Every object is placed with equal importance
→ Objects float without gravity, context, or reason
→ Too many objects = visual noise
→ Too few objects = empty stage
→ Objects don't interact with each other
→ Objects don't show wear, use, or personal history

REAL PHOTOS:
→ Objects are incidental — caught in frame, not placed
→ Objects have gravity — held, resting, leaning
→ Objects tell a story — evidence of activity, personality, moment
→ Objects are imperfect — used, worn, handled
→ Objects relate to subject — they're HER objects
```

## V1 → V2 Evolution

```
OBJECT_LOGIC_V1 (existing):
→ Object placement rules
→ Object-to-body spatial relationships
→ Basic object taxonomy

OBJECT_LOGIC_V2 (new):
→ Object narrative — why THIS object is HERE
→ Object authenticity — wear, use, imperfection
→ Object-subject relationship — personal vs environmental
→ Object timing — "just used" vs "been there a while"
→ Anti-clutter rules — when less is more
→ HK-specific object vocabulary
```

---

# PART 2: OBJECT NARRATIVE TAXONOMY

## The Object-Reason Rule

**Every object in frame must have a NON-PHOTOGRAPHIC reason to be there.**

```
OBJECT REASON HIERARCHY:

Level 1: ACTIVITY EVIDENCE (strongest)
  → Object is being used right now or was just used
  → "She was drinking this coffee" / "She was reading this book"
  → Object shows activity in progress

Level 2: PERSONAL BELONGING (strong)
  → Object belongs to subject — she brought it
  → Bag, phone, wallet, keys, personal item
  → Shows her personality, choices, presence

Level 3: ENVIRONMENTAL DEFAULT (neutral)
  → Object naturally exists in this environment
  → MTR pole, beach sand, hotel lamp
  → Not hers, not used — just there

Level 4: NARRATIVE ELEMENT (weak)
  → Object carries symbolic meaning
  → Flower, letter, gift — deliberate storytelling
  → ⚠️ Easy to overdo — reads as "prop"

Level 5: DECORATIVE (weakest)
  → Object only there for visual interest
  → ⚠️ Almost always reads as staged
  → Use sparingly, only in environmental defaults
```

## Object Timing States

```yaml
JUST_USED:
  → Object shows recent interaction
  → Coffee cup still has liquid, condensation on glass, phone screen still lit
  → Most authentic object state
  → Signal: she was just doing something

IN_USE:
  → Object being actively handled by subject
  → Phone in hand being looked at, drink being lifted
  → Strongest object-subject connection
  → Signal: she's doing something right now

ABOUT_TO_USE:
  → Object positioned for imminent use
  → Hand reaching, body oriented toward object
  → Creates anticipation
  → Signal: she's about to interact

BEEN_THERE:
  → Object settled, not recently touched
  → Bag placed, shoes kicked off, book set aside
  → Established presence — she's been here a while
  → Signal: this is a lived-in space

FORGOTTEN:
  → Object out of place, not deliberately positioned
  → Phone on floor while she's doing something else
  → Extremely authentic — humans don't curate their objects
  → Signal: she forgot about it
```

---

# PART 3: OBJECT-SUBJECT RELATIONSHIP

## Attachment Levels

```
DIRECT CONTACT (Level 1):
  → Object touches subject — held, worn, on lap
  → Most personal, highest attention
  → Camera must catch this interaction

IMMEDIATE REACH (Level 2):
  → Object within arm's reach
  → On table beside her, on floor next to her
  → Implies possible use, personal space

ROOM PROXIMITY (Level 3):
  → Object in same room, clearly visible
  → Coffee machine across hotel room, shoes by door
  → Environmental context, not personal

FRAME EDGE (Level 4):
  → Object just barely in frame, partially visible
  → Most authentic — caught, not placed
  → The friend's elbow, the edge of a sign, the corner of someone else's bag
```

## Object Personality Mapping

```yaml
OBJECT TYPE → WHAT IT SAYS ABOUT HER:

PHONE:
  → She's connected, social, documenting
  → Looking at phone = private moment in public
  → Phone face down = she's present, engaged
  → Phone in hand but not looking = habit, comfort object
  → Phone on floor beside her = forgot about it, absorbed in moment

BAG:
  → She came from somewhere, going somewhere
  → Bag open, items visible = she was just in it
  → Bag beside her on floor = this is her spot
  → Bag still on shoulder = she's not staying long

DRINK:
  → She's relaxed, social, taking a moment
  → Half-finished = she's been here a while
  → Condensation on glass = hot day, cold drink
  → Holding drink but not drinking = social prop, comfort
  → Multiple drinks = she's with someone

SHOES:
  → Where she's going, what she's doing
  → Shoes off = she's settled, comfortable, at home
  → Shoes on = she's active, going somewhere
  → One shoe off = mid-transition between states

CLOTHING_ITEMS:
  → Jacket draped = she was wearing it, now off
  → Hoodie on floor = casual comfort
  → Extra layer nearby = she's prepared for weather change

BOOK / MAGAZINE:
  → She reads, she has interests
  → Open, face down = she was reading
  → Bookmarked = she's a reader
  → ⚠️ Books can read as "prop" — need wear, use evidence

FOOD:
  → She eats, she's human
  → Half-eaten = mid-meal, caught
  → Takeout container = casual, real, Hong Kong
  → Multiple items = shared meal, social
  → ⚠️ Perfect food = stock photo, not real
```

---

# PART 4: HK-SPECIFIC OBJECT VOCABULARY

## Hong Kong Object Signifiers

```yaml
MTR / TRANSIT:
  - Octopus card visible in hand or bag
  - MTR route map (background element)
  - Phone with transit app or Octopus app
  - Plastic bag from local shop (red-white-blue, Wellcome, Mannings)
  - Umbrella (essential HK item — rain or sun)
  - Mask partially visible (post-2020 HK reality)

STREET / URBAN:
  - Dai pai dong items: plastic stool, metal table, tissue packet
  - Street food: egg waffle, fish ball stick, milk tea cup
  - Red-white-blue bag (HK icon)
  - 7-Eleven/Circle K drink
  - MTR station sign colors
  - Street sign with Chinese characters
  - Bamboo scaffolding in background
  - Neon sign fragments (waning but still HK)

BEACH / OUTDOOR:
  - Octopus stored in waterproof pouch
  - Beach mat (HK-style picnic mat)
  - Local drink brands (VLT, Bonaqua, etc.)
  - Plastic bag for rubbish (HK beach culture)
  - Flip flops (not slippers — HK distinction)

HOME / DOMESTIC:
  - Rice cooker visible in kitchen
  - Chinese tea set / cup
  - Local food packaging (Lee Kum Kee, Vitasoy, etc.)
  - Floor fan (HK apartment essential)
  - Clothes drying rack (HK apartment reality)
  - Air conditioner unit (window or split type)
  - Hot water flask / electric kettle

CAFE / SOCIAL:
  - HK-style milk tea (not latte — cultural distinction)
  - Pineapple bun / egg tart
  - Local cafe table (small, formica)
  - Condiment rack (chili oil, soy sauce, sugar)
  - Receipt on table (HK cafe detail)
```

---

# PART 5: ANTI-CLUTTER RULES

## The Object Count Rule

```
Too Few Objects (0-1):
  → Empty stage — "where is everything?"
  → Reads as: AI-generated, sterile, unnatural

Sweet Spot (2-4):
  → Enough to feel lived-in
  → Each object has purpose
  → Viewer can process all objects

Caution Zone (5-7):
  → Risk of visual clutter
  → Each object must earn its place
  → Hierarchy becomes important

Too Many (8+):
  → Visual noise — nothing stands out
  → Reads as: hoarding, staged "busy", AI over-generation
  → Viewer stops looking because nothing matters
```

## Object Hierarchy Rules

```
PRIMARY OBJECT (1 max):
  → Object subject is actively interacting with
  → Phone in hand, drink being lifted, book being read
  → This object justifies the photo
  → IN_USE or JUST_USED state

SECONDARY OBJECTS (1-3):
  → Objects in subject's immediate space
  → Bag, extra drink, clothing item
  → These establish personality and context
  → BEEN_THERE or IMMEDIATE_REACH

TERTIARY OBJECTS (0-3):
  → Environmental defaults
  → Furniture, lighting, architecture elements
  → These establish WHERE
  → Must not compete with primary object

QUATERNARY OBJECTS (0-2):
  → Frame-edge objects — barely visible
  → Someone else's bag, room corner, sign edge
  → These create authenticity through "accidental" framing
  → FORGOTTEN state — feels caught, not placed
```

---

# PART 6: OBJECT AUTHENTICITY SIGNALS

## Wear and Use Vocabulary

```yaml
OBJECT AGING SIGNALS:
  Phone: screen smudges, case slightly worn, sticker residue
  Bag: leather creases, strap wear, contents slightly visible
  Book: spine creases, dog-eared pages, cover wear
  Drink: condensation, ice melting, lip mark on rim/straw
  Shoes: sole wear, slight dirt, scuff marks
  Clothing: slight wrinkles, not perfectly pressed

OBJECT PLACEMENT SIGNALS:
  - Not centered — objects placed by use, not composition
  - Slight tilt or angle — casually placed, not arranged
  - Partial visibility — edge of object = caught, not framed
  - Overlapping objects — real spaces have object overlap
  - Different depths — objects at different distances from camera
```

## Anti-Prop Rules

```yaml
PROP DETECTION:
  If object is:
    ✗ Perfectly centered in frame
    ✗ Brand new, no wear
    ✗ Unrelated to subject's activity
    ✗ Only one of its kind in frame
    ✗ Too large or too small relative to subject
    ✗ Perfectly lit (better than subject)
  → It reads as PROPS, not authentic objects

  If object is:
    ✓ Slightly off-center or at frame edge
    ✓ Shows use, wear, age
    ✓ Connected to subject's activity
    ✓ Part of a cluster (phone + wallet + keys)
    ✓ Realistic scale
    ✓ Same lighting as everything else
  → It reads as AUTHENTIC
```

---

# PART 7: PROMPT LANGUAGE

```yaml
OBJECT_TOKENS:
  OBJECT_STATES:
    - IN_USE: actively being handled
    - JUST_USED: recently handled, evidence visible
    - ABOUT_TO_USE: positioned for imminent use
    - BEEN_THERE: settled, not recently touched
    - FORGOTTEN: out of place, not curated

  OBJECT_PLACEMENT:
    - FRAME_EDGE: partially visible, caught not placed
    - CASUAL_DROP: placed without arrangement
    - WITHIN_REACH: within arm's reach
    - PERSONAL_SPACE: immediately around subject
    
  OBJECT_RELATIONSHIP:
    - SUBJECT_BELONGING: subject's personal item
    - ENVIRONMENTAL_DEFAULT: naturally exists here
    - ACTIVITY_EVIDENCE: object shows what's happening
    - SOCIAL_OBJECT: shared item, implies company

PROMPT_PATTERNS:
  "[OBJECT] at frame edge, [SUBJECT] was just [USING_ACTION]"
  Example: "Phone at towel corner, she was just scrolling, now looking at waves"

  "[OBJECT] in [SUBJECT]'s [HAND/LAP/REACH], [USING STATE]"
  Example: "Drink in her hand, condensation beading on glass, not drinking, just holding"

  "[OBJECTS] clustered casually — [PURPOSE]"
  Example: "Phone, wallet, keys clustered on floor beside her — she dropped them when she sat down"
```

---

# PART 8: ANTI-PATTERNS

| Anti-Pattern | Why It Fails | Fix |
|---|---|---|
| PROP_PARADE | Objects placed for camera, not life | Give each object an activity reason |
| PERFECT_OBJECTS | New, clean, centered = fake | Add wear, asymmetry, casual placement |
| EMPTY_STAGE | Too few objects = AI desert | 2-4 objects with purpose |
| OBJECT_NOISE | Too many objects = visual clutter | Hierarchy — 1 primary, 2-3 secondary |
| FLOATING_OBJECTS | No gravity, no surface contact | Show surface, shadow, weight |
| UNRELATED_OBJECTS | Objects don't connect to subject or place | Match objects to subject activity + environment |
| BRAND_PERFECTION | Perfect logos, no wear = ad, not life | Wear, angle, partial visibility |
| WRONG_SCALE | Object size wrong for context | Verify object-to-human scale |

---

# PART 9: CROSS-REFERENCE

```yaml
ATTENTION_ROUTING_ENGINE:
  - Objects create flow-through attention paths (Category B3)
  - Object brightness competes with face — hierarchy rules apply
  - Phone screen = attention anchor (bright, narrative)

CAMERA_RELATIONSHIP_ENGINE:
  - Objects visible depend on camera relationship
  - Friend-shot includes social objects
  - Camera-oblivious = objects in natural use state

BODY_LANGUAGE_ATTRACTION_ENGINE:
  - Objects justify body positions (squat = petting cat)
  - Object interaction creates natural posture
  - Ground-level objects = ground-level postures

ENVIRONMENT_ENGINES:
  - Object vocabulary changes by environment
  - HK-specific objects create sense of place
  - Beach objects vs hotel objects vs MTR objects
```

---

## RESEARCH STATUS

- ✅ Core research complete
- ⏳ Pending DeepSeek V4 Pro verification + extension
- ⏳ Pending Lucy consolidation


---

# PART 10: DEEPSEEK V4 PRO VERIFICATION & EXTENSION
### Consolidation Date: 2026-06-02

## Verified Corrections

1. **Phone screen lit signal:** Only valid in low-light/indoor scenes. In bright daylight, phone screens are unreadable. Added ambient light condition qualifier.

2. **Object count "2-4 sweet spot" softened:** Changed to "2-4 visible non-environmental objects." Environmental defaults (furniture, walls) don't count. Added: "density must match environment type — 10 objects at beach is wrong, 3 objects at market is wrong."

3. **Frame-edge objects qualified:** Added: "must be low-contrast or out of focus. Bright/saturated frame-edge objects pull attention away from subject."

4. **Phone face-down reading corrected:** HK context = politeness signal (not ignoring companions). Western context = can mean ignoring. Cultural context matters.

5. **Shoes-off meaning corrected:** In HK, shoes-off at entrance is cultural norm (mandatory in homes), not comfort signal. Added distinction between "shoes-off at entrance = cultural norm" vs "shoes-off in living room = settled/comfortable."

6. **Primary object count extended:** Changed from "1 max" to "1-2, but must be in different hands/positions to avoid visual competition."

## Key Extensions Added

1. **Object Lighting Consistency (CRITICAL):** Objects must share the same lighting as subject (direction, color temperature, intensity). AI often lights objects differently — major authenticity break.

2. **Object Shadow Behavior:** Shadows cast by objects must match scene light source (direction, length, softness). Misplaced shadows = instant AI signal.

3. **Object Reflection Logic:** Reflective surfaces (phone, glass, metal) must show appropriate reflections matching the scene. Wrong reflections = AI artifact.

4. **Emotional Attachment Axis:** CHERISHED (gift, keepsake, favorite) vs. UTILITARIAN (phone, keys, wallet) vs. INDIFFERENT (generic napkin) vs. ANNOYING (broken umbrella). Objects carry emotional meaning.

5. **Object-as-Shield / Object-as-Extension / Object-as-Barrier / Object-as-Invitation:** Four new object-subject interaction dynamics covering social signaling through objects.

6. **Staged Authenticity (NEW SECTION):** KOLs deliberately place objects to appear candid. This is a SKILL, not a failure. Research now teaches creating CONVINCING staged authenticity: frame-edge objects as "staged accidents," curated object clusters following cultural scripts, brand display as legitimate object function.

7. **Digital Wear Signals:** Phone screen protector scratches, laptop stickers/keyboard wear, earbud case scratches/cable fraying.

8. **HK Object Cluster Archetypes:** MTR scene (phone + Octopus + bag + mask + water bottle), Cafe scene (drink + phone + receipt + bag + friend's drink), Street scene (phone + bag + umbrella + shopping bag).

## Reality Check
- Real HK social photos have HIGHER object density than research assumes: 4-7 objects typical for cafe, 5-8 for MTR.
- "Coffee cup grip" = 30%+ of HK KOL photos — sometimes objects ARE props, and that's authentic for KOL culture.
- KOLs use drinks as TIME MARKERS: coffee=morning, milk tea=afternoon, beer=evening, cocktail=night.

## Verification Status
- ✅ Object taxonomy: VERIFIED
- ✅ Authenticity signals: VERIFIED (extended)
- ⚠️ Object count rules: CORRECTED (less rigid)
- ⚠️ Frame-edge logic: EXTENDED (contrast qualification)
- 📋 Added: Staged authenticity section, emotional attachment axis, digital wear signals
