# ATTENTION_ROUTING_ENGINE
### V20 — Research #001
### Status: RESEARCH PHASE

---

## RESEARCH SOURCE

- **Task:** Notion 04 Research → 01 GPT Research Tasks → 2026-06-01 → Research #001
- **Date:** 2026-06-01
- **Agent:** Lucy (Hermes)
- **Priority:** P1

## RESEARCH GOAL

Study how high-performing female lifestyle / KOL / gravure-adjacent photos guide viewer attention without feeling crudely staged.

## CORE QUESTION

**Why do some images make viewers stop scrolling, while others are forgotten instantly?**

---

# PART 1: ATTENTION ROUTING CORE LOGIC

## Why Eye Flow ≠ Attention Routing

**EYE FLOW** (existing V17): Where the eye physically moves through the frame.

**ATTENTION ROUTING** (new): WHY the eye stops, WHERE it lands, WHAT makes it care.

The difference:
- Eye flow = camera mechanics
- Attention routing = viewer psychology

---

## The 5-Second Attention Window

```
0-0.5s:  INSTINCT SCAN  — brain registers brightness, movement, skin
0.5-1s:  ATTENTION PIVOT — "Is this interesting?" — sub 100ms judgment
1-2s:    ENGAGEMENT HOLD — "I'll look closer" — emotional engagement
2-5s:    MEANING RESOLUTION — "What is this? What's happening?"
5s+:     MEMORY ENCODING — "I'll remember this"
```

AI-generated images fail at 0.5-1s. They look technically fine but there is no reason to care.

Real photographs have a **REASON TO BE LOOKED AT** — an ongoing narrative tension, an unspoken question, an emotional state in motion.

---

## ATTENTION ANCHOR HIERARCHY

### Level 1: PHYSICAL ATTENTION (involuntary, pre-cognitive)

These trigger attention before the viewer even thinks:

| Anchor Type | Mechanic | Why It Works |
|-----------|----------|--------------|
| **SKIN_LUMINANCE** | Brightest area wins | Human visual system wired to detect skin — 200ms reaction |
| **HIGH_CONTRAST_EDGE** | Sharp boundary against soft | Eye drawn to contrast boundaries first |
| **MOTION_COMPRESSION** | Action blur + sharp face | Eye tracks movement then lands on stillness |
| **CAMERA_FACING** | Looking at viewer | Eye evolved to track gaze direction |
| **DIRECTIONAL_GAZE** | Looking somewhere off-frame | "What is she looking at?" — creates narrative tension |
| **BRIGHTNESS_SPIKE** | Something brighter than surroundings | "Light source" = eye trap |

### Level 2: COGNITIVE ATTENTION (emotional, decision-making)

These hold attention because they trigger meaning:

| Anchor Type | Mechanic | Why It Works |
|-----------|----------|--------------|
| **ACTION_INTERRUPT** | Middle of motion, not posed | "She's about to..." — creates anticipation |
| **EMOTIONAL_BREAKTHROUGH** | Genuine emotion, unposed expression | Mirror neuron response — viewer feels |
| **NARRATIVE_GAP** | Something off-frame is implied | "What is that?" — viewer reconstructs story |
| **OBJECT_INTEREST** | Familiar object in unexpected context | "Oh I have that too" — personal recognition |
| **BODY_LANGUAGE_READ** | Posture tells a story | Viewer decodes meaning without words |
| **SOCIAL_PROOF** | Someone else in frame paying attention | "What's she looking at?" doubles engagement |

### Level 3: MOTIVATED ATTENTION (social, identity-driven)

These create memory because they connect to identity:

| Anchor Type | Mechanic | Why It Works |
|-----------|----------|--------------|
| **ASPIRATIONAL_IDENTITY** | "I want to be her" | Aspirational self-projection |
| **RELATABLE_IDENTITY** | "That's so me" | Self-recognition, shared experience |
| **ENVY_NURTURE** | Beauty you want to protect | Nurturance response to beauty |
| **ENVY_COVET** | Beauty you want to possess | Competitive response |
| **SOCIAL_TRIBAL** | "She belongs to my world" | Tribe recognition |
| **CURIOSITY_STATUS** | "Where is that? Is that expensive?" | Social status scanning |

---

## SCROLL-STOPPING MECHANISMS

### Mechanism 1: THE NARRATIVE GAP

**Definition:** Something important is happening off-frame or just happened, and the viewer wants to know what.

**Pattern:** Subject looking at something we can't see. Body positioned relative to an unseen element. Expression suggesting off-frame event.

