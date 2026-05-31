# Narrative Continuity System — V18

## Overview

The Narrative Continuity System addresses a fundamental challenge in AI-generated image sets: making multiple images feel like they belong to the same coherent experience—a family barbecue, a wedding day, a child's birthday, a European vacation. Human photographers naturally maintain continuity across a roll of film or a camera burst; AI image generation historically treats each prompt as an isolated event, resulting in inconsistent lighting, wardrobe changes mid-day, shifting skin tones, and contradictory weather. V18's CONT tokens encode the invisible connective tissue of visual storytelling.

---

## CONT-01: Garment Continuity Token

### Problem Statement

**How do you ensure a person wears the same outfit across five generated images depicting the same day?** V17 generates each image as an independent event—one prompt shows a red linen shirt, the next shows a blue sweater, breaking the narrative spell. Viewers immediately notice outfit discontinuities as "something wrong" even if they cannot articulate why.

### Why V17 Cannot Solve It

V17 processes each prompt in isolation. Even with identical subject descriptors ("woman in red linen shirt"), stochastic sampling produces variations. Color references resolve inconsistently across runs. Garment details like buttons, collars, and sleeve lengths drift between generations. The model has no mechanism to "remember" what a person wore in image 1 when generating image 4. Negative prompting ("do not change clothes") has limited effect because the model lacks a persistent wardrobe schema.

### Real Photography References

- **Family photo albums**: A Christmas morning sequence shows Dad in the same flannel shirt across kitchen, living room, and outdoor shots—the photographer dressed once and shot the entire event.
- **Wedding photobooks**: The bride wears the same gown in getting-ready frames, ceremony, and reception; viewers would reject a gown change between church and reception as surreal.
- **Travel diaries**: Instagram travel carousels show the same tourist in identical outfits at different landmarks (Eiffel Tower, Louvre, Seine riverbank)—this deliberate repetition signals "same trip."
- **Social media carousels**: Fashion influencers post "5 looks, one suitcase" where the same background location appears with outfit changes; the visual anchor (location) makes the outfit changes readable as intentional styling choices, not continuity errors.

### Human Behavioral Logic

People dress for the occasion and the weather, not frame-by-frame. A hiker starts in hiking boots and a fleece jacket and ends in the same gear after a mountain summit. Parents dress children once for a birthday party and shoot the entire event. Fashion photographers lock wardrobe choices before shooting begins. The human expectation when viewing a set of related images is wardrobe persistence—the same clothes persist unless there is an explicit narrative reason for change (bathing suit at beach, formal wear for dinner).

### Visual Evidence

- Consistent garment color family (warm earth tones, cool blues) across all frames
- Matching hardware (brass buttons, silver zippers, visible brand logos)
- Same fit and silhouette (loose linen, fitted denim)
- Unbroken accessories (watch on left wrist, necklace visible in all shots)

### Prompt Vocabulary

```
garment-locked, wardrobe-persistent, same-outfit-continuity,
outfit-coherence, consistent-clothing, unchanged-wardrobe,
same-day-attire, single-wardrobe-take, clothing-consistency,
outfit-lock, persistent-attire, look-locked, same-fits,
wardrobe-anchored, outfit-memory, attire-continuity
```

### Integration Rules

- Apply to primary subject tokens in multi-image generation requests
- Combine with CONT-02 (color palette lock) for garment color consistency
- Override: explicit narrative prompts ("later that evening she changed into...") supersede garment locking
- Weight recommendation: 0.7–0.85 for subtle wardrobe persistence, 0.85–1.0 for strict continuity (wedding, formal event)

### Anti-AI Benefits

Prevents the "costume change effect" where AI generates the same person in wildly different outfits across a story set. Outfit consistency is a primary cue that images derive from a real photographed event, not AI generation. Garment-locked sets read as authentic documentation; outfit variations signal synthetic or manipulated imagery.

### Example Prompt Fragments

```
"...same red linen shirt, garment-locked, outfit-coherence..."
"...outfit-continuity: the father wears the same flannel throughout..."
"...consistent-clothing across frames, unchanged-wardrobe, same-day-attire..."
```

---

## CONT-02: Color Palette Lock Token

### Problem Statement

**How do you maintain the same dominant color temperature and palette across an image set?** V17 may generate morning shots with warm golden tones, afternoon shots with flat daylight, and evening shots with cool blue light—but a real photo album from the same day maintains a unified color story. The viewer's eye catches palette discontinuities as "wrong" before they consciously identify them.

### Why V17 Cannot Solve It

V17 lacks a persistent color memory across generations. Each image resolves its own color temperature, white balance, and saturation independently. A prompt specifying "warm summer afternoon" resolves differently in each frame. The model cannot maintain "this series uses Kodak Portra 400 warmth" or "desaturated coastal palette" across independent generations.

### Real Photography References

- **Film photography**: A roll of Portra 400 shot in daylight has a consistent color signature; a roll of Tri-X has consistent black-and-white grain. Same-day albums inherit the film stock's color character.
- **Smartphone albums**: Images captured in Apple's "photographic styles" maintain unified color grading across a session.
- **Editorial photobooks**: A magazine's "same-day" fashion spread uses unified color grading to create cohesion across pages shot at different times.
- **Travel diaries**: A Greek island vacation album maintains consistent blue-and-white palette across all locations—the color story is part of the memory, not an accident.

### Human Behavioral Logic

Human memory distills days into color moods. A sunset beach day is remembered as golden and warm; an overcast forest hike is remembered as green and muted. When viewing a set of images labeled "Saturday at the farmers market," the viewer expects a unified color temperature. Palette discontinuity triggers "these aren't from the same event" even if the subject and location are consistent.

### Visual Evidence

- Unified color temperature across all frames (all warm, all cool, or deliberately consistent in variation)
- Matching saturation levels (all vibrant, all muted, all desaturated)
- Consistent color cast (slight orange warmth, blue shadows) maintained
- Harmonious palette that an editor would approve for a printed spread

### Prompt Vocabulary

```
palette-locked, color-temperature-consistent, unified-palette,
same-day-color, film-stock-matching, color-memory,
palette-coherence, warm-tone-consistent, cool-palette-lock,
color-grading-consistent, saturated-consistency, tone-locked,
color-story-persistent, unified-color-mood, palette-anchor
```

### Integration Rules

- Use as a modifier on lighting tokens rather than standalone
- Combine with CONT-03 (time-of-day lock) for strongest effect
- Can override individual image color prompts if set above 0.8 weight
- Weight recommendation: 0.75–0.9 for natural variation within palette, 0.9–1.0 for strict matching

### Anti-AI Benefits

AI-generated image sets frequently exhibit "color drift" where the same scene shifts temperature and saturation frame to frame. Palette locking produces the unified look of film photography or a curated smartphone album—both of which signal authentic capture rather than synthetic generation.

