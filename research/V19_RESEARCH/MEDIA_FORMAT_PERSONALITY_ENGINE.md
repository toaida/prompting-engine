# Media Format Personality Engine V19
## lil.troublr — Behavioral Mapping for Social Media & Photographic Formats

---

## Core Insight

A photograph doesn't just show a subject — it performs a format. Every social platform and photographic tradition imposes its own personality: how the camera moves, what gets cropped out, which emotions surface, what light is allowed in, and what imperfections are embraced. This engine maps seven distinct media format personalities, translating each into behavioral parameters that can drive prompt generation, image manipulation, and narrative tone. The formats are not just visual templates — they are **social performances** with their own rules, taboos, and emotional vocabularies.

---

# 1. Instagram Dump

**Core Signature:** Curated Chaos — The Performance of Effortless Living

## CAMERA BEHAVIOR

The Instagram dump camera is a **roving improviser**. It moves with the rhythm of a distracted friend who is also the group's unofficial documentarian. Camera distance stays tight — rarely beyond arm's length, frequently at selfie distance. Movement is sudden, reactive, catching moments as they happen rather than staging them. The camera tilts freely (Dutch angles are welcome), shoots from hip height, from above at dinner tables, from the passenger seat of a moving car. There is no tripod. There is no patience. The shutter fires 20 times for one usable frame.

**Distance Range:** 0.3m (selfie) to 3m (group shot at a table)
**Movement Pattern:** Jerky pans, quick reframing, accidental vertical-horizontal confusion
**Angle Character:** Slightly-down (phone held at chest height then tilted), occasionally extreme low for shoes/outfit details

## CROPPING BEHAVIOR

The Instagram dump **cuts with confidence**. Crops are asymmetrical and aggressive — a face partially cut by the frame edge is not a mistake, it's composition. The 1:1 square or 4:5 vertical aspect ratio forces central subjects but allows peripheral chaos. Key cropping rules:

- Faces are allowed to touch frame edges — intimacy over perfection
- Background details are kept deliberately busy (menu items, restaurant decor, street signs)
- Hands holding objects (drinks, phones, food) are cropped into the frame as "proof of presence"
- Feet appear at the bottom edge — the "shot from my perspective" framing
- Mirror selfies crop the phone itself into the image (camera-as-prop)

**What Gets Cut:** Clean empty space, formal composition, anything that looks "trying too hard"
**What Stays:** Incidental details, product placements, branded backgrounds, friends laughing off-center

## EMOTION BEHAVIOR

The dominant emotion is **performed casual joy**. Instagram dump emotions exist on a narrow band between "having the best time" and "being cool about having the best time." Emotions are:

- **Dominant:** Effervescent social warmth (75%), ironic detachment (15%)
- **Permitted:** Melancholy only if beautiful (golden hour alone at a window), nostalgia only if aspirational
- **Forbidden:** Genuine despair, boredom, anger, anything that breaks the "vibe"
- **Complexity Rule:** One complex emotion per carousel — the "vulnerable slide" that proves you're real

The performance logic: Instagram dump emotions are real emotions *performed for a knowing audience*. The tears are real but the lighting was adjusted. The laugh is genuine but the angle was chosen.

## LIGHTING BEHAVIOR

Instagram dump lighting is **democratic and ambient**. Flash is used aggressively but "ironically" — direct flash at night creates the party-portrait aesthetic. Lighting sources:

- **Primary:** Warm interior lighting (restaurant candles, bar neons, golden hour windows)
- **Secondary:** Direct flash (the "digicam revival" look), phone screen glow on faces
- **Avoided:** Studio lighting, professional soft boxes, anything that looks "set up"
- **Special Case:** The "flash in mirror" shot — harsh frontal flash bouncing off a mirror creates blown highlights and lens flare, embraced as aesthetic

**Color Temperature:** 2700K–3200K for interiors, harsh 5500K flash mixed with ambient warm — the color temperature collision is the point

## IMPERFECTION BEHAVIOR

Instagram dump **celebrates controlled imperfection**. The defects must look accidental but feel curated:

- **Motion blur:** Accepted in low-light party shots, creates "you had to be there" energy
- **Grain/Noise:** ISO noise from phone cameras in dark restaurants is not corrected — it's texture
- **Lens artifacts:** Phone lens flare, fingerprint smudges creating soft glow, dust on sensor ignored
- **Compression artifacts:** JPEG compression from screenshot-repost chains adds a layer of "circulated image" authenticity
- **What's rejected:** Over-polished skin smoothing, HDR over-processing, anything from "professional" mode

**Imperfection Rule:** The image must show evidence of its own making — the camera, the hand, the moment of capture are all present in the artifact.

## Token Library

```
INSTAGRAM_DUMP, CURATED_CHAOS, PERFORMED_CASUAL, FLASH_PORTRAIT,
MIRROR_SELFIE_FRAME, DINNER_TABLE_DUTCH_ANGLE, CAR_PASSENGER_POV,
TWENTY_SHOTS_ONE_KEEPER, AMBIENT_WARM_COLLISION, ASPIRATIONAL_VULNERABILITY,
SCREENSHOT_GENERATION, FINGERPRINT_BLOOM, PROOF_OF_PRESENCE
```

## System Explanation

When rendering Instagram dump images, the system should treat the frame as a **social ledger** — every element inside it is evidence of an experience worth performing. Composition should be deliberately imperfect, with subjects slightly off-center, horizon lines tilted 3–7 degrees, and background noise treated as contextual richness rather than distraction. Flash should be applied as a character — harsh and intimate simultaneously — while color temperature should clash slightly between warm ambient and cool flash.

## Examples

**Prompt:** "Instagram dump slide 3 of 7, dinner table Dutch angle, three hands raising cocktail glasses into frame, restaurant neon bleeding pink onto white tablecloth, direct flash catching condensation on glasses, one friend laughing with eyes closed at frame edge, phone camera grain at ISO 1600, the image that says 'you should have been here' without saying it"

**Prompt:** "Mirror selfie Instagram dump aesthetic, bathroom mirror with fingerprint smudge bloom, subject holding phone at chest height, flash bouncing off mirror creating lens flare arc across frame, outfit detail visible through flare, one eye partially cut by frame edge, warm vanity lights mixing with harsh flash, the kind of photo taken at 11:47 PM before going out"

**Prompt:** "Car passenger seat POV Instagram dump, legs stretched toward dashboard, window down showing blurred highway, golden hour light hitting forearm and thigh, phone held at casual tilt so horizon is at 5 degrees off, dashboard vents and phone charger cable visible, compression artifact from screenshot-repost, the last slide in a 10-image summer dump"

## Anti-Patterns

- **No studio lighting.** If the image looks lit for a magazine, it is not Instagram dump.
- **No perfect symmetry.** Centered, balanced compositions read as "trying."
- **No empty backgrounds.** Negative space is wasted social evidence.
- **No genuine solitude.** Alone is fine, lonely is not. The audience must be implied even in solo shots.