**Examples:**
```
❌ FAILS:
"Beautiful woman smiling at camera"
→ Complete. No narrative. Nothing unresolved.

✅ WORKS:
"Caught mid-laugh looking off-frame at something sudden, 
mouth still open, body turning"
→ Narrative gap: "What made her laugh?"
→ "What was so sudden?"
→ Viewer needs resolution — stops scrolling
```

**Prompt language:**
```
Caught looking off-frame at [IMPLIED EVENT]
Body pivoting toward [OFF-FRAME ELEMENT]
Expression just broke into [EMOTION] — moment just passed
```

### Mechanism 2: THE INTERRUPTED ACTION

**Definition:** Action is in progress — not before, not after. The moment itself.

**Pattern:** Motion blur on extremities combined with face in clear focus. Hand mid-gesture. Hair mid-movement. Body weight in transit.

**Examples:**
```
❌ FAILS:
"Standing in pose, perfect composure"
→ Static. Nothing is happening.

✅ WORKS:
"Caught in the moment of sitting down — butt just touching 
seat, weight still transferring forward, arms slightly 
out for balance, surprised expression at the unexpected 
comfort of the seat"
→ Body math that only works mid-motion
→ Face shows genuine surprise, not posed
→ If she completed the sitting, it would look staged
```

**Critical Rule:** The action must be at a point where completing it would make the image look posed.

### Mechanism 3: THE GAZE ESCAPE

**Definition:** Subject is looking at something off-frame, AND that something is implied by the environment.

**Pattern:** Looking at phone/door/window/mirror/friend/water. Environment provides object. Gaze has destination.

**Examples:**
```
❌ FAILS:
"Looking anywhere, no context for why"
→ Gaze feels random. Viewer shrugs.

✅ WORKS:
"Gaze locked on phone screen, phone visible at frame 
edge, laughing at something on screen, hand still 
holding phone, not posing for camera"
→ Clear gaze destination
→ Activity justifies attention
→ Phone in frame creates photo-reason
```

### Mechanism 1b: THE GAZE TETHER

**Definition:** Subject looks at off-frame element AND the photo-reason justifies why someone would be taking this photo.

**Pattern:**
```
Looking away from camera at [OBJECT IN FRAME]
+ [OBJECT TYPE] implies social/candid photo reason
= "A friend captured this moment"
```

**Examples:**
```
Gaze toward [DESIGNATED OBJECT] — [OBJECT NAME] is the reason 
someone took this photo. Looking away from camera shows she 
was genuinely absorbed in [ACTIVITY], not posing.

Objects that tether the gaze:
- Phone (documentary)
- Food (casual meal)
- Friend (friend-shot)
- Mirror (selfie logic)
- Window (daydream)
- Ocean/wind (environmental presence)
- Book/cup (domestic activity)
```

---

## ATTENTION PATH CATEGORIES

### Category A: FACE-DOMINANT PATH (Face = Anchor + Destination)

Viewer's attention starts AND ends at the face. Nothing competes.

**Use when:** Face expression carries all emotional payload.

```
SUBTYPES:
A1: FACE_ISOLATION — Face is framed alone, no body context
A2: FACE_CASCADE — Hair→Face→Eyes (gravure path, beauty content)
A3: FACE_SOFT — Face in window light, soft background (portrait mode)
```

**A1 Examples:**
```
tight_frame_face_only:
"Face filling frame, eyes direct, expression [EMOTION],
sharp focus, minimal bokeh, no shoulder, no hand visible"
→ Face IS the content
→ Used for: expression study, beauty content, voyeur moment

A2 Examples:
cascade_hair_face_eyes:
"Shot from above through hair curtain, eye finds face through 
hair frame, then eyes, hair is slightly in motion, sharpest 
point at eyes, background soft bokeh"
→ Hair creates natural frame
→ beauty/gravure optimization
→ Eye trapped by hair → face → eyes
```

### Category B: FLOW-THROUGH PATH (Something else → Face)

Eye starts somewhere else first, then travels to face.

**Use when:** Environment, action, or context adds to the emotional payload.

```
SUBTYPES:
B1: FLOOR_ESCALATION — Floor element → Body → Face (ground level shots)
B2: DIAGONAL_SWEEP — Corner → Body → Face (architectural spaces)
B3: FOREGROUND_TETHER — Object → Hand → Face (activity focus)
B4: LIGHT_GUIDE — Light source → Lit area → Face (atmosphere mood)
B5: ENVIRONMENTAL_STORY — Space → Position → Face (documentary)
```