### Example Prompt Fragments

```
"...unified-palette, warm-tone-consistent, Kodak Portra warmth..."
"...palette-locked across all frames, same-day-color, tone-locked..."
```

---

## CONT-03: Time-of-Day Lock Token

### Problem Statement

**How do you ensure all images in a set register as the same time of day?** V17 may generate one image reading as morning light (long shadows, golden rim light), another as midday (flat overhead light), and a third as late afternoon (warm side-lighting). A real photographer adjusts shooting time or uses lighting modifiers to maintain consistent time-of-day cues.

### Why V17 Cannot Solve It

V17 has no temporal persistence. Each generation independently resolves its sun position, shadow length, and light quality. Prompting "sunset" in one frame and "golden hour" in another may produce overlapping or contradictory results. The model cannot maintain "this entire series is lit as 4pm October light" across four generations.

### Real Photography References

- **Family albums**: A full day of birthday photography maintains the same light quality despite hours passing—the photographer either shoots quickly or uses flash to override natural light changes.
- **Wedding timelines**: Bridesmaids photos taken at 3pm and reception photos at 8pm both read as "same wedding day" because editorial choices (backlighting, flash, golden hour timing) create consistent time-of-day cues.
- **Travel diaries**: Tourists visiting Rome in July shoot Colosseum at 10am and Trevi Fountain at 10am—both images share the harsh midday Mediterranean light.
- **Documentary photography**: A photo essay on "a day in the life" maintains consistent lighting cues (indoor ambient, window light, the same lamp) to signal temporal unity.

### Human Behavioral Logic

Time-of-day is a fundamental organizing principle for visual narratives. "Saturday morning" reads as specific light (soft, even, shadow direction) and specific mood (leisure, coffee, slow start). Viewers unconsciously map light quality to clock time. Inconsistency breaks the narrative contract—"these aren't from the same day."

### Visual Evidence

- Consistent shadow direction and length across all frames
- Matching light temperature (all golden, all flat, all blue-hour)
- Unchanged rim light position relative to subject
- Consistent indoor-outdoor light ratio in mixed scenes

### Prompt Vocabulary

```
time-locked, same-time-of-day, golden-hour-consistent,
midday-light, afternoon-light, morning-light, sunset-time,
blue-hour-lock, lighting-consistency, shadow-direction-locked,
light-quality-persistent, temporal-unity, sun-position-locked,
time-of-day-persistent, same-hour-light, lighting-memor
```

### Integration Rules

- Must be combined with lighting direction tokens (e.g., side-lit, backlit)
- Combine with CONT-02 (palette lock) for temporal color coherence
- Specify season as modifier: "late-afternoon November light" rather than just "afternoon"
- Weight recommendation: 0.8–0.95 for strict time-of-day lock

### Anti-AI Benefits

AI-generated sets commonly exhibit "time travel"—the same person in radically different lighting conditions frame to frame. Time-locked sets mimic the controlled shooting environment of professional photography (all shots at the same golden hour) or the deliberate timing of a film director. This kind of consistency signals production intentionality, not AI randomness.

### Example Prompt Fragments

```
"...same-time-of-day: 4pm October golden hour, shadow-direction-locked..."
"...time-locked, late-afternoon Mediterranean light, lighting-consistency..."
```

---

## CONT-04: Weather Continuity Token

### Problem Statement

**How do you ensure consistent weather across an image set?** V17 may generate the same beach scene with sunny skies in one frame and overcast clouds in another. Real photographers either shoot quickly enough that weather doesn't change, or use editing to impose a unified weather narrative on the day's images.

### Why V17 Cannot Solve It

V17 has no weather memory. Each generation independently resolves its atmospheric conditions. "Beach day" in one frame may mean brilliant sunshine; in another, haze and wind. The model cannot maintain "the entire series shows a slightly hazy coastal afternoon" across independent generations.

### Real Photography References

- **Travel albums**: A Greek island trip shows identical hazy Mediterranean atmosphere at the Acropolis, at a taverna, and on a ferry—the same atmospheric conditions imposed by editing or shooting speed.
- **Wedding albums**: Outdoor ceremonies and indoor receptions both carry the same "June afternoon" quality—warm, slightly golden, no rain.
- **Family barbecues**: A backyard party shows consistent mid-summer overcast (soft, even light) across pool, table, and porch shots—weather is an afterthought, but consistency is required.
- **Ski trip albums**: A full day on the mountain shows consistent bright, cold, high-contrast snow light across all frames.

### Human Behavioral Logic

Weather is an ambient context that humans expect to persist across an event. "That rainy Sunday in Paris" is a complete memory—rain is part of every frame. Viewers unconsciously normalize weather to the narrative context; they don't expect a beach album to shift from sunny to stormy between shots.

### Visual Evidence

- Consistent cloud formation type across frames (cumulus, overcast, clear)
- Same haze level and atmospheric perspective
- Matching precipitation cues (wet surfaces, umbrellas, indoor condensation)
- Uniform wind effect on hair, fabric, foliage

### Prompt Vocabulary

```
weather-consistent, same-weather, overcast-consistent,
sunny-day-lock, hazy-atmosphere, rain-day, snow-consistent,
atmospheric-persistence, weather-locked, same-sky,
cloud-consistency, fog-persistent, weather-memory,
storm-locked, clear-skies, humidity-persistent
```

### Integration Rules

- Combine with CONT-03 (time-of-day lock) and CONT-02 (palette lock) for full environmental coherence
- Weather overrides: explicit narrative weather changes ("the storm rolled in") should be sequential and directional
- Weight recommendation: 0.75–0.9 for natural weather consistency

### Anti-AI Benefits

Weather inconsistency is a signature artifact of AI image generation, where each frame is independently resolved. Weather-locked sets produce the cohesive atmosphere of a film scene or a real documentary, implying intentional production rather than stochastic generation.

### Example Prompt Fragments

```
"...same-weather: hazy coastal afternoon, atmospheric-persistence..."
"...weather-consistent, overcast-consistent, same-sky..."
```

---

## CONT-05: Skin Tone Persistence Token

### Problem Statement

**How do you maintain consistent skin tone across a multi-image set?** V17 frequently generates the same person's face with different base skin tones, undertone warmth, and luminosity across frames. A "same day, same person" set may show three different skin complexions, breaking continuity.

### Why V17 Cannot Solve It

V17 resolves skin tones stochastically within a prompted range. "Warm medium skin" may resolve as olive, tan, or golden in different frames. The model's latent space does not maintain a persistent skin tone embedding across independent generations. Even with detailed description, subtle undertone shifts occur.

### Real Photography References

- **Film photography**: A single roll of film processes all frames identically, ensuring the same person's skin reads consistently across an entire roll.
- **Digital photography**: A photographer using auto-white-balance and the same lens will produce consistent skin tones across a shoot.
- **Family albums**: Dad's skin looks like Dad's skin in January photos and July photos—not identical (summer tan is acceptable) but recognizably the same person.
- **Editorial spreads**: A model's skin is color-graded to be consistent across a fashion shoot, even across different lighting conditions.

