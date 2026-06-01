# Verification & Extension Analysis: OBJECT_LOGIC_ENGINE_V2

## Verification Notes

### ✅ CORRECT CLAIMS
- **Object-Reason Rule (Level 1-5 hierarchy)**: Sound. Activity evidence is indeed strongest; decorative is weakest. This aligns with cognitive load theory — viewers process action-linked objects faster.
- **Object Timing States (JUST_USED, IN_USE, etc.)**: Accurate. These map to real-world behavior patterns observed in candid photography.
- **HK-specific vocabulary**: Generally correct. Octopus card, red-white-blue bag, dai pai dong items are authentic signifiers. However, see below for missing items.
- **Anti-Prop Rules**: The detection criteria are solid. Perfectly centered, brand-new objects are the #1 giveaway of AI generation.

### ❌ FLAGGED CLAIMS (Need Evidence or Correction)

1. **"Phone screen still lit" as JUST_USED signal** — Partially wrong. In bright daylight, phone screens auto-dim or are unreadable. This signal only works in low-light or indoor scenes. Add: "Phone screen lit only if ambient light allows visibility."

2. **"Object Count Rule: Sweet Spot 2-4"** — Overly rigid. Real social photos often have 5-7 objects (e.g., a cafe table with drink, phone, wallet, keys, receipt, napkin, and friend's bag). The rule should be: "2-4 *visible* objects that are *not* environmental defaults." Environmental defaults (furniture, walls) don't count toward this limit.

3. **"Frame Edge objects = most authentic"** — True but incomplete. Frame-edge objects can also be *distracting* if they're bright, moving, or recognizable. A friend's elbow at frame edge is authentic; a bright red sign at frame edge pulls attention away from subject. Add: "Frame-edge objects must be low-contrast or out of focus to maintain authenticity without distraction."

4. **"Object Personality Mapping: Phone face down = she's present, engaged"** — Overgeneralization. In Hong Kong, phone face-down on a table is also a *cultural signal* of politeness (not ignoring companions). But in Western contexts, it can mean "I'm ignoring you." This needs cultural context.

5. **"Shoes off = she's settled, comfortable, at home"** — In Hong Kong, shoes-off is *mandatory* in most homes. This is not a signal of comfort but of cultural norm. The distinction matters: "Shoes off at entrance = cultural norm; shoes off in living room = settled."

6. **"Object Hierarchy: PRIMARY OBJECT (1 max)"** — False. Real photos often have *two* primary objects in interaction (e.g., phone in one hand, drink in the other). The rule should be: "1-2 primary objects, but they must be in *different* hands or positions to avoid visual competition."

7. **"Too Few Objects (0-1) = empty stage"** — Not always. Minimalist photography (e.g., portrait with only a face and sky) is valid. The rule applies to *environmental* shots, not close-ups. Add: "Rule applies to wide/medium shots; close-ups exempt."

## Extensions & Missing Patterns

### Missing Object States
The research covers 5 timing states but misses:
- **ABANDONED**: Object left behind (e.g., umbrella forgotten on MTR seat). Extremely authentic — implies distraction, rush, or carelessness.
- **BORROWED**: Object not belonging to subject (e.g., friend's jacket, borrowed charger). Adds social dimension.
- **MULTI-USE**: Object serving multiple purposes (e.g., phone used as mirror, bag used as pillow). Shows creativity, resourcefulness.

### Missing Object Types
- **Earbuds/Headphones**: Critical in HK — AirPods visible in ear or case, wire dangling, one earbud in while talking. Signals: "she's in her own world," "she's listening to something," "she just took them out."
- **Tissue packet**: Essential HK item — on table, in hand, peeking from bag. Signals: "she has a cold," "she's prepared," "HK humidity reality."
- **Fan (handheld)**: Battery-operated or folding fan — ubiquitous in HK summer. Signals: "she's hot," "she's outdoors," "she's local."
- **Shopping bag with logo**: Wellcome, Mannings, ParknShop — not just any bag. Specific logos create authenticity.
- **Water bottle**: Reusable or disposable — signals: "she's hydrated," "she's been walking," "HK heat."
- **Cigarette pack/lighter**: If subject smokes (or friend does). Signals: "she's taking a break," "social moment." ⚠️ Use sparingly — can dominate frame.

### Missing Object-Subject Dynamics
- **Object as shield**: Phone held in front of chest, bag held in front of body — signals: "she's protecting herself," "she's shy," "she's in a crowd."
- **Object as extension**: Phone used to point at something, bag swung to gesture — signals: "she's using objects to communicate."
- **Object as barrier**: Bag placed between subject and camera, drink held between them — signals: "she's creating distance," "she's not fully engaged."
- **Object as invitation**: Offering drink, showing phone screen to camera — signals: "she's sharing," "she's including you."

### Missing HK-Specific Patterns
- **"MTR etiquette" objects**: Phone held at specific angle (not blocking others), bag held in front (not swinging), mask in pocket (not on face but visible).
- **"Wet market" objects**: Plastic bag with produce, reusable bag, coin purse, receipt with Chinese characters.
- **"Cha chaan teng" objects**: Metal cup with milk tea, plastic menu, napkin dispenser, toothpick holder.
- **"Temple" objects**: Incense stick, red packet, joss paper, offering fruit.
- **"Night market" objects**: Street food on stick, phone for payment, shopping bag, selfie stick.

## Gap Analysis

### What's Missing Entirely

1. **Object Lighting Consistency** — Objects must have the *same* lighting as the subject. AI often lights objects differently (brighter, softer, different color temperature). This is a major authenticity signal.

2. **Object Shadow Behavior** — Objects must cast shadows consistent with the scene's light source. AI often omits or misplaces shadows. Add: "Shadow direction, length, and softness must match environment."

3. **Object Reflection** — Reflective surfaces (phone screen, glass, metal) must show *appropriate* reflections. AI often shows reflections that don't match the scene (e.g., phone screen reflecting a room that doesn't exist).

4. **Object Interaction with Other Objects** — Objects don't exist in isolation. A phone on a table interacts with: table surface, nearby drink condensation, napkin, receipt. These interactions create authenticity.

5. **Object Temperature** — Hot objects (coffee, tea) should show steam; cold objects (iced drink) should show condensation. AI often gets this wrong or inconsistent.

6. **Object Sound Implication** — Objects that make sound (phone ringing, drink being set down, bag zipper) imply audio context. This isn't visual but affects narrative: "She just heard something on her phone."

7. **Object Smell Implication** — Food, drink, flowers, incense imply smell. This adds sensory depth: "The coffee smell is still in the air."

8. **Object History** — Objects have backstory. A scarred table, a faded bag, a chipped mug — these tell time. AI generates objects without history.

9. **Object Gender/Culture** — Objects signal gender and culture. A pink phone case vs. black, a branded bag vs. unbranded, a specific drink choice. These are identity markers.

10. **Object Seasonality** — Umbrella in summer (sun), umbrella in spring (rain), scarf in winter, fan in summer. Objects must match season.

### Missing Cross-References
- **LIGHTING_ENGINE**: Object lighting consistency
- **COLOR_ENGINE**: Object color harmony with scene
- **COMPOSITION_ENGINE**: Object placement within rule of thirds
- **NARRATIVE_ENGINE**: Object as story element across multiple frames

## Strengthening Suggestions

### Section 2: Object Narrative Taxonomy
**Weakness**: Level 4 (Narrative Element) and Level 5 (Decorative) are dismissed as "weak" but are *essential* for storytelling. A flower in frame isn't always a prop — it can be a gift, a souvenir, or something she picked up.

**Fix**: Rename Level 4 to "SYMBOLIC OBJECT" and Level 5 to "ENVIRONMENTAL DECOR." Add: "Symbolic objects work when they have *in-world* justification (e.g., she was given a flower at a protest, she picked a flower on a hike). Environmental decor works when it's *part of the location* (e.g., cafe's decorative lamp, hotel's art piece)."

### Section 3: Object-Subject Relationship
**Weakness**: Attachment Levels are spatial only. Missing *emotional* attachment.

**Fix**: Add "EMOTIONAL ATTACHMENT" axis:
- **CHERISHED**: Object she values (gift, keepsake, favorite item)
- **UTILITARIAN**: Object she uses (phone, keys, wallet)
- **INDIFFERENT**: Object she doesn't care about (generic cafe napkin)
- **ANNOYING**: Object she's frustrated with (broken umbrella, tangled earbuds)

### Section 5: Anti-Clutter Rules
**Weakness**: Object Count Rule is too rigid. Real photos vary wildly.

**Fix**: Replace with "OBJECT DENSITY RULE":
- **Low density** (0-2 objects in frame): Works for close-ups, minimalist aesthetic
- **Medium density** (3-6 objects): Most natural for social photos
- **High density** (7-12 objects): Works for crowded scenes (cafe, market, party)
- **Very high** (13+): Only works for wide shots of busy environments

Add: "Density must match *environment type*. A beach shot with 10 objects is unnatural; a market shot with 3 objects is unnatural."

### Section 6: Object Authenticity Signals
**Weakness**: Wear and Use Vocabulary is good but misses *digital* wear.

**Fix**: Add:
- **Phone**: Screen protector scratches, case wear, charging port dust
- **Laptop**: Stickers, keyboard wear, trackpad shine
- **Earbuds**: Case scratches, ear tip wear, cable fraying

### Section 7: Prompt Language
**Weakness**: Prompt patterns are too generic. Need *HK-specific* patterns.

**Fix**: Add:
```
HK_PROMPT_PATTERNS:
  "[OBJECT] on [HK_SURFACE], [SUBJECT] [ACTION] nearby"
  Example: "Octopus card on MTR ticket machine, she's tapping, phone in other hand"

  "[OBJECT] in [HK_ENVIRONMENT], [SUBJECT] [STATE]"
  Example: "Red-white-blue bag on dai pai dong stool, she's eating egg waffle, condensation on milk tea cup"

  "[OBJECTS] clustered on [HK_SURFACE] — [PURPOSE]"
  Example: "Phone, wallet, keys, tissue packet on formica table — she just sat down at cha chaan teng"
```

### Section 8: Anti-Patterns
**Weakness**: Missing "OBJECT_GHOSTING" — objects that appear and disappear between frames.

**Fix**: Add:
| Anti-Pattern | Why It Fails | Fix |
|---|---|---|
| OBJECT_GHOSTING | Object appears in one frame, vanishes in next | Maintain object continuity across series |
| OBJECT_CLONING | Same object appears in multiple identical forms | Vary objects — no two identical items |
| OBJECT_MISPLACEMENT | Object in wrong environment (snow boots on beach) | Match object to environment + season |

## Reality Check

### How Real KOLs/Social Media Behave

**KOL Object Patterns (Instagram, Xiaohongshu, TikTok):**
1. **"The Coffee Cup Grip"** — Every HK KOL holds a coffee cup in at least 30% of photos. It's a *social prop*, not a drink. This contradicts the research's "activity evidence" rule — sometimes objects ARE props, and that's *authentic* for KOL culture.

2. **"The Phone as Accessory"** — KOLs often hold phones in ways that *don't* suggest use: phone held at side, phone in front of face (as partial shield), phone on table face-up (showing wallpaper). These are *staged* but read as authentic because they mimic real behavior.

3. **"The Bag Placement"** — KOLs place bags in specific positions: on floor beside them (showing brand), on table behind drink (showing brand), on lap (showing brand). This is *advertising*, not natural. The research should acknowledge that "brand display" is a real object function.

4. **"The Drink as Time Marker"** — KOLs use drinks to signal time of day: coffee = morning, milk tea = afternoon, beer = evening, cocktail = night. This is a *narrative* function the research misses.

5. **"The Object Cluster"** — Real KOL photos often show *intentional* object clusters: phone + coffee + notebook (work aesthetic), phone + cocktail + sunglasses (vacation aesthetic), phone + snack + water bottle (gym aesthetic). These are *curated* but read as authentic because they follow cultural scripts.

6. **"The 'Accidental' Object"** — KOLs deliberately place objects at frame edges to create "candid" feel. A friend's hand, a stranger's bag, a random sign — these are *staged accidents*. The research's "frame edge = authentic" is correct but incomplete: frame-edge objects can be *deliberately* placed.

**What Real HK Social Photos Actually Show:**
- **MTR photos**: Phone in hand (always), Octopus card visible (often), bag on lap or floor, mask in pocket or on chin, water bottle in bag side pocket.
- **Cafe photos**: Drink (always), phone (always), sometimes food, sometimes receipt, sometimes friend's drink, sometimes bag on chair.
- **Street photos**: Phone in hand, bag on shoulder, sometimes drink, sometimes shopping bag, sometimes umbrella.
- **Home photos**: Phone, laptop, water bottle, snack, sometimes pet, sometimes clothing item on chair.

**Key Insight**: Real HK social photos have *higher object density* than the research suggests. A typical cafe photo has 4-7 objects (drink, phone, bag, receipt, napkin, friend's drink, condiment rack). The "sweet spot" of 2-4 is too low for HK urban environments.

### Final Verdict

**Strengths**: Excellent taxonomy of object states, relationships, and authenticity signals. HK-specific vocabulary is strong. Anti-prop rules are practical.

**Weaknesses**: Overly rigid object count rules, missing cultural context for object behavior, insufficient acknowledgment of *staged authenticity* (KOLs deliberately create "candid" object arrangements), missing digital wear signals, no consideration of object lighting/shadow consistency.

**Recommendation**: Add a "STAGED AUTHENTICITY" section acknowledging that KOLs deliberately place objects to appear candid. This is *not* a failure — it's a *skill*. The research should teach how to create *convincing* staged authenticity, not just "natural" authenticity.