**B1 Examples:**
```
floor_object_to_face:
"Eye starts at sand grain at bottom frame edge, travels up 
through towel fold line to body to face, phone visible at 
towel corner where her hand is, body reclined, face looking 
at phone"

standing_environmental_anchor:
"Eye starts at floor tile pattern, travels up through legs 
and body to face looking at something above frame, standing 
in [LOCATION], someone else's [OBJECT] in background"
```

**B3 Examples (Most Common Scroll-Stopping Path):**
```
phone_hand_face:
"Eye travels from phone screen ( brightest element in frame)
to hand holding phone to head tilt to eyes looking down — 
phone visible in frame, she's genuinely looking at something 
on screen"

drink_to_face:
"Eyeline follows drink in hand up to lips to face — drink 
at chest level, head tilted toward drink, face showing 
reaction to taste, activity justifies the photo"
```

### Category C: NARRATIVE-QUESTION PATH (Face + Gaze Creates Tension)

Face visible, looking off-frame. Viewer constructs narrative.

```
SUBTYPES:
C1: GAZE_ESCAPE_DEVICE — Face + looking at something implied
C2: GAZE_ESCAPE_PERSON — Face + looking at person off-frame
C3: GAZE_ESCAPE_WINDOW — Face + looking at window/environment
```

**C1 Examples:**
```
face_gaze_chain:
"Face [EXPRESSION TYPE], gaze directed toward [DESTINATION], 
[DESTINATION TYPE] visible at frame edge, suggesting 
[IMPLIED STATE], she's not noticing the camera"

caught_gaze_reaction:
"Caught in the moment of noticing something, eyes just 
shifted to [DIRECTION], expression transitioning from 
[OLD STATE] to [NEW STATE], she hasn't registered the camera yet"
```

### Category D: BODY-LANGUAGE-READ PATH (Posture = Story)

Face may be small, but body language tells the complete story.

**Use when:** Action, posture, position carry more emotional weight than face expression.

```
SUBTYPES:
D1: ACTION_DOCUMENTARY — Body mid-action, face as context
D2: SPATIAL_CONFIDENCE — How subject occupies space communicates
D3: LOW_GROUND_AFFINITY — Ground postures read as confident/trapped
D4: LEANING_INTOX — Environmental leaning creates personality
```

**D1 Examples:**
```
action_not_pose:
"Body caught mid-[ACTIVITY], weight has not settled, 
not posing, face visible but secondary, feet positioned 
for [REASON], hands in natural position from [ACTION], 
documents the actual moment not a reenactment"

feet_floor_context:
"Body language reads as [FEELING] through [POSTURE TYPE], 
feet planted for [REASON], upper body expressing [STATE], 
face visible but letting body tell the story"
```

---

# PART 2: VISUAL HIERARCHY IN ATTENTION

## Priority Rules: What Wins Attention First

### Hierarchy Rules (in priority order):

```
PRIORITY 1: SKIN + DIRECT EYE CONTACT
→ Anything with these always wins attention first
→ When direct eye contact is in frame: eye goes there instantly
→ This is why friend-shot eye contact is so powerful

PRIORITY 2: OBJECT CARRYING NARRATIVE
→ Phone, drink, food, book — these justify WHY the photo exists
→ Objects at frame edge create photo-reason
→ Objects in hand show activity → narrative

PRIORITY 3: BRIGHTEST AREA
→ Light source, reflective surface, screen glow
→ Eye always tracks to brightest first
→ Window light is a free attention anchor

PRIORITY 4: MOTION
→ Blur on extremities, sharp on face
→ Eye tracks motion first, then lands on "suddenly still" face
→ This is why mid-motion shots outperform static poses

PRIORITY 5: CONTRAST
→ Highest contrast area wins
→ Sharp edge against soft background
→ Subject's edge is her frame
```

### When to Break Priority Rules:

**RULE: Direct eye contact always wins**
↓
**EXCEPTION:** When face expression is HIDDEN and body language is doing all the work:
```
"Face partially turned away, looking at [DESTINATION],
body language dominant, face visible but not primary"
→ Eye goes to most readable body posture, not face
```

**RULE: Brightest area wins**
↓
**EXCEPTION:** When brightest area is ENVIRONMENTAL and subject is darker but still readable:
```
"Face in shadow but visible, looking away from camera,
body lit from behind, subject is darker than background
light but eye still finds her because of gaze direction"
→ Eye uses gaze direction as secondary path
```