### Human Behavioral Logic

Face recognition depends on skin tone as a primary identifier. A viewer seeing the same person with different skin tones in a supposedly connected image set immediately identifies a continuity error. "That person looks different" triggers skepticism about the images' authenticity or coherence.

### Visual Evidence

- Identical base skin tone across all frames (within realistic variation for lighting changes)
- Consistent undertone (warm, neutral, cool) across all frames
- Matching luminosity/brightness level under controlled lighting
- No artificial skin texture shifts (smooth vs. textured reads as different person)

### Prompt Vocabulary

```
skin-tone-persistent, consistent-complexion, same-skin,
undertone-locked, skin-consistency, complexion-matching,
natural-skin-tone, tone-consistent, skin-memory,
face-matching, persistent-complexion, same-undertone,
skin-coherence, luminosity-matched, subject-consistency
```

### Integration Rules

- Apply to subject tokens, not background figures
- Combine with CONT-02 (palette lock) for full-spectrum color consistency
- Weight recommendation: 0.8–0.95 for strict skin consistency
- Note: Some lighting variation is natural and acceptable; aim for "same person in different light" not "identical skin pixels"

### Anti-AI Benefits

Skin tone drift is a significant AI artifact that signals synthetic generation. Consistent skin tones across a set mimic the unified processing of film or the intentional color grading of professional photography—both hallmarks of authentic, produced imagery rather than stochastic AI output.

### Example Prompt Fragments

```
"...skin-tone-persistent, same-undertone, complexion-matching..."
"...consistent-complexion, natural-skin-tone across frames..."
```

---

## CONT-06: Object/Prop Continuity Token

### Problem Statement

**How do you maintain consistent objects across a set—the coffee mug in every frame, the bouquet in the second shot, the book on the table?** V17 may generate a different coffee mug shape, color, or placement in each frame. Real photographers place and reuse the same props throughout a shoot.

### Why V17 Cannot Solve It

V17 has no object persistence. Each generation places its own version of "a coffee mug" based on learned object priors. The mug in frame 1 and the mug in frame 4 may be entirely different objects sharing only the label "coffee mug."

### Real Photography References

- **Still life photography**: A photographer arranges a table setting once and photographs it from multiple angles—the same apple, the same linen napkin, the same ceramic cup.
- **Product photography**: A product launch shoot uses the same product unit (not different units of the same product) across all angles.
- **Family albums**: The birthday cake appears in the same condition across multiple shots; the same balloon stays in frame; the same chair appears in background shots.
- **Travel diaries**: The same red backpack appears at every landmark—the backpack is a continuity prop that anchors the narrative.

### Human Behavioral Logic

Objects tell the story. The coffee mug on the kitchen table says "Sunday morning." The bouquet says "celebration." When objects persist across frames, the viewer reads these as "same scene, different angle." When objects change, the viewer reads "different event."

### Visual Evidence

- Identical object design, color, and material across all frames
- Same wear patterns, labels, and surface details
- Consistent object placement relative to scene geography
- No anachronistic intrusions (a phone model that didn't exist in the scene's implied era)

### Prompt Vocabulary

```
object-locked, prop-consistency, same-object,
artifact-persistent, item-consistency, prop-lock,
object-memory, consistent-props, item-unchanged,
same-coffee-mug, scene-anchoring, prop-anchored,
object-continuity,道具锁定, item-persistence
```

### Integration Rules

- List critical objects explicitly in prompt; use object-locked token on each
- Combine with CONT-09 (scene geography lock) for placement consistency
- Weight recommendation: 0.75–0.9 for natural variation, 0.9–1.0 for strict prop lock
- Override: narrative destruction ("she crushed the paper cup") supersedes prop lock

### Anti-AI Benefits

Object inconsistency is a major AI artifact. The "different coffee mug" problem is a recognized signature of AI image generation. Object-locked sets mimic the discipline of professional photography and set design, where continuity is a production value, not an afterthought.

### Example Prompt Fragments

```
"...same red ceramic coffee mug, object-locked, prop-consistency..."
"...the birthday cake remains untouched, object-continuity..."
```

---

## CONT-07: Gaze/Facial Expression Continuity Token

### Problem Statement

**How do you maintain consistent facial expression mood across a set?** V17 may generate a person's face with a warm smile in frame 1 and a neutral expression in frame 4. A real photographer captures the same emotional register across the entire shoot—joy, solemnity, playfulness.

### Why V17 Cannot Solve It

V17 resolves expressions stochastically. The model's face latent space samples expression independently per generation. "Happy family" in one frame may mean laughing parents; in another, it may mean content but not smiling. No emotional persistence exists across generations.

### Real Photography References

- **Wedding photography**: The couple maintains a consistent affectionate, joyful expression across ceremony, portraits, and reception shots—not forced smiles in every frame, but the same emotional register.
- **Family albums**: A child's birthday captures genuine laughter and excitement, not a mix of crying, laughing, and neutral faces.
- **Fashion photography**: A campaign maintains the model's consistent expression (smolder, fresh-faced, serious) across all campaign images.
- **Documentary photography**: A photo essay on "market day" maintains the vendors' consistent working expressions (focused, engaged) across frames.

### Human Behavioral Logic

Emotional continuity is part of narrative coherence. A "joyful birthday" set should feel joyful throughout. Expression shifts are noticed as discontinuous events—"why is she sad in the second photo?"—and break the narrative spell. People in real photographs carry their emotional state across a scene; they don't randomly shift between joy, neutrality, and solemnity in the same hour.

### Visual Evidence

- Consistent expression category across frames (all smiling, all contemplative, all neutral content)
- Similar eye crinkling and smile depth (within natural micro-expression variation)
- Matching eyebrow position and forehead tension
- Consistent eye gaze direction when multiple angles are involved

### Prompt Vocabulary

```
expression-consistent, emotional-continuity, same-mood,
smile-consistent, expression-locked, facial-mood-persistent,
joyful-continuity, contemplative-same, expression-memory,
mood-locked, facial-consistency, expression-unchanged,
affective-consistency, emotional-register, expression-anchored
```

### Integration Rules

- Combine with CONT-05 (skin tone persistence) for face coherence
- Use expression category descriptors: "warm smile," "subtle smile," "content neutrality," "joyful laughter"
- Weight recommendation: 0.7–0.85 for natural emotional variation within a register
- Note: Some micro-expression variation is realistic and desirable

### Anti-AI Benefits

Expression inconsistency undermines the authenticity signal of any narrative image set. Consistent emotional register mimics the work of a skilled photographer who captures the right moment repeatedly, not the stochastic sampling of AI generation.