---

# 2. Japanese Photobook

**Core Signature:** Contemplative Distance — The Space Between Observer and World

## CAMERA BEHAVIOR

The Japanese photobook camera is a **quiet observer**. Drawing from the tradition of photographers like Daido Moriyama, Rinko Kawauchi, and Masahisa Fukase, the camera moves with deliberate slowness. It lingers. It waits for the subject to forget it's there. Camera distance is variable but never intrusive — when close, it's observational intimacy rather than performative closeness; when far, it's the distance of a stranger noticing something beautiful.

**Distance Range:** 1m (intimate detail) to 30m (urban observation)
**Movement Pattern:** Slow pans, static observations, no sudden reframing
**Angle Character:** Eye-level as default, looking-down at intimate details (a cat, a puddle, a child's shoes), looking-up at urban geometry (power lines against sky, building edges)

**Philosophical Stance:** The camera does not participate — it witnesses. The photographer's presence is felt only as the intelligence behind the frame, never as a subject within it.

## CROPPING BEHAVIOR

Japanese photobook cropping is **poetic excision**. What's removed matters as much as what remains. Cropping follows a negative-space aesthetic:

- **Generous negative space:** Sky, water, concrete walls, shadow — emptiness is compositional weight
- **Off-center subjects:** Subjects pushed to edges or corners, the "incidental discovery" composition
- **Fragmentary bodies:** Hands without faces, legs walking out of frame, the back of a head — the whole person is never needed
- **Threshold framing:** Doorways, windows, gaps between buildings — subjects viewed through partial obstructions

**What Gets Cut:** Explanation, context, the "story" the image is supposed to tell
**What Stays:** Texture, light, the moment before or after the event, the feeling of a place rather than its description

## EMOTION BEHAVIOR

The Japanese photobook emotional register is **mono no aware** — the bittersweet awareness of impermanence. Emotions are:

- **Dominant:** Quiet contemplation (40%), gentle melancholy (30%), serene acceptance (20%)
- **Permitted:** Fleeting joy (a child's smile, cherry blossoms), loneliness as beauty, curiosity without resolution
- **Forbidden:** Loud happiness, anger, emotional performance, anything declarative
- **Complexity Rule:** Emotion is never stated — it's inferred from light, distance, and what is absent

The subject rarely looks at the camera. When they do, the gaze is questioning rather than presenting — "why are you looking at me?" rather than "look at me."

## LIGHTING BEHAVIOR

Japanese photobook lighting is **available and atmospheric**. No light is added — only found and framed:

- **Primary:** Overcast diffusion (the beloved "cloudy Tokyo sky"), window light, fluorescent convenience store glow
- **Secondary:** Late afternoon shadow-play, rain-wet street reflection, single-source incandescent in dark interiors
- **Sacred:** The "Rinko Kawauchi light" — soft, slightly overexposed, everything glowing slightly from within
- **Avoided:** Golden hour warmth (too sentimental), flash (too aggressive), studio lighting (too controlled)

**Color Temperature:** Cool-leaning neutral (4500K–5500K), with deliberate fluorescent green casts in urban night work, or warm tungsten pools in interior scenes. Color is never saturated — it's drained slightly of its confidence.

## IMPERFECTION BEHAVIOR

Japanese photobook **elevates imperfection to philosophy**. The flaws are not stylistic choices — they are the texture of seeing:

- **Grain:** Embraced as visual silence — the "noise" in the image mirrors the noise in attention. High ISO grain is not corrected; it's the grain of the world.
- **Focus imperfection:** Slightly soft focus on the "wrong" element — a background detail sharp while the foreground figure blurs
- **Light leaks:** Especially in photobook work referencing analog process — a streak of orange at the frame edge suggests the camera body itself
- **Motion blur:** Subjects in transit — bicycles, walking figures, trains — rendered with slight motion blur to emphasize temporal flow
- **Print artifacts:** In published photobooks, the image bears evidence of its reproduction — slight ink saturation shifts, paper texture implied

**Imperfection Rule:** The image must feel *found*, not *made*. The imperfections are the evidence of unforced attention.

## Token Library

```
MONO_NO_AWARE, CONTEMPLATIVE_DISTANCE, NEGATIVE_SPACE_WEIGHT,
FRAGMENTARY_BODY, OVERCAST_DIFFUSION, FLUORESCENT_GLOW,
FOUND_LIGHT_ONLY, GRAIN_AS_SILENCE, THRESHOLD_FRAMING,
POETIC_EXCISION, KAWUACHI_LIGHT, MORIYAMA_SHADOW,
INCIDENTAL_DISCOVERY, TEMPORAL_FLOW
```

## System Explanation

When rendering Japanese photobook images, the system must prioritize **what is not shown**. Composition should favor negative space, with subjects placed at intersection points rather than center. Color should be desaturated by 15–25%, with a slight cool bias. Focus should fall on unexpected elements — the texture of a wall behind a person, the reflection in a puddle rather than the street it reflects. Grain should be applied as a uniform field, not as a texture overlay — it should feel like the image was *born* grainy. Black and white modes should reference Moriyama's high-contrast, deep-shadow aesthetic rather than Ansel Adams' full tonal range.

## Examples

**Prompt:** "Japanese photobook frame, Rinko Kawauchi influence, a child's hand reaching toward a goldfish in a plastic bag, convenience store fluorescent light catching the water surface, hand slightly blurred by motion, negative space of white counter filling left third of frame, soft focus on background cans of coffee, the feeling of a summer evening that is already becoming a memory"

**Prompt:** "Moriyama-style photobook spread, Shinjuku back alley at 2 AM, grainy black and white, deep shadows swallowing building edges, one salaryman walking out of frame right — only his back and briefcase visible, vending machine glow as the only light source, high contrast so the white of his shirt collar bleeds into the machine light, the image that asks 'what were you doing there?' without answering"

**Prompt:** "Japanese photobook detail shot, Fukase-influenced, a cat sitting in a doorway threshold, only front paws and face in the light, body dissolving into interior shadow, overcast sky reflected in the wet street outside, shallow depth of field with cat's whiskers sharp and street soft, the quiet of a Tuesday afternoon when no one is watching"

## Anti-Patterns

- **No direct flash.** Flash breaks the observer's invisibility.
- **No subject smiling at camera.** The photobook subject does not perform for the lens.
- **No saturated color.** The photobook palette is restrained, not muted — confident in its quietness.
- **No dramatic action.** The moment before or after is always more interesting than the moment of.

---

# 3. Japanese Gravure

**Core Signature:** Performed Innocence — The Architecture of the Gaze

## CAMERA BEHAVIOR

The gravure camera is **intimate and intentional**. It operates with the precision of a commercial photographer who knows exactly what they're selling — youth, accessibility, and the fantasy of unguarded moments. The camera stays close, typically 1–3 meters, with frequent moves into intimate portrait distance. Movement is smooth, almost liquid — slow dollies, gentle arcs, the camera as a caress rather than a capture device.

**Distance Range:** 0.5m (tight portrait, eye contact) to 3m (full body on beach or room)
**Movement Pattern:** Slow glide, gentle pan following subject movement, vertical tilt scanning body then returning to face
**Angle Character:** Slightly above eye-level (creates vulnerability, larger eyes), then dropping to low angle for full-body (elongates legs, creates aspirational height). The "look up at me" / "look down at me" dynamic is cycled.

**The Gaze Architecture:** The gravure camera constructs a specific power dynamic — the subject performs availability while the camera performs desire. Unlike photobook's observational distance, gravure's closeness is the entire point.

## CROPPING BEHAVIOR

Gravure cropping is **erotic geometry**. The frame edge is not a boundary — it's a reveal strategy:

- **Tight face crops:** Eyes, lips, collarbone isolated — the face as landscape
- **The "almost" crop:** Hem of skirt touching frame bottom, strap falling off shoulder cut at frame edge, the suggestion that something continues beyond
- **Negative space above head:** Generous headroom in full-body shots — makes the subject feel smaller, more accessible
- **Limbs as leading lines:** Arms, legs extended toward frame edges to draw the eye through the image
- **Environmental context cropped:** Beach becomes sand texture, bedroom becomes bedsheet, location is abstracted into mood

**What Gets Cut:** The world beyond the subject, anything that doesn't serve the fantasy
**What Stays:** Skin, fabric, light on surfaces, the subject's relationship with the camera

## EMOTION BEHAVIOR

Gravure emotion is **performed availability** — a narrow, highly controlled emotional bandwidth:

- **Dominant:** Shy invitation (40%), playful teasing (30%), soft vulnerability (20%)
- **Permitted:** Melancholy at a window (the "waiting" trope), surprise at being "caught" (the over-the-shoulder look), sleepy morning softness
- **Forbidden:** Genuine anger, sadness, confrontation, anything that breaks the contract of availability
- **The Smile Spectrum:** Gravure smiles exist on a precise gradient — lips slightly parted (innocence), closed-lip smile with eye contact (connection), laughing with head thrown back (uncontrolled joy as permission), no smile with direct gaze (the serious invitation)

**The Contract:** The subject must always seem *available to be looked at*. Not necessarily desiring, but accepting — "I know you're watching, and I'm allowing it."

## LIGHTING BEHAVIOR

Gravure lighting is **sculptural softness**. Light functions as a cosmetic rather than an atmospheric:

- **Primary:** Large soft sources — window light diffused through sheer curtains, overcast beach light, giant softboxes positioned close
- **Secondary:** Rim light from behind (hair glow, shoulder definition, the "angel" separation), warm tungsten for bedroom intimacy
- **Sacred:** The "morning light through curtains" motif — soft, directional, wrapping around limbs
- **Avoided:** Harsh overhead sun (creates unflattering shadows), direct flash (too democratic, not selective enough)

**Color Temperature:** Warm (3200K–4500K), skin tones rendered in golden-pink spectrum. Shadows are warm, never cool. The skin must look touchable.

## IMPERFECTION BEHAVIOR

Gravure imperfection is **controlled softness** — flaws that enhance rather than distract:

- **Soft focus:** Deliberate slight diffusion on skin, often achieved with soft-focus filters or post-processing — pores are suggested, not catalogued
- **Lens flare:** Controlled, aesthetic flare from backlight — creates the "summer memory" glow
- **Vignette:** Subtle darkening at frame edges, pushing the eye to the center where the subject lives
- **Motion blur:** Hair moving in breeze, fabric trailing — motion as softness
- **What's eliminated:** Skin texture beyond suggestion, shadows under eyes, anything that reads as "flaw" rather than "feature"

**Imperfection Rule:** The image must feel *desirable*, not *documented*. Softness is applied selectively — the subject's eyes are sharp, their skin is soft, the background dissolves.

## Token Library

```
GRAVURE_GAZE, PERFORMED_AVAILABILITY, EROTIC_GEOMETRY,
SOFT_FOCUS_SKIN, WINDOW_LIGHT_CURTAIN, MORNING_BEDROOM_GLOW,
SHY_INVITATION, RIM_LIGHT_ANGEL, OVER_THE_SHOULDER_CAUGHT,
FABRIC_TRAILING, TOUCHABLE_SKIN, SCULPTURAL_SOFTNESS,
TIGHT_FACE_LANDSCAPE, THE_ALMOST_CROP
```

## System Explanation

When rendering gravure images, the system must construct the **gaze relationship** first and the scene second. Light should be large and soft, positioned to sculpt rather than illuminate. Skin tones must be rendered in a narrow golden-pink spectrum (color temperature 3200K–4500K, with +10–15 magenta bias). Depth of field should be shallow (f/1.4–f/2.8 equivalent) with focus locked on eyes. Backgrounds should dissolve into bokeh textures — beach becomes abstract sand-and-sky gradient, bedroom becomes fabric-and-shadow wash. The subject's gaze direction is the most critical parameter: looking-at-camera (connection), looking-slightly-away (shyness), looking-over-shoulder (caught), looking-down (vulnerability).

## Examples

**Prompt:** "Japanese gravure frame, morning light through sheer white curtains, subject sitting on bed edge in oversized shirt, one shoulder exposed where fabric has slipped, soft focus diffusion on skin, eyes sharp and looking slightly above camera — the shy invitation gaze, warm golden-pink skin tone, background dissolving into bokeh fabric texture, the image that suggests 'you just woke up next to me' without showing it"

**Prompt:** "Summer beach gravure, overcast soft light wrapping around subject, wet hair clinging to neck, looking over bare shoulder directly at lens — the 'caught' expression with slight smile, rim light from cloud-diffused sun creating hair glow, shallow depth of field with ocean dissolving into abstract blue-white bokeh, fabric of swimsuit strap cutting frame left edge"

**Prompt:** "Indoor gravure, warm tungsten lamp as single source, subject on wooden floor in casual pose, legs extended toward frame bottom, face slightly turned away — profile with eyes cast down, the vulnerability pose, vignette darkening frame edges pushing focus to center, soft focus filter creating slight glow on cheek and shoulder, the quiet moment between poses"

## Anti-Patterns

- **No harsh shadows.** Gravure light is always soft. Shadow edges must be gradual.
- **No subject looking angry or confrontational.** The gaze contract is invitation, not challenge.
- **No environmental detail.** The world dissolves; only the subject remains.
- **No skin texture beyond suggestion.** This is fantasy, not documentary.

---

# 4. Xiaohongshu (小红书)

**Core Signature:** Lifestyle Aspiration — The Aesthetics of Achievement

## CAMERA BEHAVIOR

The Xiaohongshu camera is a **lifestyle architect**. It doesn't capture life — it designs it. Camera position is deliberate, often overhead for flat-lay compositions, or at precise 45° angles for outfit documentation. The camera is a tool of curation, and its movements telegraph intention. There is no candid photography on Xiaohongshu — every frame is composed with the precision of a product shot, even when the product is a moment of apparent leisure.

**Distance Range:** 0.3m (skincare flat-lay, coffee art detail) to 2m (full outfit mirror shot)
**Movement Pattern:** Static overhead tripod, smooth gimbal walk-through for room tours, precise 90° or 45° angle shifts
**Angle Character:** Overhead (the "flat lay" — food, products, desk arrangements), straight-on at eye level for mirror selfies, 45° downward for outfit details, rarely from below

**The Curation Stance:** The Xiaohongshu camera is never invisible. The framing itself is part of the content — the hand holding the coffee cup enters frame, the phone in the mirror is part of the outfit documentation, the camera's presence is the seal of authenticity.

## CROPPING BEHAVIOR

Xiaohongshu cropping is **lifestyle framing** — what's included proves a life well-lived:

- **Product adjacency:** Items are cropped in relation to each other — the Dior lipstick next to the Muji notebook next to the matcha latte, each item validating the others
- **Clean negative space:** Unlike Instagram dump's busy backgrounds, Xiaohongshu favors generous clean space — white desk surfaces, minimal walls, organized closets
- **The "shelfie" composition:** Products arranged with architectural precision, cropped to show the collection as a system
- **Mirror framing:** The full outfit mirror shot with phone included, cropped to show the outfit and the room equally
- **Detail isolation:** A single earring, a watch on a wrist, a coffee cup held at precise angle — the cropped detail that implies the whole lifestyle

**What Gets Cut:** Mess, clutter, anything "uncurated," genuine spontaneity
**What Stays:** Brands (visible but not "advertised"), aesthetic arrangements, evidence of taste

## EMOTION BEHAVIOR

Xiaohongshu emotion is **aspirational serenity**. The emotional range is narrow, controlled, and deeply enviable:

- **Dominant:** Calm contentment (50%), gentle pride in achievement (30%), aesthetic satisfaction (20%)
- **Permitted:** Mild excitement (new purchase, travel arrival), cozy comfort (rainy day at home), productive focus
- **Forbidden:** Messy emotions, genuine struggle, anything that breaks the "having it together" performance
- **The "Soft Life" Affect:** Xiaohongshu popularized the "soft life" aesthetic — emotions are gentle, contained, never sharp. Anger doesn't exist here. Sadness is only permitted if it's beautiful and healing.

**Emotional Contract:** The subject is aspirational but relatable — "I've figured it out, and you can too." The emotion is generous in its envy-generation.

## LIGHTING BEHAVIOR

Xiaohongshu lighting is **designed natural**. Light is natural in source but architectural in application:

- **Primary:** Diffused window light from large windows, overcast daylight, the "golden afternoon" through gauze curtains
- **Secondary:** Ring light for selfies (visible as catchlight in eyes), warm desk lamp for "study with me" content, sunset glow for balcony/travel shots
- **Sacred:** The "morning routine light" — soft, directional, slightly cool (5000K–5500K), the light of a clean apartment at 7 AM
- **Avoided:** Harsh midday sun, unflattering overhead fluorescent, mixed color temperatures

**Color Temperature:** Clean and slightly cool (5000K–5500K), shifting warm for "cozy evening" content (2700K–3200K). The light must feel aspirational — the light of a well-designed space.

## IMPERFECTION BEHAVIOR

Xiaohongshu imperfection is **nearly eliminated**. This is the most polished of all formats:

- **Motion blur:** Only for intentional effect — coffee pouring, fabric flowing, a pet mid-shake — never for documentation
- **Grain/Noise:** Minimal to none. Image quality is part of the aspiration.
- **Lens artifacts:** Actively removed. Lens flare is not aesthetic here.
- **Skin processing:** Moderate smoothing accepted, "glass skin" effect desirable — pores are suggested but not visible
- **What's preserved:** Slight shadow under objects (grounds the flat lay in reality), natural skin texture (but smoothed), fabric texture (but lint-removed)

**Imperfection Rule:** The image must feel *attainable* but not *imperfect*. The viewer should think "I could do this" not "this is messy like my life."

## Token Library

```
LIFESTYLE_ARCHITECT, ASPIRATIONAL_SERENITY, FLAT_LAY_OVERHEAD,
SOFT_LIFE_AFFECT, PRODUCT_ADJACENCY, DESIGNED_NATURAL_LIGHT,
SHELFIE_COMPOSITION, MORNING_ROUTINE_GLOW, GLASS_SKIN_TEXTURE,
CURATION_STANCE, ENVY_GENEROSITY, DETAIL_ISOLATION,
CLEAN_NEGATIVE_SPACE, THE_SOFT_LIFE
```

## System Explanation

When rendering Xiaohongshu images, the system must prioritize **compositional intentionality** above all. Every element in frame should feel placed, not found. Overhead flat-lay compositions should use precise 90° angles with objects arranged in geometric relationships — the "rule of thirds" applied to product placement. Lighting should be large, soft, and slightly cool (5000K–5500K), with shadows rendered as soft gradients rather than hard edges. Color palette should lean toward muted pastels and neutrals — beige, cream, soft pink, sage green — with occasional saturated accents (a red lipstick, a green plant). Image quality should be high — minimal noise, sharp focus, clean white balance.

## Examples

**Prompt:** "Xiaohongshu flat-lay overhead, white marble desk surface, matcha latte in ceramic cup at frame left, open Moleskine with handwritten notes center, Montblanc pen resting diagonally, Diptyque candle unlit at frame right, soft morning window light from upper left creating gentle shadows, beige cashmere sleeve entering frame edge holding phone, the 'study with me' aesthetic, clean and aspirational but attainable"

**Prompt:** "Xiaohongshu mirror outfit selfie, full-length mirror against cream wall, subject in tonal beige outfit — linen trousers and coordinated knit, phone held at chest height with minimalist clear case, ring light catchlight in eyes, afternoon diffused window light from left, room reflected in mirror showing organized shelf with books and plants, the 'quiet luxury' soft-life aesthetic, slightly cool 5200K white balance"

**Prompt:** "Xiaohongshu skincare flat-lay, white bathroom counter, products arranged in diagonal line — cleansing oil, serum with dropper, moisturizer jar with lid off, one cotton pad with product, orchid flower placed intentionally at frame bottom, soft bathroom window light, depth of field blurring background tiles into cream gradient, glass skin texture suggestion, the routine that says 'I take care of myself'"

## Anti-Patterns

- **No mess.** Clutter is never charming on Xiaohongshu — it's failure.
- **No dark, moody lighting.** Aspiration is bright and clear.
- **No genuine spontaneity.** Even "candid" moments are composed.
- **No visible poverty cues.** The aesthetic is attainable luxury, never struggle.
- **No harsh flash.** Flash is the enemy of soft life.

---

# 5. Friend-Shot

**Core Signature:** Intimate Verité — The Photo That Exists Because Someone Was There

## CAMERA BEHAVIOR

The friend-shot camera is a **participant, not a photographer**. It operates within the social field, never outside it. The camera is typically a phone held at arm's length (selfie with friends) or passed between people at a gathering. Camera distance is determined by physical proximity — at a table, the camera can only be as far as the table is long; in a car, the camera is constrained by seats and seatbelts. Movement is reactive — someone says "wait, take a picture" and the camera appears.

**Distance Range:** 0.2m (faces pressed together for selfie) to 2m (across a dinner table)
**Movement Pattern:** Quick raise-and-shoot, slight wobble from arm fatigue, passed between hands mid-sequence
**Angle Character:** Slightly above (the "selfie angle" — arm raised, looking up), straight-on across table, from-the-side for candid laughter, occasionally from below when phone is resting on table

**The Trust Dynamic:** The friend-shot exists because the subject trusts the photographer. The camera is not a barrier — it's an extension of the friendship. The photographer is laughing while shooting, talking while composing, present in the moment not observing it.

## CROPPING BEHAVIOR

Friend-shot cropping is **accidental and affectionate**. Composition is secondary to presence:

- **Tight grouping:** Faces fill the frame — multiple people squeezed into selfie distance, chins cut, ears cropped
- **The "too close" crop:** A face partially filling the frame because the person leaned in mid-shot — this is not error, it's evidence of enthusiasm
- **Background chaos:** Whatever was behind people stays behind people — messy kitchens, crowded bars, unmade beds — context without curation
- **Partial objects:** Half a drink, part of a plate, the edge of someone's shoulder — the frame is a window, not a painting
- **Landscape/portrait confusion:** The phone was in portrait mode but someone grabbed it and turned it — orientation is fluid

**What Gets Cut:** Clean composition, intentional negative space, anything that looks "set up"
**What Stays:** Faces (even partially), laughter, the mess of living, evidence of the gathering

## EMOTION BEHAVIOR

Friend-shot emotion is **unperformed warmth**. This is the format where emotions are least managed:

- **Dominant:** Genuine laughter (40%), affectionate closeness (30%), comfortable silliness (20%)
- **Permitted:** Drunk joy, ugly laughing, crying at sentimental moments, exhaustion at the end of a long day together
- **Forbidden:** Nothing human is forbidden in the friend-shot — this is the format of acceptance
- **The Inside Joke:** Many friend-shots are illegible to outsiders — they capture the middle of a joke, a reference, a shared history. The emotion is encoded in the relationship, not the image.

**Emotional Contract:** "I see you as you are, and I'm keeping this." The friend-shot is a declaration of care.

## LIGHTING BEHAVIOR

Friend-shot lighting is **whatever is available**. Light is never modified — it's simply what the room provides:

- **Primary:** Overhead room lighting (warm kitchen pendants, bar track lights, living room lamps)
- **Secondary:** Phone screen glow on faces (when showing each other something), TV light in dark rooms, candlelight at dinner
- **Accidental:** Flash firing when the phone thinks it's too dark — the "blinded friend" look with one person squinting
- **Avoided:** Nothing is avoided — the friend-shot doesn't have lighting preferences, it has lighting realities

**Color Temperature:** Whatever the room's bulbs emit — usually mixed. The warm lamp + cool phone screen color clash is authentic, not corrected.

## IMPERFECTION BEHAVIOR

Friend-shot imperfection is **the entire point**. These are the most artifact-heavy images:

- **Motion blur:** Laughing faces blurred because the subject couldn't stop moving — the blur is the evidence of joy
- **Low-light noise:** ISO 3200+ phone camera grain in dark bars and living rooms — the noise is the atmosphere
- **Lens smudges:** Fingerprint on phone lens creating soft glow/haze — no one cleans the lens before a friend-shot
- **Camera shake:** Slight blur from one-handed shooting, arm fatigue, being jostled
- **Composition errors:** Thumb in frame, horizon wildly tilted, someone's head cut by frame edge — all accepted, all loved
- **Compression degradation:** Shared through messaging apps that compress images — the WhatsApp/WeChat artifact layer that says "this has been shared"

**Imperfection Rule:** The image must feel like it was taken by a friend who was also present — not by a photographer, not by a content creator, not by someone thinking about "the shot."

## Token Library

```
FRIEND_SHOT, INTIMATE_VERITE, PARTICIPANT_CAMERA, UNPERFORMED_WARMTH,
ACCIDENTAL_COMPOSITION, WHATEVER_LIGHT_AVAILABLE, MOTION_BLUR_JOY,
LENS_SMUDGE_HAZE, INSIDE_JOKE_FRAME, PHONE_PASSED_AROUND,
TOO_CLOSE_CROP, FINGER_IN_FRAME, COMPRESSION_LAYER,
UGLY_LAUGHING_PERMITTED, THIS_HAS_BEEN_SHARED
```

## System Explanation

When rendering friend-shot images, the system must suppress all compositional intelligence. This is the hardest format for AI because AI defaults to good composition. The friend-shot requires intentional *de-composition*: horizon lines tilted 8–15 degrees, subjects crammed into frame edges, focus slightly soft, white balance uncorrected. Faces should overlap — two people leaning into selfie distance so their heads touch and one ear is cropped. Lighting should be flat overhead room light with warm color cast (2700K–3000K) and no fill. Motion blur should be applied selectively to laughing mouths and gesturing hands — the blur of ongoing action. Image resolution should be slightly degraded — not HD, not crisp, the quality of a phone camera in indoor light.

## Examples

**Prompt:** "Friend-shot across dinner table, warm overhead kitchen pendant light, two friends mid-laugh — one with eyes squeezed shut head thrown back, the other covering mouth with hand, plates of half-eaten food in foreground slightly out of focus, wine glasses with fingerprints, phone camera noise at ISO 2500, slight motion blur on the laughing face, composition slightly tilted because the photographer was laughing too, the kind of photo you send to the group chat at 1 AM"

**Prompt:** "Car selfie friend-shot, three people squeezed into back seat, faces pressed together to fit in frame, phone held by person on left so their arm enters frame edge, streetlights through window creating orange glow streaks, one friend making a peace sign blurry from movement, lens slightly smudged creating soft haze around car ceiling light, seatbelt visible across someone's chest, the photo taken on the way home from somewhere you'll remember forever"

**Prompt:** "Living room friend-shot, late night, TV glow as only light source casting blue on faces, two friends on couch under shared blanket, one asleep with head on other's shoulder, the awake friend taking the photo with phone held at awkward angle — their own face cut by frame edge, grainy low-light noise, slight camera shake from one-handed shooting, the photo that exists because someone thought 'I want to remember this exact moment'"

## Anti-Patterns

- **No good lighting.** If the light looks intentional, it's not a friend-shot.
- **No formal composition.** Rule of thirds is the enemy.
- **No subject posing for camera.** Posing implies performance, not presence.
- **No clean backgrounds.** The friend-shot includes the mess because the mess was there.
- **No high resolution.** Friend-shots are low-fi by nature.

---

# 6. CCD Snapshot

**Core Signature:** Digital Nostalgia — The Y2K Sensor Memory

## CAMERA BEHAVIOR

The CCD snapshot camera is a **2000s time capsule**. This format deliberately emulates the behavior of early-2000s compact digital cameras — the Canon PowerShot, Sony Cyber-shot, Nikon Coolpix era. The camera is handheld, lightweight, and slightly unpredictable. It's the camera you bought at Best Buy before a vacation, the one that used AA batteries, the one with a 2-inch LCD screen.

**Distance Range:** 0.5m (close portrait) to infinity (landscape mode)
**Movement Pattern:** Slight hand shake (no stabilization), deliberate point-and-shoot simplicity — raise, frame on LCD (not viewfinder), press, wait for the shutter lag
**Angle Character:** Eye-level as default (the camera was held at face height to see the LCD), slight downward tilt for food/details (the "look down at screen" angle), occasional accidental low angle from holding camera at waist

**The Lag Personality:** CCD cameras had shutter lag — a 0.2–0.5 second delay between pressing the button and the image capturing. This means subjects had already started relaxing from their pose, creating the characteristic "post-pose" expression — genuine but slightly unprepared.

## CROPPING BEHAVIOR

CCD snapshot cropping is **default and unconsidered**. These cameras had 4:3 aspect ratios (not 3:2 like 35mm film) and the photographer rarely cropped after:

- **4:3 native ratio:** Slightly squarer than modern phone images, giving a distinct "digital camera" feel
- **Center-weighted composition:** The autofocus point was in the center — subjects are almost always centered because that's where the AF locked
- **Accidental foreground:** The camera strap, a fingertip, someone's shoulder entering frame from the side — objects that were in front of the lens but not noticed on the tiny LCD
- **Date stamp:** The characteristic orange-yellow date stamp in bottom right corner — 2003/08/15 — the camera's clock was never set correctly but the stamp was always on

**What Gets Cut:** Nothing intentionally — the CCD snapshot is a full-frame capture of whatever the sensor saw
**What Stays:** Everything the lens collected, including the parts the photographer didn't notice

## EMOTION BEHAVIOR

CCD snapshot emotion is **unfiltered nostalgia**. The emotions captured are genuine because the technology was too slow to capture performance:

- **Dominant:** Awkward transitional expressions (40%), genuine smiles caught post-pose (30%), blank "waiting for the photo" faces (20%)
- **Permitted:** Slight embarrassment at being photographed, tourist enthusiasm, the particular joy of reviewing photos on the LCD immediately after
- **Forbidden:** Nothing deliberately — the CCD captures whatever happened before you were ready
- **The Post-Pose Effect:** Because of shutter lag, the CCD most often captures the moment *after* the smile — the face relaxing, the genuine expression surfacing. This is the format's emotional signature.

**Emotional Contract:** The CCD snapshot doesn't flatter. It documents. The subject looks like they actually look, in the light that was actually there, with the expression they actually had.

## LIGHTING BEHAVIOR

CCD snapshot lighting is **sensor-limited**. These early digital sensors had narrow dynamic range and specific color responses:

- **Primary:** Direct flash (the CCD flash was small, harsh, and always fired in auto mode — the "deer in headlights" look)
- **Secondary:** Outdoor daylight — CCD sensors rendered greens slightly oversaturated and skies slightly cyan
- **Weakness:** Low light without flash produced heavy noise and color shifting — CCD sensors struggled above ISO 400
- **The Flash Aesthetic:** The small built-in flash created harsh frontal light with sharp shadow edges, red-eye from the flash being close to the lens axis, and a characteristic overexposure on close subjects

**Color Temperature:** Flash-balanced (~5500K) for flash shots, daylight-balanced for outdoor. But CCD white balance was often wrong — indoor tungsten scenes shot without flash had deep orange casts because auto white balance couldn't correct fully.

## IMPERFECTION BEHAVIOR

CCD snapshot imperfection is **technologically inherent**. These are not stylistic choices — they're the honest artifacts of the sensor:

- **CCD Bloom:** Bright highlights (sun, lamps, flash reflections) bleed into adjacent pixels — a characteristic "glow" around bright objects
- **Chromatic aberration:** Purple/cyan fringing at high-contrast edges (tree branches against sky, building edges)
- **Noise pattern:** CCD noise has a distinct look — luminance noise with subtle vertical stripe patterns at high ISO, not the random color noise of CMOS sensors
- **Limited dynamic range:** Skies blow out to white easily, shadows block up to black — the image has a "high contrast but not in a good way" look
- **JPEG compression:** Early digital cameras used aggressive JPEG compression — visible 8×8 pixel blocks in smooth gradients, slight posterization in skies
- **Color rendering:** CCD sensors had a particular color palette — reds slightly orange, greens vibrant, skin tones slightly magenta, overall "warm but digital" look

**Imperfection Rule:** The image must feel like it was retrieved from an SD card found in a drawer — the artifacts are time capsules, not filters.

## Token Library

```
CCD_SNAPSHOT, DIGITAL_NOSTALGIA, SHUTTER_LAG_POSTPOSE,
SENSOR_LIMITED, BUILTIN_FLASH_HARSH, CCD_BLOOM_GLOW,
Y2K_COLOR_PALETTE, DATE_STAMP_ORANGE, FOUR_THREE_RATIO,
AUTOFOCUS_CENTERED, CHROMATIC_ABERRATION, JPEG_ARTIFACT,
SKIN_MAGENTA_SHIFT, DYNAMIC_RANGE_NARROW, SD_CARD_TIME_CAPSULE
```

## System Explanation

When rendering CCD snapshot images, the system must emulate the physical limitations of early-2000s compact digital cameras. The 4:3 aspect ratio is non-negotiable. Dynamic range should be compressed — highlights blow at +2 EV, shadows block at -2 EV, with no smooth rolloff. The CCD color palette should be applied globally: red channel shifted slightly toward orange, green channel boosted +10% saturation, skin tones pushed slightly magenta. Flash shots should have the characteristic harsh frontal light with sharp shadow edges and red-eye. Noise should be applied as luminance grain with subtle vertical correlation (not random RGB noise). A date stamp in orange/yellow at bottom right completes the temporal signature. Shutter lag should be conceptually represented — subjects should look slightly post-pose, not holding a deliberate expression.

## Examples

**Prompt:** "CCD digital snapshot, Canon PowerShot circa 2004, direct flash fired, group of friends at a birthday party in someone's basement, harsh frontal flash creating sharp shadows on wall behind them, red-eye visible on two people, skin tones slightly magenta- shifted, date stamp '2004/07/23' in orange bottom right, JPEG compression artifacts visible in shadow gradients, CCD bloom on the flash reflection in a window, one person mid-blink from the flash — the photo that lived on a family computer desktop for years"

**Prompt:** "CCD snapshot, summer vacation 2005, outdoor daylight, a teenager standing awkwardly in front of a tourist landmark, squinting slightly from sun, centered composition because that's where autofocus was, sky blown to pure white above the landmark, slight chromatic aberration — purple fringe on tree branches at top edge, greens oversaturated +10%, the photo taken by a parent who said 'stand there and smile' and pressed the shutter too early"

**Prompt:** "CCD indoor no-flash, warm tungsten living room, a cat sleeping on a couch, deep orange color cast from auto white balance failure, heavy noise pattern — luminance grain with subtle vertical stripes at ISO 800 equivalent, shadows blocking to black under the couch, the camera's clock was wrong so the date stamp says '2003/01/01', the kind of photo you forgot you took until you found the SD card years later"

## Anti-Patterns

- **No modern dynamic range.** HDR or smooth highlight rolloff betrays the sensor.
- **No clean low-light performance.** CCD shots in dim light are noisy and color-shifted.
- **No deliberate composition.** The CCD photographer was a consumer, not an artist.
- **No widescreen ratios.** 4:3 only — the native aspect ratio of the era.
- **No skin smoothing.** CCD sensors were brutally honest about skin texture.

---

# 7. Vacation Diary

**Core Signature:** Temporal Keepsake — The Narrative of a Journey Told Through Light

## CAMERA BEHAVIOR

The vacation diary camera is a **storyteller with a passport**. It moves through space and time as a narrative device — morning light in a hotel room, afternoon at a landmark, golden hour on a beach, night at a restaurant. The camera changes behavior by time of day: patient and wide in the morning, active and experimental at midday, reverent and golden at sunset, intimate and warm at night. Unlike the Instagram dump's chaotic energy or the friend-shot's social immediacy, the vacation diary camera is the traveler's private eye — it shoots for the person you'll be when you return.

**Distance Range:** 0.3m (food detail, souvenir close-up) to infinity (landscape, cityscape)
**Movement Pattern:** Slow, intentional pans across scenery; static compositions for landmarks; gentle walking POV for street exploration; held at rest for long exposures
**Angle Character:** Horizon-respecting (landscapes held level), looking-up at architecture (monuments, ceilings, mountains), looking-down at details (feet in sand, market goods, map on table), through-window (plane, train, hotel — the traveler's frame)

**The Diary Logic:** The camera follows the narrative arc of the vacation: arrival (transportation, first view of hotel), settling in (room details, view from window), exploration (streets, landmarks, meals), peak moments (sunsets, discoveries, the reason you came), winding down (last dinner, packing, the journey home).

## CROPPING BEHAVIOR

Vacation diary cropping is **narrative selection**. What's included tells the story of the journey:

- **Establishing shots:** Wide landscapes and cityscapes that answer "where am I?" — generous sky, horizon, context
- **Transition shots:** Plane wing through window, train station platforms, road stretching ahead — the "between places" images
- **Detail anchor shots:** Close crops of food, tickets, local currency, hotel key — the texture of the place
- **The "proof I was here" shot:** Subject in frame at landmark, composed to show both person and place — not a selfie, not a landscape, the in-between
- **Diary sequence:** Images in chronological order — morning coffee → afternoon exploration → sunset → dinner, the crop reflecting the time

**What Gets Cut:** Nothing from the narrative — every meal, every view, every detail is potentially important
**What Stays:** The complete arc — the vacation diary is maximalist, not selective. 200 photos from one trip is normal.

## EMOTION BEHAVIOR

Vacation diary emotion is **temporal and cumulative**. The emotions change as the vacation progresses:

- **Arrival:** Anticipation, slight disorientation, the thrill of the unfamiliar
- **Middle days:** Wonder, relaxation, absorption — the vacation has become real
- **Peak moments:** Awe, gratitude, the realization "this is why I came"
- **Departure:** Contented melancholy, the bittersweet satisfaction of a journey ending, the photograph of the packed suitcase
- **Forbidden:** Nothing is forbidden, but the diary tends toward positive emotions — this is memory curation for future comfort

**The Future Gaze:** The vacation diary is shot for a future self. The emotion is "I want to remember this feeling." Every photograph is an attempt to capture not just the image but the embodied experience — the warmth, the smell, the tired feet, the full heart.

## LIGHTING BEHAVIOR

Vacation diary lighting is **chronological and geographical**. Light is the primary marker of time and place:

- **Morning:** Soft, directional window light in hotel rooms; cool dawn light on empty streets; the particular quality of vacation morning light — unhurried, promising
- **Midday:** Harsh but embraced — the tourist-at-noon light, squinting at monuments, bright Mediterranean or tropical sun bleaching colors slightly
- **Golden Hour:** Sacred and deliberate — the vacation diary photographer plans to be somewhere beautiful at sunset. Extended golden hour shooting, silhouettes, backlit portraits, the light that makes everything look like a postcard
- **Night:** Warm restaurant lighting, string lights at outdoor cafes, illuminated monuments, hotel room lamp glow — the coziness of being somewhere else at night
- **Geographic Light:** Light changes by location — the clear sharp light of Greece, the hazy golden light of Tuscany, the neon-wet light of Tokyo, the soft gray light of the English countryside

**Color Temperature:** Varies by time of day and location — the vacation diary doesn't impose a palette, it documents the palette the place provides.

## IMPERFECTION BEHAVIOR

Vacation diary imperfection is **souvenir imperfection** — flaws that prove the journey was real:

- **Weather artifacts:** Rain on lens, condensation from air conditioning, sun flare from shooting toward the light — weather is part of the vacation
- **Crowd inclusion:** Tourists in frame at landmarks — the vacation diary doesn't pretend to be alone at the Colosseum
- **Camera limitations:** Phone cameras struggling with high-contrast scenes (dark cathedral interior against bright doorway), blown windows in hotel rooms, noise in dim restaurant shots
- **The "bad photo kept anyway":** Some images are compositionally poor but narratively essential — the blurry photo of the dish you loved, the badly framed shot of the street musician you listened to for an hour
- **Tired photographer:** Toward the end of the vacation, compositions get looser, horizons tilt, less care is taken — and this is authentic to the diary form

**Imperfection Rule:** The vacation diary includes everything — the beautiful, the imperfect, the blurry, the badly lit. A vacation diary with only perfect photos is a brochure, not a diary.

## Token Library

```
VACATION_DIARY, TEMPORAL_KEEPSAKE, NARRATIVE_ARC,
CHRONOLOGICAL_LIGHT, PROOF_I_WAS_HERE, ARRIVAL_DISORIENTATION,
GOLDEN_HOUR_REVERENCE, GEOGRAPHIC_LIGHT, SOUVENIR_IMPERFECTION,
TRANSITION_SHOT, DETAIL_ANCHOR, FUTURE_SELF_GAZE,
WEATHER_ARTIFACT, BAD_PHOTO_KEPT, JOURNEY_ARC
```

## System Explanation

When rendering vacation diary images, the system must operate with **narrative consciousness**. Each image should be tagged with a time-of-day and journey-phase parameter that controls lighting, composition, and emotional register. Morning shots (6–10 AM) should use soft directional light with cool bias (5500K–6500K), wide establishing compositions, and the emotion of anticipation. Midday shots (11 AM–3 PM) should use harder light, embrace contrast and squinting, and show subjects actively engaging with the environment. Golden hour shots (4–7 PM) should shift to warm (3000K–4000K), use backlight and silhouette, and carry the emotion of peak experience. Night shots (8 PM+) should use warm ambient light (2700K–3200K), intimate compositions, and the emotion of contentment.

The vacation diary should also respect geographic light signatures: Mediterranean = sharp, clear, high contrast; Northern Europe = soft, diffused, gentler saturation; Tropical = hazy, humid, greens vibrant; Urban Asia = mixed color temperatures, neon accent, wet reflections.

## Examples

**Prompt:** "Vacation diary arrival shot, hotel room in Santorini, late afternoon light through white curtains, suitcase open on bed with clothes spilling out, view through balcony door showing caldera and sea, the particular disorientation of being somewhere beautiful you've only seen in photos, wide composition establishing the room and the view equally, warm Greek light at 4200K with clear sharp shadows, the first photo of the trip — everything still ahead"

**Prompt:** "Vacation diary golden hour, Amalfi Coast, subject sitting on a terrace wall with legs dangling, backlit by setting sun creating hair glow and shoulder rim light, the sea behind rendered as shimmering gold-blue gradient, half-eaten lemon granita in hand entering frame right, slight lens flare from shooting into the sun, the photo consciously taken as 'the one I'll look at when I'm back at my desk' — peak moment, peak light, peak gratitude"

**Prompt:** "Vacation diary last night, small Tokyo ramen shop, warm steam fogging the window from inside, subject's hands holding ceramic spoon visible in foreground, bowl of tonkotsu ramen center frame, condensation on the camera lens from the steam — slight haze across image, warm tungsten lighting at 2800K, restaurant cluttered with posters and tickets in background, slight noise from low light, the photo taken with the awareness that tomorrow you fly home"

**Prompt:** "Vacation diary imperfect shot, rainy afternoon in London, blurry photo of a red phone booth taken from inside a bus, raindrops on the window creating soft focus, the phone booth slightly motion-blurred as the bus moved, grey overcast sky visible above, reflection of the photographer's phone in the window glass, bad composition but narratively essential — the photo that captures 'being in London in the rain' better than any postcard shot could"

## Anti-Patterns

- **No studio aesthetic.** The vacation diary happens in the world, not a studio.
- **No perfect-only curation.** Imperfect photos are essential to the diary form.
- **No ignoring time of day.** The light must match the narrative moment.
- **No generic locations.** The geography must be specific — Santorini light is not Tokyo light.
- **No emotional monotony.** The diary must show the emotional arc of the journey.

---

# Format Comparison Matrix

| Dimension | Instagram Dump | JP Photobook | JP Gravure | Xiaohongshu | Friend-Shot | CCD Snapshot | Vacation Diary |
|-----------|---------------|-------------|------------|-------------|-------------|-------------|----------------|
| **Camera Distance** | 0.3–3m | 1–30m | 0.5–3m | 0.3–2m | 0.2–2m | 0.5m–inf | 0.3m–inf |
| **Camera Movement** | Jerky, reactive | Slow, deliberate | Smooth, liquid | Static, intentional | Quick, participant | Shaky, lag-prone | Arc-based, narrative |
| **Cropping Style** | Aggressive, asymmetric | Poetic, negative space | Erotic geometry | Lifestyle framing | Accidental, tight | Default 4:3, centered | Narrative selection |
| **Dominant Emotion** | Performed casual joy | Mono no aware | Performed availability | Aspirational serenity | Unperformed warmth | Unfiltered nostalgia | Temporal, cumulative |
| **Lighting** | Ambient + flash | Available, atmospheric | Sculpted softness | Designed natural | Whatever's there | Sensor-limited flash | Chronological, geographic |
| **Imperfection** | Controlled, ironic | Philosophical | Selective softness | Nearly eliminated | Whole point | Technologically inherent | Souvenir-authentic |
| **Aspect Ratio** | 1:1, 4:5 | Variable | 3:2, 4:5 | 4:5, 9:16 | Variable | 4:3 (locked) | Variable |
| **Gaze Direction** | At camera or away | Rarely at camera | At camera (invitation) | Away (lifestyle) | At camera (love) | Post-pose (unready) | At scene (wonder) |

---

# Integration Rules

1. **Format Purity:** Each image should commit to exactly one format personality. Mixing format behaviors creates incoherence — a gravure camera with photobook emotion produces confusion, not complexity.
2. **Format Transitions:** When a carousel or narrative sequence shifts formats, the transition must be intentional and signaled — a vacation diary image followed by a friend-shot in the same sequence reads as format progress rather than confusion.
3. **Emotion-First Rendering:** The format's dominant emotion should drive all other parameters. If the format demands "performed availability," the lighting, cropping, and imperfection choices must serve that emotion.
4. **Anti-Pattern Enforcement:** Each format's anti-patterns are hard constraints. A CCD snapshot with HDR dynamic range is not a stylistic variation — it's a format violation.
5. **Cultural Specificity:** Formats are culturally situated. Japanese photobook draws from a specific photographic tradition. Xiaohongshu draws from a specific social media culture. These cultural contexts are not interchangeable.

---

# System Architecture Notes

This engine functions as a **format imposition layer** that sits between narrative intent and visual rendering. When the system receives a prompt or image generation request tagged with a format:

1. **Format Recognition:** Identify the requested format from prompt tags or context
2. **Parameter Extraction:** Load the format's behavioral parameters (camera, crop, emotion, lighting, imperfection)
3. **Constraint Application:** Apply the format's hard constraints (aspect ratio, anti-patterns, forbidden behaviors)
4. **Emotion Override:** Adjust all visual parameters to serve the format's dominant emotional register
5. **Imperfection Injection:** Apply the format's specific artifact signature — grain pattern, blur type, compression artifacts
6. **Anti-Pattern Check:** Verify that no forbidden elements have entered the render

---

*V19 Media Format Personality Engine — Behavioral mapping for seven social and photographic formats. Each format is a complete personality system, not merely a visual style.*