---

# PART 3: ENVIRONMENT-SPECIFIC ATTENTION MAPS

## Beach

```
ATTENTION PATTERNS:
1. WET SKIN BEATS DRY SKIN — wet skin reflects light = eye magnet
2. WATER AT FRAME EDGE — implies motion, suggests she just came from water
3. HAIR TEXTURE — wet hair has visual weight and movement
4. SAND CONTEXT AT FOOT — natural foreground anchor
5. SUN/GLARE ON SKIN — bright spots create multiple eye traps

FAIL STATES:
- Dry organized beach setup = 100% AI signal
- Perfect towel alignment = staged
- Elaborate pose on beach towel = "photoshoot on beach"
- Hair controlled and styled = "got ready to pose"

WORKING PATTERNS:
- Sand at feet, slightly messy towel
- Water glistening on skin, hair wet
- Body not perfectly positioned, slight tilt/lean
- Something she brought (book, bottle) casually placed
- If on towel: not centered, not posed, doing something
```

## Hotel Room

```
ATTENTION PATTERNS:
1. WINDOW LIGHT — primary attention anchor
2. BEDROOM CLUTTER — objects show she lives there
3. BODY SPATIAL LANGUAGE IN ROOM — how she occupies the space
4. REFLECTION — mirror doubling the shot, creates depth
5. ROOM SERVICE / LUGGAGE ELEMENTS — spatial logistics

FAIL STATES:
- Perfect bed arrangement = stock photo
- No objects in frame = empty stage
- Single-source flattering light = studio setup
- Standing at window perfectly lit = posed

WORKING PATTERNS:
- Luggage open, clothes visible
- Coffee cup at frame edge (she was awake, drinking coffee)
- Hair messy from just waking
- Not looking at camera, engaged with room
- Window light from side, face catches some, body in partial shadow
```

## MTR / Transit

```
ATTENTION PATTERNS:
1. PLATFORM YELLOW LINE — natural floor anchor for foot placement
2. POLE / RAIL — body connection to environment
3. PHONE IN HAND — transit activity justification
4. CROWD CONTEXT — social presence triggers attention
5. TRANSIT GRAPHICS — HK-specific floor/cling/window ads

FAIL STATES:
- MTR with no people = simulation
- Perfect MTR pose = never happens in real life
- Looking at camera in MTR = impossible unless documentary
- Too clean, too organized = staged

WORKING PATTERNS:
- Looking at phone, phone visible
- Standing with weight shift, one hand on pole
- Behind others in frame (depth, social proof)
- In motion: escalator, walking through station
- MTR as backdrop while doing something else
- Chinese characters, station branding visible in frame
```

## Street / Night Out

```
ATTENTION PATTERNS:
1. NEON REFLECTION — light sources double visual interest
2. PUDDLE REFLECTION — creates horizontal eye path
3. BODY CONFIDENCE IN SPACE — how she occupies urban environment
4. STREET LIGHT SPILL — uneven lighting = naturalist
5. MOVING CARS / CROWD — motion creates urgency

FAIL STATES:
- Perfect neon arrangement = city romance shot
- Too posed in street = "she's trying to look natural"
- Perfect hair/makeup under neon = makeup ad
- No environmental personality = could be anywhere

WORKING PATTERNS:
- Leaning against wall naturally (not posed-for-wall)
- Hair affected by wind/atmosphere
- Holding drink, bag, phone — urban objects
- Not posing, walking somewhere
- Rain on skin in night = extremely high retention
```

---

# PART 4: THE ATTENTION-PRODUCTION CONNECTION

## Why Attention Routing Matters for Prompting

### The Single Most Important Discovery:

**AI images fail because there's no INTERNAL NARRATIVE.**

A human photographing her friend knows WHY they're taking the photo:
- "She looks really pretty right now"
- "This view is amazing and we're here together"
- "That was a funny moment and I caught it"
- "She looks so happy with this drink"

This WHY creates the ATTENTION ROUTING:
- The moment of surprise → attention pivot on face
- The view behind → attention guides through environment
- The activity → attention follows object to face
- The laugh → attention finds reaction to capture it

**AI prompts skip the "why" and describe the "what."** Result: technically correct but emotionally dead images.

### The Engine Fix: Photo-Existence Anchor

Every image needs a REASON FOR EXISTING. This reason routes attention.