### Example Prompt Fragments

```
"...same warm smile, expression-consistent, emotional-continuity..."
"...joyful-continuity, smile-consistent across all frames..."
```

---

## CONT-08: Scene Geography Lock Token

### Problem Statement

**How do you maintain consistent spatial relationships across multiple images depicting the same location?** V17 may generate "kitchen scene" with a stove on the left wall in frame 1 and on the right wall in frame 2. A real photographer moves around a fixed set; the geography of the scene doesn't change.

### Why V17 Cannot Solve It

V17 has no spatial memory. Each generation constructs its own version of "a kitchen" from learned spatial priors. The model cannot maintain "the window is always behind the subject" or "the door is always on the left" across independent generations.

### Real Photography References

- **Real estate photography**: A property is photographed from multiple angles, but the house's architecture remains consistent—same window positions, same staircase, same room layout.
- **Family albums**: The backyard barbecue shows the same picnic table, same fence, same tree in every shot—the scene geography is fixed.
- **Travel photography**: The Colosseum is photographed from the south angle in morning shots and the same south angle in evening shots; the structure's features remain geographically consistent.
- **Fashion lookbooks**: A model poses against the same brick wall in multiple frames; the wall's features are consistent.

### Human Behavioral Logic

Spatial relationships are fundamental to scene recognition. When the geography shifts between frames ("the stove moved"), the viewer reads "different place" rather than "different angle." Even subtle geography shifts (a wall appearing in one frame but not another) break the sense of shared space.

### Visual Evidence

- Consistent architectural features in the same relative positions
- Same window and door placements across frames
- Matching background props and furniture positions
- No "impossible geometry" where perspective contradicts established scene layout

### Prompt Vocabulary

```
geography-locked, spatial-consistency, scene-fixed,
location-consistent, spatial-relationships-persistent,
room-geometry, architectural-consistency, set-locked,
scene-anchored, spatial-unity, layout-consistent,
background-consistency, environment-persistent,
scene-continuity, spatial-memory
```

### Integration Rules

- Combine with CONT-04 (weather continuity) for environmental totality
- Specify cardinal directions when relevant: "window light from the north"
- Use camera angle tokens in conjunction: "three-quarter view, same perspective"
- Weight recommendation: 0.8–0.95 for strict geography lock

### Anti-AI Benefits

Spatial inconsistency is a known AI artifact—"impossible kitchens" where the layout contradicts itself. Geography-locked sets mimic the discipline of shooting on a fixed set or in a fixed location, signaling authentic capture rather than AI hallucination.

### Example Prompt Fragments

```
"...geography-locked, kitchen scene fixed, spatial-consistency..."
"...same brick wall background, scene-anchored, room-geometry..."
```

---

## CONT-09: Hair/Styling Continuity Token

### Problem Statement

**How do you maintain consistent hairstyle and hair color across a set?** V17 may generate a person's hair as long and wavy in one frame, short and straight in another, or change the hair color mid-session. Real photographers capture the same person with the same hairstyle throughout a shoot.

### Why V17 Cannot Solve It

V17 resolves hair independently per generation. The model's face and hair latent spaces are sampled separately for each image. "Woman with auburn hair" may resolve as brunette, red, or copper in different frames. Hair length and style may shift due to stochastic sampling.

### Real Photography References

- **Wedding photography**: The bride's hairstyle is locked for the entire day—bridal portrait, ceremony, and reception all show the same updo or flowing style.
- **Family albums**: A child's pigtails persist across all birthday party frames; the father's haircut looks the same in every photo from that year.
- **Passport and ID photography**: The same person in multiple official photos maintains consistent hair because the hair hasn't changed and the photo conditions are standardized.
- **Fashion photography**: A model's hairstyle is consistent across a campaign shoot—same cut, same color, same styling.

### Human Behavioral Logic

Hair is a primary personal identifier. Viewers notice "different hair" in a supposedly connected set as a discontinuity error. A person's hair doesn't change over the course of a birthday party or a vacation day. The viewer expects hair consistency as part of the identity confirmation process.

### Visual Evidence

- Same hair color (within realistic lighting variation for highlights/shadows)
- Same hair length and cut silhouette
- Same styling approach (straightened, curled, natural, updo)
- Consistent hair texture reading (smooth, textured, voluminous)

### Prompt Vocabulary

```
hair-locked, hairstyle-consistent, same-hair,
hair-color-persistent, styling-continuity, hair-memory,
cut-consistent, hair-consistency, style-locked,
texture-consistent, fringe-consistent, haircut-matching,
grooming-persistent, hair-unchanged, style-memory
```

### Integration Rules

- Combine with CONT-05 (skin tone persistence) for full subject identity
- Specify hair accessories when relevant: "same gold clip, same headband"
- Weight recommendation: 0.8–0.95 for strict hair lock
- Note: Some highlight variation under different lighting is acceptable

### Anti-AI Benefits

Hair inconsistency is a recognizable AI artifact. The "different hair in every frame" problem is a signature of AI generation and undermines the authenticity of narrative sets. Hair locking mimics the discipline of professional portrait and fashion photography.

### Example Prompt Fragments

```
"...hair-locked, auburn waves, hairstyle-consistent..."
"...same long straight black hair, styling-continuity..."
```

---

## CONT-10: Identity/Subject Persistence Token

### Problem Statement

**How do you ensure the same specific person appears in all frames of a multi-image set?** V17 may generate what appears to be the same person (similar face shape, similar build) but with wholly different facial features in each frame. A real photographer photographs the same subject; their face is the connecting thread across all images.

### Why V17 Cannot Solve It

V17 lacks a subject identity embedding. Each generation samples from the model's latent face space independently. The result is "different people who look like they could be related" rather than "the same person." No mechanism exists to say "this is the same face in image 1 and image 4."

### Real Photography References

- **Family photo albums**: The grandmother appears in every Christmas photo across decades; her face is a fixed reference point.
- **Wedding albums**: The bride is the visual anchor of every image—she appears in getting-ready shots, ceremony, portraits, and reception, always recognizably herself.
- **Travel diaries**: The tourist is present in every frame, identifiable by consistent facial features, body proportions, and posture.
- **Documentary series**: A photo essay on "the fisherman" features the same man in every image; his face is the narrative through-line.

### Human Behavioral Logic

Subject identity is the primary narrative thread. "Look, it's Sarah at her birthday" requires Sarah to be recognizably the same Sarah in every frame. When faces shift between frames, the viewer loses the narrative thread and reads the images as unrelated or fabricated.

### Visual Evidence

- Identical facial proportions and bone structure across frames
- Consistent distinguishing features (birthmarks, eyebrow shape, nose profile)
- Matching skin tone and texture (see CONT-05)
- Same hair (see CONT-09) and consistent eyewear when applicable

### Prompt Vocabulary

