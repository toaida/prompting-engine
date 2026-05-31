# MEMORY_CAPTURE_SYSTEM.md
### AContent / lil.troublr V14.6 Core Module
### Human Memory Realism — Camera Imperfectly Remembering a Lived Moment

---

## WHY THIS SYSTEM EXISTS

AI image generators produce **optimized images**:

- Perfect centering
- Full anatomy in frame
- Sharp focus throughout
- Ideal composition
- Complete expressions
- Static perfection

Human memory captures **imperfect reconstructions**:

- Emotional timing prioritised over technical perfection
- Incomplete fragments
- Imperfect focus
- Distracted gaze
- Environmental interruption
- Timing-over-anatomy

The V14.6 engine shifts from "beautiful social realism" to **"emotionally remembered human-world realism"**.

The image should feel: recovered, interrupted, imperfectly captured, physically constrained, emotionally unfinished, socially believable, environmentally caused.

NOT: designed, optimized, glamour-framed, viewer-serving, pose-first.

---

## THE MEMORY ENCODING PRINCIPLE

Human memory prioritises:

1. **Emotional peak moment** — the exact heartbeat when something felt real
2. **Environmental texture** — what the room/light/air felt like, not the perfect angle
3. **Sensory fragment** — a specific detail that triggered the memory (wet fabric, cold tile, someone's laugh)
4. **Temporal position** — before/during/after a social moment, not perfectly on-moment
5. **Constraint acknowledgment** — what limited the shot (darkness, distance, movement)

When a camera genuinely captures a moment worth remembering:
- The moment is usually already passing
- Composition is secondary to preserving the feeling
- Imperfection is the signature of authenticity
- Incomplete framing means the photographer was inside the moment, not outside directing it

**Core principle:**
*"The photo exists because the photographer was moved. Not because the scene was set."*

---

## SYSTEM 1: INCOMPLETE FRAMING

### What AI Does
- Always keeps full anatomy in frame
- Centers subject precisely
- Maintains rule-of-thirds idealization
- Renders complete environmental context

### What Human Memory Does
- Framing is accidental, not designed
- Body parts leave frame naturally (turning, bending, leaning)
- Horizon tilts without awareness
- Objects obstruct because the photographer was chasing a feeling
- Cropping happens mid-expression, mid-movement

### Incomplete Framing Types

**A. Accidental Crop**
- Shoulder or arm cutting frame edge at angle, not straight cut
- Head tilted slightly past frame boundary
- Waist or hip消失在frame boundary，而非刻意midriff shot
- Hair部分離開畫面邊緣（甩出咗嚟）
- Leg消失在膝蓋以上，唔係標準full-leg framing

**B. Timing-Over-Anatomy**
- Subject's hand moves out of frame mid-gesture
- Foot steps just beyond frame edge (caught mid-step)
- Hair flips past frame boundary at apex of movement
- Body turns away AND head tilts, chest nearly invisible
- Phone held too high, chin部分cut off

**C. Horizon Imbalance**
- Slight tilt (8-15 degrees) — not dramatic aesthetic tilt, just unlevel
- Horizon line intersects subject at awkward position (neck, waist)
- Sea/ceiling/wall dominates unexpectedly
- Subject positioned extremely off-center because photographer tracked movement

**D. Obstructed Objects**
- Foreground object partially obscures subject (bag strap, glass edge, furniture corner)
- Subject behind/beside another person — face partially hidden
- Umbrella or plant interrupts view
- Someone's shoulder in frame edge
- 燈柱/柱/欄杆/電線杆 positioned awkwardly, not artistically

**E. Body Partially Leaving Frame**
- Leaning forward/backward causes torso to leave frame top/bottom
- Turning causes hip to leave frame side
- Sitting causes leg to leave frame
- Reaching causes arm to leave frame

### Prompt Grammar

```
[MAIN SUBJECT] captured at [ANGLE] by [OPERATOR]
— [frame disruption type] — [cause/reason in-world]
— [body part] exiting frame at [side/angle]
— [obstruction type] partially blocking [subject area]
— [horizon description]
```

### Trigger Conditions
- **Moonlit / nighttime scenes**: darkness naturally causes imperfect framing
- **Movement sequences**: turning, laughing, walking naturally produce crop
- **Environmental intimacy scenes**: foreground clutter creates natural obstruction
- **Social group contexts**: human obstacles produce natural obstruction
- **Beach/water scenes**: reflective/rippling surfaces cause partial visibility

### Implementation Examples

```
// Moonlit shoreline, accidentally captured
realistic moonlight shoreline, warm korean slim woman,
casual white linen shirt unbuttoned at top 2 buttons,
dark denim shorts, bare feet in shallow warm tidal water,
[HALF-BODY FORM nearchest frame left edge, body weight shifted
forward as if about to pick up shell from wet sand],
waist-level angle from slightly behind girlfriend's right shoulder,
evening blue-hour shoreline, cool moonlight on water surface,
phone snapshot from girlfriend, casual walking-away moment,
[PHONE HELD SLIGHTLY HIGH, chin部分cut off above lip],
skin showing natural warm redness from evening sun,
3-degree tilt, [WATER EDGE cuts through subject's bare ankles],
slight motion blur on water behind, phone-camera compression,
// EMOTIONAL MEMORY FRAGMENT: [frozen mid-laugh
breath just expelled, mouth not yet closed back]

// Seated on sofa, interrupted by phone
realistic ordinary apartment living room, afternoon warm light,
slim korean woman seated on gray linen sofa, oversized cream
long-sleeve knit cardigan worn loose, [RIGHT ARM extended along
sofa backrest, hand disappearing past frame right edge],
white bralette visible at deep V-neckline of cardigan,
[stray hair strand falling across cheek at mouth height],
half-profile turned toward phone held low,
[EXPRESSION frozen at moment before smile, lips just parting],
soft natural light from left window, mild digital noise,
casual girlfriend candid, body angled 30 degrees from camera,
// EMOTIONAL MEMORY: [eye contact just broken, gaze drifting
toward something outside frame — photographer was second choice]

// Overhead poolside — water-splash moment
overhead hotel poolside, late afternoon rim-light,
slim korean woman [LOWER LEGS submerged in pool from mid-shin,
knees appearing to cut frame BOTTOM edge at sharp diagonal],
[ONE ARM holding phone above water, wrist invisible above frame],
skin flushed warm from water temperature,
black one-piece swimsuit with subtle V-open back,
hair gathered to one side, wet dark hair clinging to neck,
[CROPPED at chest height, subject filling only upper 60% of frame],
reflective pool surface visible, [TILTED 10 DEGREES off horizontal],
hotographer lying on pool deck, iphone held underwater-at-surface,
// EMOTIONAL MEMORY: [caught in moment between looking at
phone and surfacing, eyes half-closed from chlorine]
```

---

## SYSTEM 2: MOTION CONTAMINATION

### What AI Does
- Perceptually frozen
- Sharp edges on moving parts
- No temporal ambiguity
- Perfect stability

### What Human Memory Does
- Moving through space = soft focus on parts in transit
- Shutter lag = image caught slightly after the moment
- Camera shake = photographer physically part of the moment
- Walking softness = real movement happening
- Turning body blur = natural act, not performance

### Motion Contamination Types

**A. Slight Motion Blur**
- Only on extremities (hand, foot, hair tip) — NOT entire body
- Direction-and-speed consistent with described action
- Blur radius: 1-3px equivalent, not dramatic
- Strands of hair show movement trails, not all hair

**B. Walking Softness**
- Subtle unsharpness on lower legs/steps during walk
- Upper body relatively sharper than feet/legs
- Body weight temporarily centered between steps
- Slight forward lean inconsistent with standing-still

**C. Camera Shake**
- Slight rotational smudge (not linear blur)
- Environmental details soft at edges
- Subject core relatively stable but periphery unstable
- Caused by: cold hands, laughing while shooting, excitement

**D. Shutter Lag Feeling**
- Expression caught 0.3-0.5 seconds AFTER the peak emotion
- Subject's gaze has moved but torso haven't caught up
- Hand position suggests gesture mid-execution
- Mouth in position between two sound expressions

**E. Turning-Body Blur**
- Torso rotates faster than legs
- Head leads, body follows with delay
- Shoulder line tilted from neutral
- Blur gradient: sharpest at eyes, softest at hip

### Prompt Grammar

```
[ACTION description] — [motion type]
— [blur direction/speed consistency]
— [what is sharper vs softer]
— [camera shake description if present]
```

### Trigger Conditions
- **Walking/running scenes**: always generate walking softness
- **Laughing/expression scenes**: natural shutter lag
- **Beach/pool scenes**: wind/air/water causes hair motion blur
- **Night/low-light scenes**: slower shutter = more shake
- **Excited/emotional moments**: photographer's camera shake

### Implementation Examples

```
// Walking along wet pavement
realistic urban hk alley, early evening, post-rain wet pavement,
slim korean woman in [oversized white cotton shirt,
lightly damp from light rain mist, two buttons undone at collar],
black midi skirt, [bare feet stepping carefully on wet tiles
visible foot COMING DOWN onto pavement with slight impact softness],
black crossbody bag worn across chest,
[stray hairs at temple starting to lift away from cheek with walk],
mid-body camera-level shot, [slight forward lean consistent w walk],
phone photo from walking friend, evening ambient warm light,
// MOTION SIGNATURE: [feet/ankles show 1.5px directional blur;
// upper body relatively stable; face sharpest element]

// Laughing at food stall
realistic hk dai pai dong food stall area, warm yellow tungsten
lights, auntie stall behind, slim korean woman [LAUGHING with head
tilted back, lips parting mid-exhale], oversized cream cable-knit
sweater worn off one shoulder, high-waisted dark denim skirt,
bare shoulders visible,
[CAMERA SHAKE: subtle 1-degree rotational smudge on right edge],
phone held at chest height from girlfriend beside her,
warm yellow light on wet skin from food stall steam,
// MOTION SIGNATURE: [expression caught SLOWER than body —
// smile full but gaze already drifting somewhere else]
// SHUTTER LAG: [moment AFTER peak laugh, breath just released]

// Turning away from camera
realistic small hong kong cafe interior, afternoon soft window light,
slim korean woman [TURNING AWAY slowly from camera,
[right shoulder already 3/4 from viewer, LEFT shoulder still
facing camera producing asymmetric body angle)],
oversized sage-green linen shirt, tucked-front tuck,
black high-waisted straight trousers,
// [skin visible at shirt neckline where shoulder turning exposed it],
[HAIR moving: several strands lifting away from neck with turn],
phone photo from friend standing behind-left,
caffe latte on wooden table beside her,
// MOTION SIGNATURE: [transition blur on torso; head sharpest;
hip area softest; blur gradient from face to leg]
```

---

## SYSTEM 3: EMOTIONAL TIMING

### What AI Does
- Perfect expression at decision point
- Eyes at full contact
- Smile at apex
- Emotion locked at peak

### What Human Memory Does
- Memory preserves the MOMENT BEFORE peak emotion
- Eyes fluctuate — contact, break, reconnect
- Expression catches mid-formation
- Laughter interrupted or abandoned
- Conflicted emotional states: happy AND distracted, sad AND composing

### Emotional Timing Types

**A. Expression Before Smile Completes**
- Lips just parting, not yet forming shape
- Cheeks beginning to lift, not yet full roundness
- Breathing audible — chest visible rising/falling
- Sound-forming mouth shape before laugh sound or speech

**B. Eye Contact Reconnecting**
- Eyes looking away at moment before re-engagement
- Gaze drift: subject looking at something in environment (not at viewer)
- Eyes in process of finding camera (not already locked on)
- Pupil slightly unfocused (processing, not presenting)
- Blink mid-expression (not staged full-eye contact)

**C. Distracted Gaze**
- Eyes focused past camera/photographer on something else
- Attention split between camera and environmental element
- Thought interrupted by photo: expression registers camera-acknowledgment late
- Eyes looking DOWN at something, then slowly lifting to meet camera
- Gaze through/around obstruction: partial obstruction, partial eye contact

**D. Interrupted Laughter**
- Laugh started but interrupted by breath/switch/bewilderment
- Smile settling back down from peak (not rising toward it)
- Breath being controlled/measured mid-expression
- Mouth transitioning from expression back to neutral
- One side of mouth still lifted but other already relaxing

**E. Sleepy Reaction Timing**
- Eyes half-lidded, not fully open
- Blink-stamp: eyes briefly closing, not camera-induced timed-blink
- Face not fully awake despite attempt
- Movement slower, more deliberate
- Expression processing at lower cognitive priority

### Prompt Grammar

```
[EMOTIONAL STATE description with timing]
— [expression in process / mid-formation]
— [eye contact status AND trajectory]
— [breathing/posture movement in progress]
— [what emotion is being interrupted by what]
```

### Trigger Conditions
- **Early morning / just-waking scenes**: sleepy reaction timing
- **Just-finished-laughing moments**: interrupted laughter
- **Environmental distraction scenes**: distracted gaze (look at ocean, sky, rain, food, someone else)
- **Warm indoor scenes (friends/food/drinks)**: expression-before-smile
- **Post-activity scenes**: expression returning to neutral

### Implementation Examples

```
// Post-laughing: settling back down
realistic hk rooftop bar with skyline view, evening warm air,
slim korean woman [LAUGHTER JUST SETTLING, right side of mouth
still slightly lifted, left side already dropping back to neutral],
oversized charcoal cashmere sweater, tucked-front tuck,
[warm flush spreading from cheeks downward to neck],
drink in right hand near face, [EYES DARTING from skyline
back to camera, pupil adjusting focus],
phone held high from girlfriend standing beside,
city lights beginning to glow in background,
// EMOTIONAL TIMING: [smile apex ALREADY PASSED;
// breath being measured; expression in DECAY phase not RISE]
// EYE PATTERN: [gaze found camera, held 0.5s, now looking away
at skyline again before camera captured]

// Mid-distracted: looking at ocean
beach shoreline at golden hour, warm tidal water,
slim korean woman [LOOKING OUT AT OCEAN, gaze unfocused
on horizon, eyes at 20% focus, no attempt to meet camera],
ocean-blue one-piece swimsuit with subtle ruched detail,
[skin flushed warm from 30min in water — redness on shoulders],
wind lifting hair away from face,
sand-flecked bare feet, [PHONE hanging relaxed at right side
not being held — photographer forgot to look at it mid-scene],
wide shot: subject small in frame with ocean dominant,
// EMOTIONAL TIMING: [ DISTANCED GAZE — caught in sensory
moment, not performance; camera caught her in private moment]
// POSTURE: [weight on back foot, side to camera,
shoulders relaxed — not pose-stance]

// Morning moment: not yet awake
small simple apartment bedroom, early morning warm light,
slim korean woman [LYING BACK on white linen pillow,
eyes HALF-OPEN, consciousness visibly not fully present],
bare shoulders above white cotton cami top,
chestnut hair spread on pillow, [SLEEP-WRINKLE visible
on one cheek pressed into pillow],
morning light from right window catching skin at angle,
// EMOTIONAL TIMING: [NOT performing — expression processing
at low cognitive priority; face relaxed in private morning moment]
// POSTURE: [weight entirely surrendered to gravity;
// no muscle tone in shoulders — completely natural]
```

---

## SYSTEM 4: ENVIRONMENTAL INTERRUPTION

### What AI Does
- Perfect environmental conditions
- Stable lighting throughout
- Objects in static idealization
- Weather serves composition
- Reflections as aesthetic

### What Human Memory Does
- Wind doesn't follow direction of light — it moves hair unplanned
- Wet fabric clings and shifts unpredictably
- Objects slip and change position mid-scene
- Moving shadows cut across faces unpredicted
- Reflections distort shape beyond recognition

### Environmental Interruption Types

**A. Wind Affecting Hair**
- Hair lifts in unplanned direction (not styled wind)
- Uneven wind: one side lifted, other side flat
- Hair shifts during exposure: image shows movement trail on one section
- Bangs blown across eye or cheek in messy unplanned way
- Hair lifts off neck, neck skin now exposed at unexpected angle

**B. Wet Fabric Shifting**
- Swimwear/skin wet with water: fabric clings differently than dry
- Water trails on skin: gravity-affected drip patterns, not even sheen
- Sheer fabric becomes MORE revealing when wet (cotton, linen)
- Fabric clings to body contours with water-weight drag
- Wet hair on skin: cools and causes goosebump response

**C. Object Slipping**
- Phone nearly dropped — grip tension visible in hand/forearm
- Drink sliding on table — hand chasing it
- Hairclip slipping out — half-escaped from hair
- Slipper sliding off foot — foot adjusting
- Bag strap sliding off shoulder — shoulder hiking up

**D. Moving Shadows**
- Sun moving across scene during exposure
- Cloud passing: shadow sweeps across face mid-shot
- Person walking past: shadow sweeps background
- Tree/shutter shadow oscillating with breeze
- Light quality changing through frame (half in sun, half in shadow)

**E. Reflections Changing Shape**
- Water rippling: reflection unrecognizable as coherent shape
- Phone screen / glass: face distorted and fragmented in reflection
- Wet floor: reflection of figure partially broken by foot contact
- Sunglasses: double-reflection from both lenses

### Prompt Grammar

```
[PRIMARY ENVIRONMENT description]
— [environmental interruption type]
— [physical causation chain]
— [what changed mid-scene from causal trigger]
— [resulting element: shifted fabric, blown hair, shadow sweep]
```

### Trigger Conditions
- **Beach/pool scenes**: water-related fabric and skin effects
- ** Outdoor scenes with humidity**: wind + wet fabric combo
- **Night scenes near water**: reflections + movement
- **Moving vehicles**: light changes, reflections, sliding objects
- **Food/drink scenes**: drink-related interactions

### Implementation Examples

```
// Wind + wet hair at beach
beach shoreline, late afternoon golden light, slim korean woman
[sitting on warm sand near water edge, SUN-TAN LOTION still
visible as slight white caste on upper back and shoulders],
[WET one-piece swimsuit: black with subtle side ruched detail,
CLINGING to body from ocean water, more revealing than dry],
[WIND lifted hair off neck and blown it asymmetric to right side,
several strands stuck to cheek wet with saltwater],
[SKIN showing natural pink from 1hr ocean activity —
redness concentrated on shoulders and collarbone],
bare feet half-buried in warm sand, ocean lapping at ankles,
// ENVIRONMENTAL INTERRUPTION: [ WATER caused swimsuit to
cling revealingly; WIND shifted hair asymmetrically;
// uneven wet causing irregular skin redness patterns]
// CAUSATION: ocean swim → wet clinging fabric + wet hair

// Rain-interrupted: sheltering with wet elements
hk narrow covered walkway, light rain tapping overhead,
slim korean woman [STANDING in shelter, OVERSIZED cream
long-sleeve knit cardigan DAMP at shoulders where rain
sprayed through shelter gap, fabric darkened and clinging],
[shelter rain causing unexpected damp on upper arm skin],
hair damp from humidity not rain direct, [WET HAIR CLINGING
to NECK showing goosebump texture pattern],
black wide-leg trousers, [LEFT SHOULDER slightly higher
from carrying bag — one sleeve riding up unevenly],
looking down at phone, wet pavement visible below walkway,
// ENVIRONMENTAL INTERRUPTION: [INCOMPLETE SHELTER caused
unexpected damp on specific body areas; rain indirect but
physically present and affecting fabric and skin]

// Moving shadows through frame
small rooftop hk apartment, late afternoon sun approaching angle,
[SUN MOVING ACROSS ROOM as cloud passes: warm light shaft
sweeping across subject's LEFT CHEEK AND NECK, mid-face
in partial shadow from moving cloud],
slim korean woman lying back on gray sofa, oversized white
cotton tee worn asymmetric (one side shoulder visible),
[skin showing natural warmth on sun-facing left side,
right side cooler-toned in shadow of cloud-sweep],
[stray hair bracket of temple hair blown slightly off face
from afternoon breeze coming through open window],
late-afternoon sofa candid, mild digital noise,
// ENVIRONMENTAL INTERRUPTION: [CLOUD PASSING causing shadow
sweep through face mid-exposure; half-face warm/half-cool;
light quality changing through frame, not stable]
```

---

## SYSTEM 5: CAMERA-MEMORY BEHAVIOR

### What AI Does
- Composition optimized for viewer response
- Subject centered or rule-of-thirds idealization
- Full lighting for full subject
- Environment as backdrop
- Everything simultaneously in sharp focus

### What Human Memory Does
- Emotionally significant elements sharper even at cost of other details
- Environment darkness survives flash (memory: camera light didn't carry to dark areas)
- Imperfect focus means photographer was emotionally invested, not technically precise
- Exposure balances memory priority, not technical correctness
- Camera operator was inside the moment, not outside observing it

### Camera-Memory Behavior Types

**A. Emotional Priority Over Composition**
- Camera operator shot because something FELT significant, not because it looked good
- Composed toward emotional moment even at compositional cost
- Subject slightly off-center but their eyes/face maximally committed to frame
- Environment cropping unfortunate but accepted: moment was about person, not place

**B. Memory-Preserving Exposure**
- Bright element (window, sky, light source) may blow to white
- Dark areas remain dark — flash/reflection not extended
- Highlight detail sacrificed for subject emotional exposure
- Shadow detail sacrificed for glow of skin / expression
- Sometimes face slightly underexposed to preserve atmospheric context

**C. Imperfect Focus**
- Focus locked on eyes/face, everything else soft
- Focus on gesture: hands/wrists sharp, face soft
- Focus on emotional center: expression sharp, environment soft
- Occasionally front-element focus miss (nose sharp, eyes soft — not ideal but human)
- Soft focus gradient: face clear, chest medium, legs very soft

**D. Environmental Darkness Surviving Flash**
- Flash pops in low-aperture burst, doesn't fully illuminate room
- Dark corners remain dark — memory of dark corners preserved
- Background remains dark even with foreground illumination
- Overhead/shadow areas invisible to camera = invisible in photo
- Flash creates a pocket of light around subject, darkness beyond

### Prompt Grammar

```
[MOMENT description — what the photographer was emotionally responding to]
— [emotional priority: what the camera operator COVETED capturing]
— [exposure compromise: what was sacrificed]
— [focus zone: what was prioritized]
— [flash behavior: atmospheric vs fill]
```

### Trigger Conditions
- **Low-light / night scenes**: memory-preserving exposure essential
- **Intimate indoor scenes**: emotional priority over composition
- **Social moments with friends (dining, laughing, drinking)**: focus on expression
- **Environmental atmosphere-first scenes**: imperfect focus, darkness surviving
- **Group dynamics moments**: camera operator had favorite person, adjusted for them

### Implementation Examples

```
// Emotional priority: camera loved her reaction, not her pose
humble hk apartment kitchen, late evening tungsten light,
slim korean woman [TURNED AWAY from camera slightly,
eating late-night ramyun straight from pot, chopsticks lifting
noodles mid-air, steam rising near chin level],
oversized black henley-tee, white shorts underneath,
[stray wet noodle-broth droplet at corner of mouth —
not yet noticed, not yet wiped],
[PHOTOGRAPHER FOCUSED ON HER EXPRESSION, face sharp,
upper body medium-sharp, kitchen background COMPLETELY
SOFT AND DARK — environment abandoned visually],
slight smile around chopstick mouth, eyes looking down at pot,
// EMOTIONAL PRIORITY: [not a good photo technically;
// kitchen dark, posture non-ideal, face just adequate —
// but photographer loved her being comfortable enough to
// eat messily and wanted to preserve THIS feeling]
// MEMORY EXPOSURE: kitchen lost to darkness

// Flash memory: darkness survived
realistic hk small apartment living room, evening,
compact digital camera flash, [FLASH illuminating subject
but living room corners REMAINING COMPLETELY DARK
despite flash — room too large for on-camera flash to reach],
slim korean woman seated on floor leaning against sofa,
crumpled oversized cream cable-knit cardigan around her,
[BARE FEET, toes slightly curled against floor],
phone-checking moment, soft slight smile,
[KITCHEN DOORWAY visible at frame right edge, completely black —
flash didn't carry there, memory preserved dark],
street light glow from window washing wall faintly,
// FLASH BEHAVIOR: [pocket of light on subject — kitchen
doorway 1m away completely black — real camera, real flash]

// Imperfect focus: photographer loved her hands
realistic small nail salon interior, late afternoon,
slim korean woman at nail station, [HANDS raised above
nail desk surface, each finger being attended by nail tech],
[EYES slightly soft from camera proximity and shallow depth],
[FOCUS GRADIENT: wrists sharp > fingers sharpest > face soft],
casual white cropped tank top, black high-waisted wide trousers,
// IMPERFECT FOCUS: [not a portrait — photographer prioritized
hands, face just context; eyes not camera-locked, partially
unfocused from looking at nail work (not at camera)]
// ATMOSPHERE: [nail salon pink-white lighting, mild chemical
scent feeling, small space detail]
```

---

## MODERATION IMPLICATIONS

### Emotional Timing — Mod-Friendly
- Expressions caught mid-process tend to be LOWER intensity than peak-expression
- Distracted gaze = viewer engagement lower = lower moderation risk
- Interrupted laughter = open mouth but not posing = natural, not performative

### Environmental Interruption — Mod-Friendly  
- Environmental chaos ("wind-blown," "water-damp") provides fabric-shift justification
- Hair covering neck/face reduces visible skin surface
- Object obstruction naturally reduces direct body display
- Shadows are natural, not imposed darkness

### Motion Contamination — Mod-Friendly
- Blur reduces anatomical precision = less platform flagging risk
- Soft edges on limbs/body reduce "display" feeling
- Shutter lag = natural, unplanned, not pose-stance = less glamour signal
- Camera shake = candid feel = social photography context

### Camera-Memory Behavior — Mod-Friendly
- Flash underexposure tends to darken skin = lower contrast/saturation risk
- Dark environments reduce platform scanning readability
- Emotional priority framing = less "about her body" feeling
- Imperfect focus = less "professional quality" = less influencer-coded

### AVOID Moderation Risks
- Motion blur does NOT justify explicit anatomical content
- Environment darkness does NOT justify implied-nudity photography
- Incomplete framing does NOT justify partial-nipple visible
- Emotional timing does NOT justify close-up sexual expression

### Hard Rules for Memory System Mod-Safety
- Incomplete framing: body parts exit frame as ACCIDENT not INTENT
- Partial visibility: subject INCOMPLETE because of natural crop, not CROP FOR DISPLAY
- Dark environments: darkness from reality, not FROM SHADOW ADDITION for hide-reveal
- Motion blur: reduce sharpness naturally, NOT to obscure explicit content

---

## ANTI-AI LOGIC

The Memory Capture System is the strongest anti-AI production system:

1. **AI cannot generate genuine emotional priority**: AI doesn't feel, only composes
2. **AI cannot generate true shutter lag**: AI captures best moment, not delayed one  
3. **AI cannot generate unplanned environmental causation**: AI controls all variables
4. **AI cannot generate imperfect focus that feels intentional**: AI focuses perfectly
5. **AI cannot generate accidental crop**: AI always frames intentionally

**Detection markers that humans find authentic but AI struggles with:**
- Emotional timing: the moment before/after peak (AI gives peak)
- Motion contamination: partial blur only on specific areas (AI blurs everything uniformly)  
- Environmental interruption: specific, causal, physically traceable (AI makes things beautiful, not messy)
- Incomplete framing: body parts leave frame at angles, not straight cuts (AI gives complete bodies)
- Camera-memory behavior: exposure/exposure compromises that feel emotionally motivated (AI optimizes technically)

---

## V14.6 INTEGRATION NOTES

### Memory System Activation Triggers
When ANY of these conditions are present, EMOTIONAL MEMORY FRAGMENT becomes mandatory:
- Moonlit / night scenes
- Water / wet environments  
- Movement sequences (walking, turning)
- Social moments with friends
- Laughing / emotional expression scenes
- Early morning / late night scenes
- Intimate indoor environments

### Mandatory Emotional Memory Fragment
Every prompt should include a bracketed memory fragment describing the SPECIFIC MOMENT being preserved:

```
[EMOTIONAL MEMORY: description of a specific, small, real-feeling detail]
```

Examples:
- `[frozen mid-laugh breath just expelled, mouth not yet closed back]`
- `[eye contact just broken, gaze drifting toward something outside frame]`
- `[caught in moment between looking at phone and surfacing, eyes half-closed]`
- `[smile apex ALREADY PASSED — breath being measured; expression in DECAY phase]`

### Integration Hierarchy
1. Character anchor (from CHARACTER_LOCK)
2. Environment causation + social reason (from V14 core)  
3. MEMORY_CAPTURE_SYSTEM — incomplete framing + emotional timing
4. Camera operator identity (from CAMERA_OPERATOR_SYSTEM)
5. Fabric causality (from V14 core)
6. Anti-AI markers (from V5/V14)
7. Moderation gate

### V14.6 Naming Convention
All V14.6 new systems include:
- `[INCOMPLETE FRAMING TYPE]` markers in prompts
- `[EMOTIONAL MEMORY FRAGMENT]` bracketed description
- `[MOTION CONTAMINATION TYPE]` markers where movement present
- `[ENVIRONMENTAL INTERRUPTION TYPE]` causation trace
- `[CAMERA-MEMORY BEHAVIOR]` exposure/focus compromise description

### Cross-Reference
- CAMERA_AWARENESS_SYSTEM.md — camera awareness levels modify which memory types are most authentic
- V14 core ENGINE file — core composition/environment logic remains active
- V5 upgrade modules — HUMIDITY_HAIR_BEHAVIOR_SYSTEM integrates here