```
PHOTO_EXISTENCE_RULES:
1. If there's a phone in frame → the photo exists because she was 
   using/checking it. The attention path is phone → face.
   
2. If there's a drink in frame → the photo exists because she's 
   having a moment with the drink. Attention path is drink → face.
   
3. If there's friends in frame → the photo exists because 
   someone took it for her. Eye goes friend → her → reaction.
   
4. If there's no object → the photo must have immediate 
   narrative. She's doing something, caught mid-action.
   
5. If face is expression-heavy → the photo exists because 
   she just made that face. Expression IS the reason.
```

---

## ANTI-PATTERNS (What Kills Attention)

| Anti-Pattern | Why It Fails | Fix |
|-------------|-------------|-----|
| STATIC POSE | Nothing is happening | Use TENSION state (about to move) |
| DIRECT SMILE | Over-engaged, over-aware | Use ABSORBED state (not registering camera) |
| COMPLETE BODY COMPOSURE | Looks posed | Use INCOMPLETE SITUATION (mid-action, not settled) |
| EVEN LIGHTING | No brightness hierarchy | Illuminate face brightest, rest accepts shade |
| CENTERED composition | No flow path needed | Offset face OR add foreground anchor |
| PERFECT HAIR | "Got ready" signal | Add HAIR_MOTION or MESSY_DAMP keywords |
| CLEAN ENVIRONMENT | "Studio set" signal | Add MESSY_ANKER or IN_USE object |
| NO PHOTO REASON | "Why was this taken?" | Add phone/drink/friend/activity in frame |
| ALL FOCUS SHARP | No depth hierarchy | Soft background OR soft periphery |
| OVERLY SMOOTH SKIN | AI signal | Add SKIN_TEXTURE or DOCUMENTARY_MOOD |

---

# PART 5: WHAT THE IMAGE IS SELLING

## The Attention Economy of Female KOL Images

Every popular KOL photo is SELLING something:

| Image Type | What It Sells | Attention Route |
|-----------|-------------|-----------------|
| Beach candid | LIFESTYLE ASPIRATION | Environment → beauty → mood |
| Hotel morning | DOMESTIC INTIMACY | Object clues → face → comfort |
| Street fashion | SOCIAL IDENTITY | Outfit → pose → location |
| Café moment | RELATABLE DAILY LIFE | Activity → face → mood |
| Night out | SOCIAL EXCITEMENT | Energy → environment → confidence |
| Friend shot | AUTHENTIC CONNECTION | Friend → her → shared moment |
| Mirror selfie | UNDERSERVED INTIMACY | Reflection → self → confidence |

## Prompt Language for "Selling":

```
SELLING_THE_LIFE:
"Captured the way she actually exists — not posing for 
photographs but living in the frame. [LOCATION TYPE] 
suggests [LIFESTYLE], [OBJECT IN FRAME] implies [REASON], 
[EXPRESSION TYPE] was the unscripted moment that made 
someone reach for their camera."

SELLING_THE_CONFIDENCE:
"Body language that reads as [FEELING] without trying — 
[POSTURE TYPE] suggests she occupies this space naturally, 
[GAZE TYPE] shows [ATTENTION STATE], not aware of camera 
in this moment."

SELLING_THE_MOOD:
"[FILM_STOCK] rendering amplifies [MOOD TYPE] mood, 
[CAMERA_TYPE] from [DISTANCE] away captures the moment 
without surveillance feeling — she exists in the frame, 
she doesn't perform for it."
```

---

# PART 6: CROSS-AREA ATTENTION COMPATIBILITY

## Eye Flow Integration (V17 EYE_FLOW_LIBRARY)

| Eye Flow Template | Attention Routing Addition |
|-----------------|--------------------------|
| BOTTOM_UP | Attention starts at floor anchor — adds REALISM GROUNDED |
| DIAGONAL_LEAD | Attention sweeps through architectural space — adds SPATIAL ENERGY |
| FG_SUBJECT | Object in frame = photo reason — adds NARRATIVE COMPLETENESS |
| LIGHT_ANCHOR | Brightest area = attention source — adds ATMOSPHERE PAYLOAD |
| OBJECT_EYE | Phone/hand/face chain — this IS the core scroll-stopper |
| ENVIRONMENTAL | Space → position → face — adds DOCUMENTARY AUTHENTICITY |

## Spatial Composition Integration (V17 SPATIAL_COMPOSITION)

3-ZONE DEPTH + ATTENTION ROUTING combinations:

```
FOREGROUND OBJECT = photo reason anchor
→ Eye starts at FG object (attention pivot)
→ Travels through mid-ground subject
→ Lands on face (attention destination)
→ Creates BOTH spatial depth AND narrative reason

PATTERN:
foreground: [OBJECT — phone/drink/book at frame edge]
→ subject: [ACTIVITY/POSE/NOT-POSE]
→ background: [LOCATION CONTEXT]
→ attention_path: OBJECT → BODY → FACE
```

## Face-First Integration (V15 FACE_FIRST_COMPOSITION)

Face-anchor + gaze-escape combinations:

```
PATTERN A: FACE_DOMINANT_NARRATIVE
Face (brightest, sharpest) + looking at [DESTINATION OFF-FRAME]
→ Eye lands on face (attention anchor)
→ Travels to gaze target (tension creation)
→ Narrative gap: "What is she looking at?"

PATTERN B: FACE_SUPPORTING_BODY_STORY
Body language dominant + face small but readable
→ Eye reads body first (narrative)
→ Travels to face (emotional confirmation)
→ Both body and face work for attention

PATTERN C: FACE_MINIMAL_SCENE_ANCHOR
Face tiny but holding gaze because of gaze direction
→ Eye goes where she's looking (primary attention)
→ Face is the secondary confirmation point
→ Used for environmental/storytelling images
```

---

# PART 7: TOKENS FOR ATTENTION ROUTING

## New Token Categories

### ATTENTION PATH TOKENS (300+)

```
# Scroll-Stopping Path Tokens
[PHONE_HAND_FACE]     — Object→hand→face chain (deeply natural)
[DRINK_CHEST_FACE]     — Drink at chest→head tilt→face
[BOOK_LAP_FACE]        — Book in lap→looking down→face
[SAND_FOOT_BODY]       — Floor object→body→face (beach)
[FLOOR_TILE_BODY]      — Floor anchor→standing body→face (MTR/Street)
[TOWEL_EDGE_BODY]      — Towel corner→body reclined→face
[WINDOW_LIGHT_FACE]    — Light source→lit area→face (atmospheric)
[NEON_GLOW_FACE]       — Neon reflection→face in light
[MIRROR_DOUBLE_FACE]   — Reflection→face→reflection loop
[FRIEND_REACTION_FACE] — Friend looking→her→shared reaction

# Gaze Anchor Tokens
[GAZE_ESCAPE_PHONE]   — Looking at phone, phone visible
[GAZE_ESCAPE_WINDOW]   — Looking at window/view
[GAZE_ESCAPE_FRIEND]   — Looking at person off-frame
[GAZE_ESCAPE_DOOR]     — Looking at door/entry
[GAZE_ESCAPE_OCEAN]    — Looking at ocean horizon
[GAZE_ESCAPE_MIRROR]   — Looking at mirror reflection
[GAZE_ESCAPE_FOOD]     — Looking at food/drink arriving
[GAZE_ESCAPE_NOTICE]   — Looking at something sudden/unexpected

# Narrative Gap Tokens
[NARRATIVE_GAP_LAUGH]    — Just laughed at something off-frame
[NARRATIVE_GAP_SURPRISE] — Just surprised by something
[NARRATIVE_GAP_NOTICE]   — Just noticed something
[NARRATIVE_GAP_INTEREST]  — Currently engaged with something
[NARRATIVE_GAP_REALIZE]  — Just realized/remembered something
[NARRATIVE_GAP_FRIEND]   — Friend just said/did something

# Action-Interrupted Tokens
[MID_SIT]               — Body mid-sit, not settled, weight transferring
[MID_LIFT]               — Object mid-lift, not complete
[MID_LEAN]               — Leaning into position, not stable
[MID_TURN]               — Body turning, face following
[MID_STAND]              — Just stood up, weight not locked
[MID_APPLY]              — Product/object at face, mid-application
[MID_NOTICE]             — Expression just shifted, moment captured
[MID_LAND]               — Feet mid-step, landing moment
```

### ATTENTION STATE TOKENS

```
# Absorption States (camera not noticed)
[ABSORBED_PHONE]        — Deep in phone, not aware
[ABSORBED_FOOD]         — Eating/engaged with food
[ABSORBED_MIRROR]       — Looking at own reflection
[ABSORBED_THINKING]     — Daydreaming somewhere
[ABSORBED_ACTIVITY]     — Doing something with full attention

# Reaction States (noticed something, moment captured)
[REACT_LAUGH]           — Just laughed, expression still warm
[REACT_SURPRISE]        — Just surprised, expression open
[REACT_EXCITED]         — Just got exciting news/info
[REACT_DISAPPOINTED]    — Just received bad news (moment captured)
[REACT_CONFUSED]        — Just realized something unclear
[REACT_CONFIDENT]       — Just completed a look/reveal

# Relationship States (camera is friend/family)
[FRIEND_CAPTURE]        — Friend took photo, different from selfshot
[FRIEND_CONTEXT]        — Someone photographed her as she existed
[PARTNER_PEEK]          — Partner caught her in moment
[SELFIE_UNDERSERVED]    — Selfie but she looks like she forgot
```