```
same-person, subject-persistent, identity-consistency,
person-locked, face-matching, subject-consistency,
individual-anchored, identity-unchanged, subject-memory,
face-consistent, person-anchored, subject-coherence,
familiar-face, same-individual, subject-unity, identity-persistent
```

### Integration Rules

- Apply at the highest level of the generation prompt—subject identity overrides other tokens
- Combine with CONT-05 (skin tone), CONT-09 (hair), and CONT-07 (expression) for full identity coherence
- Weight recommendation: 0.85–1.0 for strict subject persistence
- Note: Slight age-related variation within a set is acceptable (aging overnight)

### Anti-AI Benefits

Subject identity drift is a critical AI artifact that breaks the fundamental promise of a narrative image set—"this is the same person having this experience." Identity-locked sets mimic the primary characteristic of authentic photography: the camera records who was actually there.

### Example Prompt Fragments

```
"...same-person: the mother, subject-persistent, identity-consistency..."
"...person-locked, recognizable face across all frames..."
```

---

## CONT-11: Narrative Event Continuity Token

### Problem Statement

**How do you ensure the images in a set represent a coherent narrative sequence?** V17 may generate images that are individually beautiful but narratively disconnected—one image shows greeting guests, another shows the cake being cut, another shows opening gifts, without a clear sequence. Real photographers shoot to a narrative arc: arrival → activity → conclusion.

### Why V17 Cannot Solve It

V17 has no narrative logic. Each generation is an isolated event prompt. The model cannot maintain "this is a chronological sequence" or "these three images show the progression of the party." No mechanism exists to encode cause-and-effect or temporal sequence.

### Real Photography References

- **Wedding albums**: Chronological narrative from getting ready (perfume, dress) → ceremony (vows) → portraits → reception (first dance, cake, toasts) → departure.
- **Birthday parties**: Arrival (guests arriving) → gift opening → cake → party games → departure.
- **Travel diaries**: Arrival (airport, hotel) → exploration (landmarks, food) → return (souvenirs, sunset).
- **Day-in-the-life photo essays**: Morning routine → commute → work → evening routine.

### Human Behavioral Logic

Narrative has structure. A set of images titled "Sarah's 30th Birthday" is expected to follow the party's natural arc. Viewer cognitive engagement depends on narrative coherence—the sense that these images document something that happened in time, in sequence. Out-of-order or disconnected images break the story.

### Visual Evidence

- Logical event progression across frames (before → during → after)
- Consistent participant engagement levels across narrative stages
- Matching activity-to-setting appropriateness
- No impossible temporal sequences (cake fully eaten before it appears uneaten)

### Prompt Vocabulary

```
narrative-sequence, event-continuity, chronological-flow,
story-arc, temporal-progression, narrative-coherence,
event-logic, scene-sequence, story-continuity,
documentary-flow, chronological-continuity, event-arc,
narrative-logic, sequence-coherence, temporal-unity
```

### Integration Rules

- Apply at the prompt level for multi-image generations
- Specify explicit sequence markers: "arriving at," "then," "later that afternoon"
- Combine with time-of-day lock (CONT-03) for temporal coherence
- Weight recommendation: 0.7–0.9 for natural narrative flow

### Anti-AI Benefits

AI-generated image sets often lack narrative logic—they show disconnected "moments" without causal connection. Narrative continuity tokens impose the structure of authentic documentary photography, where the photographer was present for the full event and recorded its natural arc.

### Example Prompt Fragments

```
"...chronological-flow: arrival, cake, gifts, narrative-sequence..."
"...event-continuity, story-arc across the afternoon..."
```

---

## CONT-12: Posture/Body Position Continuity Token

### Problem Statement

**How do you maintain consistent body positioning across a set?** V17 may generate the same person standing in one frame, seated in another, or in a different pose entirely. A real photographer captures a person who is either moving through activities (standing at the counter, sitting at the table, walking outside) or holding a consistent pose across frames.

### Why V17 Cannot Solve It

V17 samples body pose independently per generation. No mechanism exists to maintain "the subject is standing throughout" or "the sitting pose is held across all frames." Poses shift stochastically, breaking physical continuity.

### Real Photography References

- **Fashion photography**: A model's pose is consistent across all product shots—same stance, same angle, same weight distribution.
- **Family albums**: A toddler's birthday shows the child standing (new milestone) consistently throughout the party, not randomly sitting and standing between frames.
- **Sports photography**: An athlete's running form is captured consistently across a sequence of action shots.
- **Couples photography**: Partners maintain consistent physical relationship (facing each other, holding hands) across a portrait series.

### Human Behavioral Logic

Body position is part of scene realism. A person at a birthday party doesn't randomly teleport between standing and sitting. The viewer's body-schema expectations require consistent physical positioning within a single event.

### Visual Evidence

- Consistent overall posture (upright, relaxed, leaning)
- Matching weight distribution (standing on same foot, seated position)
- Same handedness (drinking from right hand consistently)
- Same physical relationship to objects and other subjects

### Prompt Vocabulary

```
posture-consistent, pose-locked, body-position-persistent,
standing-consistent, seated-same, pose-memory,
physical-continuity, body-locked, stance-consistent,
position-anchored, gesture-consistent, posture-unchanged,
body-geometry, physical-relationship-maintained,
stance-persistent
```

### Integration Rules

- Combine with CONT-06 (object continuity) for interaction coherence
- Specify key poses: "seated at the kitchen table, hands around mug"
- Weight recommendation: 0.7–0.85 for natural variation, 0.85–1.0 for strict pose lock
- Note: Some variation is natural for candid documentary style

### Anti-AI Benefits

Pose inconsistency is a recognizable AI artifact that undermines the physical realism of a narrative set. Posture locking mimics the intentional posing discipline of professional photography.

### Example Prompt Fragments

```
"...seated at the kitchen table, posture-consistent across frames..."
"...standing throughout, pose-locked, body-position-persistent..."
```

---

## CONT-13: Fabric Texture/Pattern Continuity Token

### Problem Statement

**How do you maintain consistent fabric patterns and textures across garments in a set?** V17 may generate a striped shirt in one frame and a solid-colored version of the same shirt in another. A real photographer dresses the subject in the same garment; the pattern and texture are inseparable from the garment identity.

### Why V17 Cannot Solve It

V17 resolves fabric texture stochastically. "Blue striped linen shirt" may resolve as horizontal stripes, vertical stripes, polka dots, or solid blue in different frames. The textile pattern is not locked to the garment identity.

### Real Photography References

- **Fashion photography**: A model's striped sweater shows the same stripe width, spacing, and direction in every campaign image.
- **Family albums**: Dad's plaid flannel shirt has the same plaid pattern in every frame—no "alternate version" of the shirt.
- **Luxury goods photography**: A leather handbag's exact grain pattern is consistent across all angles.
- **Wedding photography**: The lace overlay on a wedding gown maintains the same lace pattern across all images.

### Human Behavioral Logic

Fabric texture and pattern are details that confirm garment identity. A viewer who notices a striped shirt notices the pattern as part of recognizing "that shirt from the first photo." When the pattern changes, the viewer reads "different shirt," breaking garment continuity.

### Visual Evidence

- Identical stripe width, spacing, and direction
- Consistent weave texture (linen weave, twill, knit)
- Same plaid/tartan/check pattern placement
- Matching fabric weight reading (sheer, medium, heavy)

### Prompt Vocabulary

```
fabric-consistent, pattern-locked, textile-continuity,
stripe-consistent, plaid-matching, texture-persistent,
weave-consistency, pattern-unchanged, textile-memory,
fabric-locked, material-consistency, pattern-same,
print-consistent, textile-anchored, garment-texture
```

### Integration Rules

- Combine with CONT-01 (garment continuity) for full textile coherence
- Specify pattern type explicitly: "blue and white vertical stripes"
- Weight recommendation: 0.8–0.95 for strict pattern lock

### Anti-AI Benefits

Fabric pattern inconsistency is a subtle but recognizable AI artifact. Pattern locking produces the textile consistency of real photographed garments, signaling authentic capture rather than stochastic generation.

### Example Prompt Fragments

```
"...blue and white vertical stripes, pattern-locked, fabric-consistent..."
"...plaid-matching, textile-continuity, same flannel weave..."
```

---

## CONT-14: Accessory/Personal Item Continuity Token

### Problem Statement

**How do you maintain consistent accessories—jewelry, watches, glasses, bags—across a set?** V17 may generate a watch on the left wrist in one frame and no watch in another, or glasses that appear and disappear. Real photographers notice these details; a person wears their accessories for the duration of an event.

### Why V17 Cannot Solve It

V17 resolves accessories stochastically per frame. Items are treated as optional attributes that may or may not appear in each generation. No mechanism exists to maintain "the gold watch is always on the left wrist."

### Real Photography References

- **Portrait photography**: A subject's earrings, necklace, and watch are consistent across a portrait session.
- **Fashion photography**: A model's jewelry (statement necklace, stacked bracelets) is consistent across a campaign.
- **Family albums**: Grandmother's pearl earrings appear in every frame of Christmas morning—she didn't remove them between shots.
- **Travel diaries**: The tourist's fanny pack or day bag appears in every frame of the day's adventure.

### Human Behavioral Logic

Accessories are identity details. The gold watch is part of how we recognize a person. When accessories appear and disappear between frames, the viewer registers "these images are from different events" or "something is wrong with these photos."

### Visual Evidence

- Same jewelry pieces in same positions (watch on left wrist, earrings in ears)
- Consistent eyewear (glasses on/off as established)
- Same bag or carry item present across all frames
- Matching accessory style (delicate gold chain in all frames)

### Prompt Vocabulary

```
accessory-consistent, jewelry-locked, watch-persistent,
glasses-consistent, item-persistence, accessory-anchored,
personal-item-unchanged, same-watch, same-earrings,
bag-consistent, accessory-memory, item-locked,
jewelry-same, personal-effects-consistent, accessory-unchanged
```

### Integration Rules

- List critical accessories explicitly in prompt with the accessory-locked token
- Combine with CONT-01 (garment continuity) and CONT-06 (object continuity)
- Weight recommendation: 0.75–0.9 for natural accessory consistency

### Anti-AI Benefits

Accessory inconsistency is a subtle AI artifact that breaks the "same person, same day" reading. Accessory locking mimics the professional photographer's awareness of continuity details—the marks of authentic documentary work.

### Example Prompt Fragments

```
"...gold watch on left wrist, watch-persistent, accessory-consistent..."
"...same pearl earrings, jewelry-locked, accessory-anchored..."
```

---

## CONT-15: Background Figure Consistency Token

### Problem Statement

**How do you maintain consistent background figures across a set without them becoming the primary subject?** V17 may generate different people in the background of each frame—a restaurant scene shows different patrons in each image. Real photographers accept background figures but work to ensure they don't become distracting continuity errors.

### Why V17 Cannot Solve It

V17 resolves background independently per frame. Each generation creates its own cast of background figures with no memory of who appeared in previous frames.

### Real Photography References