### ATTENTION PRODUCTION TOKENS

```
# Photo-Reason Tokens
[PHOTO_REASON_PHONE]    — Phone justifies photo reason
[PHOTO_REASON_DRINK]   — Drink justifies photo reason
[PHOTO_REASON_MIRROR]  — Mirror justifies selfie-logic
[PHOTO_REASON_FOOD]    — Food justifies casual documentation
[PHOTO_REASON_FRIEND]  — Friend shot justifies non-camera-awareness
[PHOTO_REASON_VIEW]    — View justifies "look at this moment"
[PHOTO_REASON_NO]      — Unsure photo-reason, narrative gap required

# Scroll-Stop Intensity
[SCROLL_STOP_HIGH]      — High retention, something happens
[SCROLL_STOP_MED]      — Medium retention, visual quality
[SCROLL_STOP_CURIOSITY]— Viewer curiosity was triggered
[SCROLL_STOP_EMOTION]  — Emotional response triggered
[SCROLL_STOP_SOCIAL]   — Social/proximity trigger
```

---

# PART 8: IMPLEMENTATION RULES

## Rule 1: Every Image Needs a Photo Reason

```
ASK: "Why was this photo taken?"
→ If answer is "to show how pretty she is" → FAIL
→ If answer is "she was doing something, check it out" → PASS

IMPLEMENT:
[PHOTO_REASON_TOKEN] must be present in every prompt
Phone, drink, friend, mirror, activity — pick one or create tension
```

## Rule 2: Attention Path Must Be Unbroken

```
ASK: "Where does the eye enter? Where does it land? How does it travel?"

GOOD PATH: Entrance → Path → Destination with no competing noise
BAD PATH: Multiple equally bright areas competing for attention

IMPLEMENT:
1 bright anchor (max)
1 clear path through frame
1 clear destination (usually face)
No competing brightness close to face brightness
```

## Rule 3: Narrative Active, Not Stative

```
ASK: "What is happening in this photo?"

STATIVE: "She looks beautiful in a pose"
→ No moment, no reason, no retention

ACTIVE: "She just sat down, hasn't settled, was checking phone, 
        got distracted by something, looked up"
→ Something happened, viewer wants to know what
→ High retention, emotional engagement

IMPLEMENT:
Use [MID_*] tokens for interrupted action
Use [REACT_*] tokens for post-event states
Use [GAZE_ESCAPE_*] tokens for implied off-frame event
```

## Rule 4: Face Hierarchy Cannot Be Ignored

```
ASK: "Is the face doing enough work?"

IF face carries emotional payload → FACE_DOMINANT path
IF body/environment carries more → body language readable, 
                                   face secondary but present

IMPLEMENT:
Face must be EITHER primary anchor OR confirmed secondary
Never leave face unreadable in an image that needs human connection
```

## Rule 5: Anti-Staged Layering

```
Every prompt must include AT LEAST 2 of:
- Absorption state (not registering camera)
- Mid-action state (not complete)
- Photo-reason object in frame
- Off-frame implied event (gaze escape)
- Social lens (friend/candid, not surveillance)

3 out of 5 = very natural
2 out of 5 = workable
1 out of 5 = risk of looking staged
```

---

# PART 9: SUGGESTED PROMPT LANGUAGE

## Core Attention Routing Grammar