- **Event photography**: Background guests are consistent people (aunt's red jacket appears in multiple shots), not randomly generated figures.
- **Street photography**: The same person walking a dog appears in consecutive shots of a street scene.
- **Travel photography**: A busy square shows the same identifiable background figures across multiple frames.
- **Architecture photography**: Background pedestrians are either absent (long exposure) or consistent across frames.

### Human Behavioral Logic

Background figures anchor a scene in real space. When the background crowd changes completely between frames, the viewer reads "different location" or "different time" rather than "different angle of the same place."

### Visual Evidence

- Same identifiable background figures appearing across frames (when intentionally captured)
- Consistent crowd density (same number of people, same level of busyness)
- Matching background activity type (not swinging from lampposts when previous frames showed walking)
- No impossible crowd shifts (empty street → crowded → empty in three frames)

### Prompt Vocabulary

```
background-consistent, crowd-consistency, figure-consistent,
secondary-subjects-persistent, background-anchored,
crowd-density-locked, passerby-consistent, scene-occupants,
ambient-figures-same, background-unchanged, crowd-memory,
environmental-consistency, background-unity, figure-memory
```

### Integration Rules

- Set this token lower than primary subject tokens (CONT-10, CONT-05)
- Use for documentary/narrative sets where background realism matters
- Weight recommendation: 0.6–0.8 for natural background variation within consistency bounds
- Note: For isolated subject shots (studio, plain background), this token is less critical

### Anti-AI Benefits

Background figure consistency is a marker of authentic event photography versus staged or AI-generated scenes. Consistent background figures signal "you are there, in the same moment" rather than "random scene sampled from training data."

### Example Prompt Fragments

```
"...same café, background-anchored, ambient-figures-same..."
"...consistent crowd density, background-consistent..."
```

---

## CONT-16: Ambient Sound/Time Cue Consistency Token

### Problem Statement

**How do you encode time-of-year and season consistency beyond weather—the sense that it's clearly a summer day or a winter afternoon?** V17 may generate winter scenes without seasonal cues, or summer scenes that read as ambiguous. Human photographers shoot in the appropriate season or use wardrobe and environment to establish season.

### Why V17 Cannot Solve It

V17 lacks seasonal memory. Each generation resolves its own seasonal cues—foliage, clothing weight, light quality—independently. No mechanism exists to maintain "this entire set is a July afternoon in Tuscany."

### Real Photography References

- **Seasonal travel albums**: A December Paris trip shows the same bare trees, winter coats, and indoor café atmosphere in every frame.
- **Holiday cards**: The family's Christmas card photos establish winter cues consistently (coats, scarves, breath visible in cold air).
- **Summer camp photography**: The same camp activities show consistent summer indicators (short sleeves, sunscreen, bright sun) across the album.
- **Autumn foliage photography**: A New England fall color tour shows consistent October leaf color, light, and atmosphere.

### Human Behavioral Logic

Season is a fundamental organizing frame for visual memory. "Last summer" has a specific look—bright, warm, long shadows. "Last winter" has another. When season cues are consistent, the viewer immediately locates the narrative in time. Inconsistency ("snow in one frame, bare trees in the next") breaks temporal memory.

### Visual Evidence

- Consistent foliage type and color (autumn leaves, summer green, spring blossoms)
- Same clothing weight and coverage appropriate to season
- Matching sun angle and shadow quality for latitude and season
- Consistent seasonal ambient cues (snow on ground, bare trees, summer haze)

### Prompt Vocabulary

```
season-consistent, same-season, summer-day, winter-afternoon,
autumn-leaves, spring-morning, seasonal-cues,
time-of-year-locked, season-locked, foliage-consistent,
snow-consistent, seasonal-memory, annual-cycle,
summer-light, winter-atmosphere, seasonal-anchored
```

### Integration Rules

- Combine with CONT-03 (time-of-day) and CONT-04 (weather) for full temporal coherence
- Specify geographic latitude: "July afternoon in Tuscany" vs. "July afternoon in Norway"
- Weight recommendation: 0.8–0.95 for strict season lock

### Anti-AI Benefits

Seasonal inconsistency is a marker of AI generation—AI models often blend seasonal cues or fail to fully commit to a season. Season locking produces the unified atmospheric identity of real location-based photography.

### Example Prompt Fragments

```
"...July afternoon in Tuscany, season-consistent, summer-light..."
"...October New England, autumn-leaves, seasonal-cues..."
```

---

## CONT-17: Inter-Personal Relationship Consistency Token

### Problem Statement

**How do you maintain consistent physical relationships between multiple subjects—holding hands, facing each other, standing together—across frames?** V17 may generate a couple facing the camera in one frame and facing away in another, breaking the established relationship.

### Why V17 Cannot Solve It

V17 samples inter-subject positioning independently per frame. No mechanism exists to maintain "the couple is always facing each other" or "the children are always between the parents."

### Real Photography References

- **Family photography**: Parents flank children consistently; the family unit maintains its spatial configuration across all frames.
- **Wedding photography**: The couple faces each other at the altar, in portraits, and in reception candids—their physical relationship is the narrative core.
- **Friendship photography**: A group of friends maintains its friendship circle spatial arrangement throughout an event.
- **Couples photography**: Partners hold consistent physical relationship (touching, facing each other) as the sign of their bond.

### Human Behavioral Logic

Physical relationship between subjects carries emotional meaning. A couple who holds hands at a wedding doesn't drop hands between ceremony and reception shots without narrative reason. The viewer's emotional engagement depends on consistent inter-personal dynamics.

### Visual Evidence

- Consistent physical proximity between subjects (close together, maintaining distance)
- Matching gaze direction between subjects (facing each other, looking at camera together)
- Same contact points (holding hands, arm around waist) maintained
- Consistent grouping geometry (triangle, line, cluster)

### Prompt Vocabulary

```
relationship-consistent, couple-anchored, family-configuration,
spatial-relationship-persistent, together-maintained,
group-geometry, proximity-consistent, facing-each-other,
physical-bond, interpersonal-anchored, connection-maintained,
touch-consistent, togetherness, couple-consistency,
family-anchored, relationship-geometry
```

### Integration Rules

- Combine with CONT-10 (subject persistence) for individual identity coherence
- Specify the relationship explicitly: "holding hands," "arm around shoulder"
- Weight recommendation: 0.8–0.95 for strict relationship lock

### Anti-AI Benefits

Relationship inconsistency—subjects randomly positioned relative to each other—is a marker of AI generation, which lacks intentional compositional design. Relationship locking mimics the compositional discipline of professional portrait and event photography.

### Example Prompt Fragments

```
"...couple facing each other, relationship-consistent..."
"...family configuration: parents flanking children, together-maintained..."
```

---

## CONT-18: Scale/Proportion Consistency Token

### Problem Statement

**How do you maintain consistent relative scale between subjects and objects across frames?** V17 may generate a coffee mug that appears normal size in frame 1 and toy-sized in frame 4, or a child who is suddenly taller than a parent. Real photographers maintain consistent perspective and scale through lens choice and camera position.

### Why V17 Cannot Solve It

V17 lacks scale persistence. Each generation independently resolves the scale relationships between objects. No mechanism exists to maintain "the mug is always a standard coffee mug size relative to the hands."

### Real Photography References

- **Product photography**: A watch is photographed at a consistent scale relative to human hands across all product shots.
- **Family photography**: A child's height relative to parents remains consistent across a birthday party—no impossible growth spurts between cake and presents.
- **Real estate photography**: A room's furniture maintains consistent relative scale across all angles.
- **Travel photography**: A tourist's proportions relative to landmarks are consistent across all frames (normal human scale, not suddenly giant or tiny).

### Human Behavioral Logic

Scale is a fundamental reality cue. Objects have known sizes; humans have known heights. When scale breaks, the viewer reads "unrealistic" or "wrong." A mug that changes size between frames triggers the same dissonance as a floating coffee cup or an impossible staircase.

### Visual Evidence

- Objects maintain consistent size relative to human hands
- Subject height relationships remain stable (children shorter than adults)
- No impossible scale shifts between frames
- Consistent perspective compression (same lens feel across frames)

### Prompt Vocabulary

```
scale-consistent, proportion-locked, size-consistent,
relative-scale, proportion-persistent, scale-locked,
object-size-consistent, perspective-consistent, scale-memory,
dimension-consistent, size-persistent, scale-anchored,
human-scale, proportion-unchanged, scale-unity
```

### Integration Rules

- Combine with CONT-08 (scene geography lock) for full spatial coherence
- Use for sets involving objects of known size or multiple subjects of known relative height
- Weight recommendation: 0.8–0.95 for strict scale lock

### Anti-AI Benefits

Scale inconsistency is a known AI artifact—"the impossible coffee mug" problem. Scale locking produces the geometric realism of photography, where lens perspective and focal length create consistent spatial relationships.

### Example Prompt Fragments

```
"...standard coffee mug size, scale-consistent across frames..."
"...child remains shorter than parents, proportion-locked..."
```

---

## CONT-19: Lighting Ratio/Contrast Consistency Token

### Problem Statement

**How do you maintain consistent lighting ratio (key-to-fill ratio, contrast level) across a set?** V17 may generate one frame with high-contrast hard light and another with flat low-contrast light, even within the same time-of-day. Real photographers maintain consistent lighting ratios through consistent light sources.

### Why V17 Cannot Solve It

V17 resolves lighting ratios independently per frame. Each generation samples its own key-to-fill ratio from learned lighting priors, resulting in dramatically different contrast levels between frames that should share lighting.

### Real Photography References

- **Studio photography**: A model's portrait session uses the same light setup (key, fill, hair light) throughout—all frames share the same contrast ratio.
- **Event photography**: A wedding reception with the same flash setup produces consistent contrast ratios across all frames.
- **Fashion photography**: A campaign maintains the same lighting ratio (high key, dramatic, natural) across all campaign images.
- **Documentary photography**: A photo essay maintains the ambient-to-flash ratio established by the photographer's equipment choices.

### Human Behavioral Logic

Lighting ratio is a mood signature. High-contrast lighting reads as dramatic or harsh; low-contrast reads as soft or overcast. When contrast shifts mid-narrative, the viewer reads "different lighting setup" rather than "same moment, different angle." The emotional tone is broken.

### Visual Evidence

- Consistent shadow density (same depth of black in shadows)
- Same highlight rolloff quality (hard vs. soft edge)
- Matching fill light level (more fill = flatter, less fill = more contrast)
- Consistent rim light presence and intensity

### Prompt Vocabulary

```
contrast-consistent, lighting-ratio-locked, key-fill-consistent,
high-key-consistent, low-key-consistent, contrast-locked,
shadow-density, highlight-rolloff, fill-level-consistent,
lighting-character, rim-light-maintained, key-ratio,
chiaroscuro-consistent, tonal-consistency, contrast-anchored
```

### Integration Rules

- Combine with CONT-03 (time-of-day lock) for full lighting coherence
- Specify lighting setup explicitly: "single window, north-facing, white curtain diffusion"
- Weight recommendation: 0.8–0.95 for strict lighting ratio lock

### Anti-AI Benefits

Contrast inconsistency is a subtle but pervasive AI artifact. Lighting ratio locking produces the unified look of a professionally lit set or a consistently captured film roll—both signals of intentional production versus AI stochastic generation.

### Example Prompt Fragments

```
"...same north-facing window light, contrast-consistent..."
"...high-key lighting, fill-level-consistent, lighting-ratio-locked..."
```

---

## CONT-20: Narrative Resolution Continuity Token

### Problem Statement

**How do you ensure an image set has narrative closure—the sense that the story has reached a natural end point?** V17 may generate a set of images that feel like they could continue forever. Real photographers capture narrative arcs with beginnings, middles, and ends.

### Why V17 Cannot Solve It

V17 has no narrative structure sense. Each generation is an isolated moment. The model cannot recognize that a birthday party has a natural conclusion (guests leaving, cake mostly eaten, presents open) versus a mid-party freeze.

### Real Photography References

- **Wedding albums**: Conclude with departure (grandparents leaving, couple driving away), the classic narrative close.
- **Birthday parties**: Conclude with the child tired, the cake cut, presents open—the event's natural denouement.
- **Travel diaries**: Conclude with sunset, airport, or returning to hotel—the day's narrative resolution.
- **Photo essays**: End on a resonant image that signals "the story is over"—a closing shot.

### Human Behavioral Logic

Narrative has structure. Viewers unconsciously expect stories to have arcs. A set of images that ends mid-action ("the party is still going") feels incomplete. Narrative resolution—a clear sense of "and that was the day" —is what separates a photo album from a random image dump.

### Visual Evidence

- Natural conclusion cues in final frames (slowing activity, guests departing, sunset)
- The emotional climax has been captured and the narrative is winding down
- Final frames carry the "end of day" energy rather than "mid-event" energy
- Visual "the End" cues: closed books, blown-out candles, suitcases zipped

### Prompt Vocabulary

```
narrative-resolution, story-closure, natural-ending,
conclusion-cued, arc-complete, denouement-visualized,
final-frame-energy, story-ended, natural-close,
resolution-visited, closing-moment, ending-visualized,
finale-framed, epilogue-visualized, narrative-complete
```

### Integration Rules

- Apply to the final frame(s) of a multi-image generation
- Combine with CONT-11 (narrative event continuity) for full arc coherence
- Weight recommendation: 0.65–0.8 (narrative resolution should feel natural, not forced)
- Note: Not every set needs explicit resolution; documentary-style sets may deliberately end mid-event

### Anti-AI Benefits

AI-generated sets often lack narrative closure—they produce beautiful moments without story structure. Narrative resolution tokens impose the arc structure of authentic storytelling, where the photographer was present for the whole event and knew when it was over.

### Example Prompt Fragments

```
"...narrative-resolution, story-closure, final-frame-energy..."
"...conclusion-cued: candles blown out, guests departing, natural-ending..."
```

---

## Integration Matrix

| Token Pair | Combined Weight | Effect |
|---|---|---|
| CONT-01 + CONT-13 | 1.4–1.7 | Full garment and textile lock |
| CONT-05 + CONT-09 + CONT-14 | 2.4–2.85 | Complete subject identity lock |
| CONT-03 + CONT-02 + CONT-19 | 2.35–2.75 | Full lighting and color coherence |
| CONT-04 + CONT-16 | 1.55–1.85 | Complete environmental atmosphere |
| CONT-08 + CONT-18 | 1.6–1.9 | Full scene geometry and scale |
| CONT-10 + CONT-11 + CONT-20 | 2.5–2.85 | Narrative arc completeness |

---

## Usage Protocol

1. **Identify the narrative type** (wedding, birthday, travel day, fashion shoot, documentary)
2. **Select identity tokens** (CONT-05, CONT-09, CONT-10, CONT-14) — always apply to primary subjects
3. **Select environmental tokens** (CONT-02, CONT-03, CONT-04, CONT-16, CONT-19) — apply to all frames
4. **Select wardrobe tokens** (CONT-01, CONT-13) — apply to all frames
5. **Select scene tokens** (CONT-06, CONT-08, CONT-18) — apply when scene geography matters
6. **Select narrative tokens** (CONT-11, CONT-20) — apply at prompt level
7. **Set weights** — 0.8–0.95 for strict continuity, 0.6–0.8 for natural variation within bounds
8. **Review final frame** — ensure CONT-20 (resolution) is appropriate for narrative type

---

## Anti-AI Detection Note

This system produces image sets with the following authentic photography markers:

- **Persistent subject identity** across all frames (same face, same body)
- **Garment lock** — clothes don't change mid-event
- **Unified color temperature** — all frames share a film stock / editing style
- **Consistent time-of-day lighting** — same sun position and quality
- **Narrative arc** — beginning, middle, and natural conclusion
- **Object persistence** — props and personal items remain present
- **Spatial coherence** — scene geography doesn't contradict itself

These are exactly the markers that AI-generated sets most commonly lack. Applying this system makes generated sets read as authentically photographed documentation rather than stochastic AI sampling.