```
[PHOTO_REASON] + [ATTENTION_PATH] + [ATTENTION_STATE] + [GAZE_TYPE] + [FACE_TREATMENT]

Example A:
[PHOTO_REASON_PHONE] presence implied — someone was taking photos
    because she was absorbed in something
[MID_PHONE_CHECK] — she was on phone when something caught her attention
[EXPRESSION_SHIFT] — her expression is transitioning from phone to something else
[GAZE_ESCAPE_NOTICE] — she's looking at what just happened, gaze just shifted
[FACE_BRIGHTEST] — face catches light from window, brightest point
→ RESULT: Natural documentary moment, clearly someone took the photo 
          because something happened, not because she posed

Example B:
[PHOTO_REASON_DRINK] — she got a drink, check this moment out
[DRINK_CHEST_FACE_BOARD] — drink at chest level leads to head tilt
[ABSORBED_DRINK] — she hasn't noticed the camera, deep in the drink moment
[GRAZE_ESCAPE_FOOD] — she's tasting something or someone said something
[FACE_SOFT_WINDOW] — face in soft window light, dreamy atmosphere
→ RESULT: Girl in the moment with her drink, immediately relatable, 
          high retention, photo reason is totally natural

Example C:
[PHOTO_REASON_NO] — this moment is interesting because of what 
                    happened, not because of an object
[MID_SIT_WEIGHT] — she just sat down, weight still transferring
[REACT_LAUGH] — she just burst into laughter
[NARRATIVE_GAP_FRIEND] — friend just said something funny
[WINDOW_FACE_GAZE_ESCAPE] — face lit by window, she's looking where 
                            the laugh went (at friend)
→ RESULT: Caught mid-uncontrollable laugh, body mid-sit, not a posed 
          portrait, this moment happened — extreme retention
```

## Prompt Injection Pattern

```
INJECT INTO EXISTING PROMPTS:
Add after [LOCATION] and [SUBJECT]:

"[PHOTO_REASON_TOKEN] in frame
[ATTENTION_PATH: entrance → path → destination]
[ATTENTION_STATE: absorption/reaction/interrupted-action]
[GAZE_TYPE if applicable]"
```

---

# PART 10: CROSS-REFERENCES & VALIDATION

## Cross-References

| File | Relationship |
|------|-------------|
| EYE_FLOW_LIBRARY.md (V17) | Eye flow = physical path. Attention routing = the WHY. |
| SPATIAL_COMPOSITION_LIBRARY.md (V17) | FG→Subject→BG + Attention Path = combined |
| FACE_FIRST_COMPOSITION_SYSTEM.md (V15) | Face hierarchy + gaze escape = powerful |
| OBJECT_SOCIAL_SYSTEM.md (V16) | Objects in frame = photo reason = attention anchor |
| MEMORY_CAPTURE_SYSTEM.md (V14) | Genuine moments captured = attention/retention |
| MICRO_SOCIAL_SYSTEM.md (V15) | Micro reactions = reactive states for attention |
| CAROUSEL_ARC_ENGINE.md (V19) | Attention path across carousel = retention of story |

## Engine Change Proposal

**RECOMMENDATION: Create `ATTENTION_ROUTING_ENGINE.md` as a V20 module**

This engine extends V17's EYE_FLOW_LIBRARY with psychological depth:
- Eye flow = the mechanism
- Attention routing = the psychology

The division of labor:
- EYE_FLOW: describes WHERE the eye moves physically
- ATTENTION_ROUTING: describes WHY the eye stops and CARES

Both are needed together. V17's EYE_FLOW is not replaced — it's continued.

## Suggested Character Bible Expansion

No physical identity changes. No behavioral identity changes.

If Body Language research (#003) validates specific ground postures that create high-attention body language:
- Create a **Character Bible Proposal** in the research folder
- Outline: posture type, why it routes attention, suggested token
- GPT/Jason decides whether to merge

---

# SUMMARY

## What This Research Solves

- **WHY** AI images fail to stop scrolling (no internal narrative)
- **HOW** attention actually moves through a frame (5-Second Attention Window)
- **WHAT** scroll-stopping actually requires (narrative tension, not visual quality)
- **WHERE** to position gaze/face/object for maximum attention routing
- **WHICH** anti-patterns to eliminate systematically

## Core Takeaways (6 Sentences)

1. Eye flow is mechanics; attention routing is psychology — both needed.
2. Images fail at the 0.5-1 second mark because viewer asks "Why should I care?"
3. The answer: narrative gap, interrupted action, or gaze escape with photo-reason.
4. Every image needs a reason-to-exist: phone, drink, friend, activity, or tension.
5. Face-first and body-language-dominant are both valid attention strategies.
6. Anti-staged layer: absorption state + photo-reason object + off-frame implication.

---

*Research File: ATTENTION_ROUTING_ENGINE.md*
*Source: Research #001 — Notion 04 Research → 2026-06-01*
*Status: RESEARCH PHASE — pending DeepSeek verification + consolidation*
*GitHub: ~/Documents/lil.troublr/Engine/research/V20_RESEARCH/ATTENTION_ROUTING_ENGINE.md*
