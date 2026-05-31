# V18 SOCIAL DENSITY ENGINE
## Research Document: Why AI Photos Feel Empty and How to Fix It

---

## PART 1: PROBLEM STATEMENT

### Why AI-Generated Photos Feel "Off"

When users look at an AI-generated image of a person at a café, alone at a table, the immediate gut reaction is: **something is wrong**. Not "this looks fake" but something deeper—a sense of social death, of existing in a vacuum.

This is the **Social Vacuum Problem**. AI-generated images, even high-quality ones, suffer from a fundamental absence: **they show people without the invisible social infrastructure that surrounds every human being in reality**.

In real photography—from your friend's Instagram to Japanese gravure to Hong Kong street shots—the frame is always dense with social evidence. Even when someone appears alone, the social world bleeds in:

- A chair pushed back indicating companions recently departed
- A second coffee cup visible at the edge of frame
- Strangers walking through the background at different social distances  
- A cropped hand reaching into the frame from an off-camera friend
- A reflection showing others who exist but aren't "the subject"

**The AI Social Vacuum happens because:**
1. Diffusion models optimize for the "subject"—everything else becomes background noise to be minimized
2. Training data (stock photos) often strips context for commercial usability  
3. Negative space is confused with "clean composition"—creating socially sterile environments
4. The model learns "person at location" as an isolated atom, not as "person embedded in social fabric"

**The result**: Images that look technically perfect but feel emotionally hollow. Like a person in a museum diorama, or a staged display window.

---

## PART 2: WHY V17 CANNOT SOLVE THIS

V17's approach to social context is **token-based and explicit**. It might have tokens like "friends," "people in background," "party atmosphere." These fail because:

| V17 Approach | Why It Fails |
|--------------|--------------|
| Explicit tokens like "with friends" | Creates obvious group shots, not subtle social density |
| Background people tokens | Renders them as anonymous "crowd noise" not social evidence |
| Atmosphere tokens like "lively" | Describes an abstract quality rather than encoding specific visual proof |
| Pure subject isolation | Has no mechanism to render "implied social presence" |

**Core limitation**: V17 treats social context as a binary (present/absent) or vague atmosphere modifier. It cannot generate the specific visual evidence that humans instantly recognize as social proof:

- **Who is this person to the viewer?**
- **Are they waiting for someone?**
- **Did they just leave someone?**
- **Is someone about to enter the frame?**

These questions create narrative tension and social reality. V17 has no answer for them.

**The V17 mental model:**
```
[Subject] + [Setting] + [Atmosphere Token] = Social Context
```

**The V18 mental model:**
```
[Subject] + [Social Evidence Tokens] + [Implied Presence Markers] + [Off-Screen Social Traces] = Social Density
```

---

## PART 3: THE SOCIAL DENSITY ENGINE

The Social Density Engine introduces **25 specialized tokens** that encode specific, visually verifiable social evidence. Each token represents a real pattern from human photography that signals "this person is embedded in a social world."

### Category A: Visible Social Presence (SOC-01 through SOC-08)

---

#### SOC-01: CROPPED COMPANION EDGE

**Problem**: AI photos show complete people or no people. Real photos often cut people off at the frame edge—the universal signal of "someone is here, just not centered."

**Photography Reference**: 
- Japanese gravure photobooks (e.g., Bejean, Junshoku magazines) frequently frame models with another person's shoulder or arm visible at frame edge
- Hong Kong street photographer Fan Ho's compositions often include partial figures at frame boundaries creating spatial tension
- Xiaohongshu lifestyle posts show friends partially cropped—signaling "I was with someone" without making it "a photo of two people"
- Family albums: the universal "someone was standing right there" shot where a child's head is cut off at the top edge

**Why it works**: The cropped element creates cognitive completion—viewer's brain fills in the rest, creating stronger social presence than if the companion were fully visible. It's the photographic equivalent of dramatic irony.

**Human Behavioral Logic**: When people take photos socially, they frame imperfectly. Someone always leans in, reaches over, or the photographer crops someone by accident. Perfect framing = photographer's eye = staged. Imperfect = social moment.

**Visual Evidence**:
- Shoulder emerging from frame edge (left or right)
- Top of someone's head cut off at frame boundary
- Hand entering frame from outside
- Arm wrapping around subject but partially cropped

**Prompt Vocabulary**:
```
- "friend's shoulder at frame edge"
- "cropped arm entering from left edge"  
- "someone's hand on shoulder, partially cut off"
- "partial figure at frame boundary suggesting companion"
```

**Integration Rules**:
- NEVER position cropped companion on the same side as subject's dominant eye contact direction (creates conflict)
- Crop at natural joint boundaries (wrist, elbow, shoulder) not mid-segment
- Ensure cropped element has DIFFERENT focal blur than subject (closer = more real)
- Maximum 2 cropped elements per frame to avoid chaos

**Anti-AI Benefit**: AI models have extreme difficulty with edge-of-frame partial subjects. They tend to either complete them or blur them into background noise. The cropped companion is a strong authenticity marker.

**Example Prompt Fragment**:
```
"...casual lifestyle photo, girl's shoulder entering frame from left edge, 
blurry friend's arm visible at right margin, warm afternoon light, 
shot on Canon EOS R5 with 50mm f/1.4, authentic moment..."
```

---

#### SOC-02: HANDS IN FRAME (PROXIMAL SOCIAL EVIDENCE)

**Problem**: AI renders hands badly AND treats them as part of the subject. Real social photos have hands that belong to OTHER people doing social things.

**Photography Reference**:
- Gravure: Model with someone's hand on her waist (cropped), the hand clearly not hers
- HK street: Fan Ho's shots where a pedestrian's hand reaches across frame
- Casual SNS: The classic "holding boyfriend's hand at table edge" shot where only the hand is visible
- Family album: An adult's hand holding a child's (cropped at wrist) - signals family context

**Why it works**: Hands are intensely social organs. A hand entering the frame from below says "someone is here, they're interacting with the space or the subject." It implies touch, connection, proximity.

**Human Behavioral Logic**: When we photograph socially, other people's hands frequently enter the frame—we're reaching for drinks, touching shoulders, holding cigarettes. This is evidence of embodied social interaction.

**Visual Evidence**:
- Someone else's hand on subject's shoulder/waist/arm
- Hand passing a drink or object toward off-camera person
- Hand holding a cigarette in frame (social activity indicator)
- Hand gesturing in conversation, cropped at wrist
- Child's hand in parent's grip, cropped

**Prompt Vocabulary**:
```
- "friend's hand on shoulder, cropped at wrist"
- "someone's hand passing coffee, motion blur"
- "other person's fingers on subject's arm, partially visible"
- "child's small hand held by adult, frame cut at wrist"
- "hand with cigarette crossing frame edge"
```

**Integration Rules**:
- Hands should be at DIFFERENT focal plane than main subject (closer = more authentic)
- Motion blur on hands is good (indicates real movement happened)
- Hands should enter from frame edge or bottom, not top
- If subject's hands are visible, at least one OTHER person's hand should also be present

**Anti-AI Benefit**: Hands remain one of AI's biggest failure points. Partially visible, out-of-focus hands belonging to someone else = nearly impossible for AI to generate consistently.

**Example Prompt Fragment**:
```
"...casual street photo, another person's hand visible at frame bottom 
passing a coffee cup, motion blur on hand, subject laughing off-camera, 
shallow depth of field, shot on Ricoh GR III..."
```

---

#### SOC-03: REFLECTION TRAP (OTHERS IMPLIED)

**Problem**: AI rarely generates reflections, and when it does they're usually technically wrong (inverted light, impossible angles). Real reflections of others = instant social reality.

**Photography Reference**:
- Street photography: Vivian Maier frequently used reflections in windows, showing the backs of people who were in front of her—or showing her own reflection while capturing strangers
- HK nightlife: Neon reflections in wet streets showing blurred pedestrians  
- Graffiti/shop windows: The classic "person looking at phone with reflected crowd behind them"
- Café scenes: Chrome surfaces, glass tables, spoons showing distorted room reflections

**Why it works**: A reflection shows someone else who exists in the same space but isn't directly photographed. It's visual proof of off-camera social existence. The brain immediately registers "there are people near this person."

**Human Behavioral Logic**: We capture reflections accidentally or intentionally—it's a way of showing the social environment without making it the subject. Real photographers use reflections as compositional tools.

**Visual Evidence**:
- Window reflection showing blurred figures behind subject
- Glass door reflection of people entering behind
- Water puddle reflection of street scene (adds secondary narrative layer)
- Sunglasses reflection of photographer/viewer
- Phone screen reflection of subject's face AND someone else behind

**Prompt Vocabulary**:
```
- "reflection of strangers in glass door behind"
- "window reflection showing blurred pedestrians"  
- "puddle reflection adding secondary street scene"
- "sunglasses reflecting the photographer's silhouette"
- "phone screen with subject and someone else's face"
```

**Integration Rules**:
- Reflections must be at CONSISTENT lighting with scene (nighttime neon reflection in glass)
- Blur the reflection MORE than the subject (depth cue says "behind/beside")
- Reflections should show DIFFERENT people than subject—never self-reflection unless intentional
- Reflections of entire scenes (mirror-like) are suspicious—partial, distorted reflections are more authentic

**Anti-AI Benefit**: Reflections require understanding of optics, lighting direction, and spatial relationships. AI frequently gets reflections backwards, upside-down, or with wrong lighting. Even when AI generates reflections, they feel "placed" not "captured."

**Example Prompt Fragment**:
```
"...fashion photo, glass shop window reflection showing two blurred 
pedestrians walking behind, wet street reflecting neon signs, 
subject in foreground sharp, reflection layers at f/2.8..."
```

---

#### SOC-04: SECOND DRINK / EXTRA PLACE SETTING

**Problem**: AI shows a single person with a single drink. Real social photos encode waiting—they show evidence someone is expected.

**Photography Reference**:
- Japanese café photos: The universal "my friend hasn't arrived yet" shot—two drinks on table, one being sipped
- Western lifestyle: Empty chair with jacket draped over it (companion temporarily absent)
- Bar photography: Two glasses, one half-emptied, one still full (someone is coming back)
- Restaurant: Table set for two, one seat pushed back (someone just stepped away, not abandoned)

**Why it works**: An extra drink, an extra place setting, a pushed-back chair—these are temporal evidence. They say "this scene is paused, not complete." It implies narrative, social intention, waiting.

**Human Behavioral Logic**: We photograph moments of transition—waiting for friends, someone stepped away mid-meal, the table isn't cleared yet. These transitional states are more authentic than frozen perfection.

**Visual Evidence**:
- Two drinks, one being held, one untouched
- Two plates, one mostly finished, one just served
- Chair pushed slightly back from empty seat
- Jacket over chair back at empty spot
- Bag on empty chair indicating "saved seat"
- Phone facedown at second place setting

**Prompt Vocabulary**:
```
- "second untouched coffee cup on table"
- "chair pushed back at empty seat beside her"
- "jacket draped on chair back indicating companion temporarily away"
- "two drinks, one half-finished, one full"
- "phone facedown at second place setting"
- "bag on saved seat"
```

**Integration Rules**:
- The "missing person" evidence should be BELOW eye line (on the table, not in the frame above)
- Unfinished item should show evidence of USE (lipstick on cup rim, bite mark on fork)
- Spatial relationship: empty seat should be close enough to subject to imply connection
- Avoid "sad" framing—presence of waiting companion should feel warm, not lonely

**Anti-AI Benefit**: AI tends toward "one subject, one drink" simplification. The concept of "someone is coming" or "someone was here" requires narrative understanding that AI lacks.

**Example Prompt Fragment**:
```
"...lifestyle photo, café table with two coffee cups, one in hand 
with lipstick mark, one untouched and cooling, subject looking 
at phone, warm bokeh light, shot on Fujifilm X100V..."
```

---

#### SOC-05: STRANGER CROSSING FRAME (SOCIAL NOISE)

**Problem**: AI renders either empty backgrounds or anonymous "crowd" blur. Real photos have SPECIFIC strangers doing specific things—creating actual social texture.

**Photography Reference**:
- Fan Ho's Hong Kong street: Strangers crossing at different depths, each with implied purpose
- Tokyo Shibuya crossing: The classic "sea of people with individual trajectories"
- Café scene: Single stranger walking behind, blurred, with shopping bag (specific social context)
- Park scene: Dog walker crossing, child running past—each stranger tells a micro-story

**Why it works**: A specific stranger (carrying a specific bag, walking in a specific direction) implies a destination, a life, a narrative beyond the frame. Anonymous crowd blur feels like rendering failure. A specific stranger feels like life happening.

**Human Behavioral Logic**: When photographers capture "social context," they often wait for the right stranger to cross—a person whose trajectory adds to, rather than distracts from, the composition.

**Visual Evidence**:
- Single blurred stranger crossing at edge (specific, not generic)
- Two figures in background walking in opposite directions (social motion)
- Stranger looking at phone while passing (specific activity)
- Child running across frame with toy (family context implied)
- Elderly person crossing slowly in background (density marker)

**Prompt Vocabulary**:
```
- "single stranger crossing at frame edge, motion blur"
- "two pedestrians crossing background at different depths"
- "elderly person crossing slowly in background"  
- "child running across frame holding balloon"
- "stranger checking phone while passing, blurred"
- "couple walking through background in opposite directions"
```

**Integration Rules**:
- Stranger should be SPECIFIC (age, clothing, activity) not generic "person"
- Motion blur on stranger = authenticity. Sharp stranger = may feel placed
- Strangers should cross at EDGES, not center (center crossing distracts)
- Maximum 3 strangers per frame, each at different focal depth
- Direction of movement should be consistent with implied narrative

**Anti-AI Benefit**: AI generates "crowds" as uniform noise. The specific stranger with specific trajectory and specific purpose is a high-level social concept that breaks AI's pattern matching.

**Example Prompt Fragment**:
```
"...lifestyle photo, young woman at window, single elderly man 
crossing street below at slow pace, motion blur, rain on glass, 
out of focus couple walking opposite direction in background, 
cinematic lighting..."
```

---

#### SOC-06: CAMERA HOLDER EVIDENCE

**Problem**: AI shows people looking at camera (posing) or away (candid). Real photos often show EVIDENCE of who was holding the camera—the social context of WHO is documenting.

**Photography Reference**:
- Selfie culture: Hand holding phone visible at bottom frame
- Group shots: Someone's arm extended holding camera (visible partially)
- Photographer's shadow/reflection in mirror selfie
- Second camera visible in reflection (documenting the moment)
- Timer shot: Camera on tripod with countdown context

**Why it works**: Showing who holds the camera is meta-commentary on the social nature of photography. "Someone was here documenting this" = social proof stronger than the photo itself.

**Human Behavioral Logic**: We document moments WITH people. The hand holding the phone that took the photo is evidence of relationship, shared experience, social documenting.

**Visual Evidence**:
- Hand holding phone visible at frame bottom (selfie context)
- Camera case/strap visible at edge (documenting photographer exists)
- Shadow of photographer in frame (street photography classic)
- Phone screen reflection showing camera app interface
- Front-facing camera visible in mirror selfie (meta-selfie)
- Timer countdown visible on phone screen

**Prompt Vocabulary**:
```
- "hand holding iPhone visible at frame bottom"
- "camera strap visible at left edge"
- "photographer's shadow falling across subject"
- "phone screen reflection showing camera UI"
- "compact camera case on table beside subject"
```

**Integration Rules**:
- Camera holder evidence should be at BOTTOM or EDGE, not centered
- The hand/device should be in-focus if close, blurred if at extreme edge
- Meta-framing (photo of someone taking a photo) is a powerful authenticity trigger
- Avoid making "camera evidence" the subject—it should be peripheral social context

**Anti-AI Benefit**: Meta-photography (photos showing the act of photography) confuses AI training data. The concept of "documenting the documentarian" is philosophically complex and rarely rendered well.

**Example Prompt Fragment**:
```
"...casual portrait, hand holding smartphone visible at frame bottom, 
front camera reflected in mirror behind subject, soft lighting,
selfie aesthetic but not posed, natural expression..."
```

---

#### SOC-07: OFF-SCREEN CONVERSATION EVIDENCE

**Problem**: AI shows isolated subjects or groups facing each other directly. Real photos often show evidence of conversation with people OUTSIDE the frame—the social world extends beyond boundaries.

**Photography Reference**:
- Two people at café looking at EACH OTHER (conversation implied)
- One person looking at another off-camera (someone they're talking to)
- Subject mid-laugh at something said by someone not in frame
- Hand gesture suggesting response to off-screen comment
- Person on phone, mid-conversation (off-screen voice implied)

**Why it works**: Conversation requires at least two. When we see evidence of one person reacting to another, but can't see that other, the brain completes the social circuit. This creates narrative tension and social presence.

**Human Behavioral Logic**: We photograph moments of interaction—someone laughing, someone responding, someone gesturing. The moment of reaction is more authentic than posed interaction.

**Visual Evidence**:
- Subject mid-laugh, head tilted back, eyes crinkled (someone said something funny)
- Hand gesture of response (talking to off-screen person)
- Gaze at something outside frame (listener tracking speaker)
- Person on phone with animated expression (two-way conversation)
- Eye contact between two subjects (interaction, not isolation)

**Prompt Vocabulary**:
```
- "mid-laugh at off-screen comment"
- "gesturing in response to unheard question"
- "eyes tracking something outside frame"
- "phone conversation mid-sentence, animated"
- "two people in frame looking at EACH OTHER, not camera"
```

**Integration Rules**:
- Eye contact between subjects in frame = strong social bond marker
- Subject looking OFF-FRAME while someone else in frame reacts = conversation evidence
- Mid-action (not peak expression) is more authentic—laughter builds, doesn't start at apex
- Phone conversation is acceptable but should show ACTIVITY (gesturing, walking while talking)

**Anti-AI Benefit**: AI tends to freeze expressions at a static point. Real conversation photos capture the FLOW of interaction. The "someone just said something" moment vs. the posed smile.

**Example Prompt Fragment**:
```
"...documentary style, young woman mid-laugh with head tilted back, 
someone off-camera clearly just told her something, other friend 
in frame smiling in response, natural bokeh, shot on Leica Q2..."
```

---

#### SOC-08: SOCIAL OBJECT PROXIMITY (ABANDONED BUT PRESENT)

**Problem**: AI shows objects floating in space. Real photos show objects in the context of SOCIAL USE—placed, left behind, shared.

**Photography Reference**:
- Restaurant: Two menus on table, one open, one closed (two people were browsing)
- Beach: Two flip flops, parallel but one slightly kicked off (person just left)
- Bar: Two glasses, one finished, one still with liquid (companion exists)
- Park bench: Sweater left draped, phone beside it (owner stepped away)
- Table: Two pairs of chopsticks, one used, one untouched (waiting for friend)

**Why it works**: Objects in social context show EVIDENCE of use by multiple people, or the transitional state between presence and absence. It's temporal social evidence.

**Human Behavioral Logic**: We photograph moments where social context is embedded in objects—not "a glass" but "someone's glass" vs. "an empty glass that belongs to no one."

**Visual Evidence**:
- Two of any personal object (cups, chopsticks, shoes, bags)
- One object showing USE, one showing UNUSE (temporal contrast)
- Object in position of RECENT USE (chair warm, drink half-finished)
- Personal item left behind (jacket, bag, phone) indicating TEMPORARY ABSENCE

**Prompt Vocabulary**:
```
- "two coffee cups, one with bitten cookie beside it"
- "pair of flip flops, one kicked off at angle"  
- "jacket draped on chair back, phone on table"
- "two bowls of ramen, one half-eaten, one just served"
- "sweater left on bench, umbrella beside it"
```

**Integration Rules**:
- Objects of same type should show DIFFERENT states of use (one finished, one not)
- Position should imply recent occupation (chair slightly pushed, drink with lipstick mark)
- Avoid "abandoned" feeling—presence should feel TEMPORARY, not desolate
- Spatial relationship between paired objects should be casual, not arranged

**Anti-AI Benefit**: AI generates "objects" as isolated items with no social history. The concept of "someone's vs. no one's" requires understanding of possession and social context.

**Example Prompt Fragment**:
```
"...cozy café scene, two ramen bowls on wooden table, one half-eaten 
with chopsticks resting, one steaming full, subject looking at 
phone with smile, other person's bag visible on adjacent chair..."
```

---

### Category B: Implied Social Presence (SOC-09 through SOC-16)

---

#### SOC-09: PARTIAL BODY FRAME (CUTOFF ANATOMY)

**Problem**: AI renders complete bodies or awkward headless torsos. Real photos strategically cut bodies at natural boundaries to create intimacy and social framing.

**Photography Reference**:
- Portrait photography: Classic "top of shoulders and up" framing
- Fashion: Head and shoulders, arms partially cropped at biceps
- Lifestyle: Subject from mid-chest up, hands visible holding something
- Groups: Some members fully visible, some cropped at various points

**Why it works**: Partial bodies create COMPOSITIONAL social intimacy. The frame feels "cropped by someone standing close" rather than "rendered incomplete by algorithm."

**Human Behavioral Logic**: When we're socially close to someone, we photograph them intimately—close enough that full body won't fit. This is different from "full body shot" which is formal, distant.

**Visual Evidence**:
- Torso and up, arms cropped mid-bicep
- Full body but HEAD CROPPED at top (casual framing)
- Subject from knees up (sitting close)
- Full body with other person's arm/shoulder crossing into frame

**Prompt Vocabulary**:
```
- "portrait from shoulders up, casual framing"
- "full body but head slightly cropped at top"
- "subject from mid-chest down, hands holding coffee"
- "intimate crop at biceps, arm crossing frame"
- "knees up framing, sitting on chair edge"
```

**Integration Rules**:
- Crop at NATURAL JOINTS (elbow, wrist, shoulder, knee) not mid-segment
- Cropped edge should NOT cut through joints at 90 degrees (avoid amputee look)
- If cropping multiple subjects, use DIFFERENT crop points for each (intimate vs. formal)
- Horizon line (if visible) should NOT cut through a cropped head

**Anti-AI Benefit**: AI struggles with understanding natural crop points vs. unnatural ones. The "right" crop feels like photographer's eye; the "wrong" crop feels like rendering error.

**Example Prompt Fragment**:
```
"...casual portrait, head and shoulders cropped at collarbone, 
hands visible holding iced coffee, other person's shoulder 
entering from right edge, shot on Sony A7RIV with 85mm..."
```

---

#### SOC-10: SOCIAL HEIGHT HIERARCHY (POWER DYNAMICS IN FRAME)

**Problem**: AI renders everyone at similar apparent distance/focus. Real social photos encode power dynamics—who's above, who's below, who's leaning in.

**Photography Reference**:
- Japanese gravure: Frequently shoots from slightly below (idolizing angle)
- HK street: Fan Ho shoots from street level, people above on stairs
- Café: Someone leaning in over table (height difference = intimacy/urgency)
- Selfie: Phone held high (dominant height = casual confidence)

**Why it works**: Height relationships encode social dynamics. Leaning in over table = intimate conversation. Looking down = dominance/confidence. Looking up = vulnerability/reverence.

**Human Behavioral Logic**: We unconsciously use height in social photography—shooting down at someone makes them look small/ subordinate; shooting up makes them look important/vulnerable.

**Visual Evidence**:
- Camera angle below subject's eye level (idolizing up-shot)
- Camera above subject's head (shooting down, confident subject)
- Two subjects at different heights in same frame (power dynamic)
- Leaning posture creating height differential between two people

**Prompt Vocabulary**:
```
- "shot from below eye level, slight仰角 (upward angle)"
- "camera elevated above subject's head"
- "two subjects, one leaning in creating height gap"  
- "shooting down at subject on lower chair"
- "slight low angle making subject look empowered"
```

**Integration Rules**:
- HEIGHT RELATIONSHIP should match SOCIAL RELATIONSHIP
- Shooting down at someone comfortable = confident casual
- Shooting up at someone uncomfortable = vulnerability/formality
- Height differential between two in-frame subjects = relationship dynamic
- Low angle with wide lens = dramatic/important; high angle with portrait lens = casual/intimate

**Anti-AI Benefit**: AI tends to default to "eye level neutral" which feels staged. The specific height relationship encodes narrative information that AI doesn't understand.

**Example Prompt Fragment**:
```
"...portrait with slight low angle, subject sitting on lower stool 
while friend standing behind leaning in, natural window light, 
intimate casual mood, shot on Canon 50mm f/1.2..."
```

---

#### SOC-11: PROXIMITY SIGNALS (DISTANCE INTIMACY)

**Problem**: AI shows people at arbitrary distances. Real photos show specific, meaningful proximity—close enough to touch, far enough to be formal.

**Photography Reference**:
- Couple photography: Bodies almost touching, arm around waist (visible pressure of proximity)
- Friends: Lean in with heads close, shoulders touching (intimate friendship)
- Strangers: Full arm's length distance, no body contact (polite public distance)
- Family: Child leaning into adult, overlapping body positions (protective intimacy)

**Why it works**: Physical proximity is the universal language of social closeness. Bodies touching in frame = romantic/familial. Bodies near but not touching = friendship. Bodies distant = formal/stranger.

**Human Behavioral Logic**: We calibrate physical distance in photos unconsciously—closer = more comfortable/intimate, further = more formal/reserved.

**Visual Evidence**:
- Shoulder touching shoulder (friends/intimate)
- Arm around waist visible in frame (romantic/family)
- Bodies partially overlapping (protective intimacy)
- Full arm's length with no body contact (formal distance)
- Leaning postures creating proximity through geometry

**Prompt Vocabulary**:
```
- "shoulders touching, heads inclined toward each other"
- "arm visible around waist, slight pressure of hold"
- "bodies overlapping slightly at edges"
- "arm's length distance, no body contact"
- "child leaning into parent's side, body positions overlapping"
```

**Integration Rules**:
- Proximity should be CONSISTENT with relationship type
- Romantic = body contact or < 1 foot
- Friends = almost touching, < 2 feet
- Family = protective proximity, overlapping boundaries
- Strangers = > 3 feet, no body language alignment
- Watch for "awkward" proximity that's neither intimate nor formal (AI symptom)

**Anti-AI Benefit**: AI tends to default to "standard portrait distance" which feels like stock photo. The specific calibrated proximity is learned from real social photography, not from AI training sets.

**Example Prompt Fragment**:
```
"...casual photo of two friends, shoulders touching, heads 
inclined together laughing at something off-camera, arm's length 
from camera, natural light, shot on Fujifilm X-T4..."
```

---

#### SOC-12: OFF-CAMERA GAZE TARGET

**Problem**: AI shows subjects looking at camera or vaguely into space. Real photos show subjects looking AT someone specific—creating invisible third point in social triangle.

**Photography Reference**:
- Natural portrait: Person looking at something off-camera (the photographer is witness, not subject)
- Conversation: Both looking at same off-camera point (shared interest)
- Children: Looking up at parent not in frame (attachment/reliance)
- Event: Subject looking at something outside frame (story continues beyond)

**Why it works**: Gaze direction creates TRIANGULAR social relationship: subject, gaze target, viewer. When subject looks at camera, it's direct address (advertisement). When subject looks at someone off-camera, viewer becomes WITNESS to relationship.

**Human Behavioral Logic**: We photograph people when they're engaged with others, not when they're posed at camera. Looking at someone else = natural moment.

**Visual Evidence**:
- Subject looking to the left/right outside frame (someone is there)
- Eyes tracking movement off-camera (following someone/something)
- Downward gaze with slight smile (internal thought about off-camera person)
- Upward gaze at someone not in frame (worship/trust/love)

**Prompt Vocabulary**:
```
- "looking at something outside frame left"
- "eyes tracking someone walking away"
- "gaze downward with soft smile, thinking of someone off-camera"
- "looking up at person outside frame"
- "watching something beyond frame edge with full attention"
```

**Integration Rules**:
- GAZE DIRECTION should have IMPLICIT TARGET (not random)
- If subject looks left, ensure something LEFT of frame is visually implied
- Avoid "distant unfocused gaze" (looks like rendering error)
- Gaze should be ENGAGED, not vacant (viewer should wonder "what are they looking at?")

**Anti-AI Benefit**: AI defaults to "looking at camera" or "neutral forward." The specific gaze direction implying specific target off-camera is a learned social behavior.

**Example Prompt Fragment**:
```
"...candid portrait, young woman looking to left outside frame, 
smile suggesting she's watching someone she knows enter space, 
soft bokeh background, natural light from window..."
```

---

#### SOC-13: TOUCH AND CONTACT EVIDENCE

**Problem**: AI shows isolated bodies. Real social photos show bodies in contact—touching is the ultimate social proof.

**Photography Reference**:
- Casual intimacy: Elbow touching, shoulder pressed together
- Romantic: Hand holding, heads touching, arm around waist
- Family: Parent's hand on child's shoulder, holding child's hand
- Friendship: Arm around friend's shoulders, leaning into each other

**Why it works**: Physical contact is the most direct social bond evidence. Bodies touching = comfort, intimacy, relationship. Even casual touch (elbow against elbow) signals social closeness.

**Human Behavioral Logic**: We unconsciously photograph ourselves in contact with people we like—touching is how we confirm social bonds in photos.

**Visual Evidence**:
- Hand on shoulder (comfort/protective)
- Arms linked (casual intimacy)
- Heads touching (romantic/familial)
- Elbows touching (casual friendship)
- Hand holding hand (romantic/family/close friendship)

**Prompt Vocabulary**:
```
- "friend's arm around shoulders, visible at frame edge"
- "hand resting on lower back, guiding gesture"
- "linked arms, elbows bent"
- "fingers intertwined on table surface"
- "forehead touching, eyes closed"
```

**Integration Rules**:
- Touch should be CONGRUENT with relationship type (romantic vs. friendship vs. family)
- Touch location matters: hand on shoulder = protective; hand on waist = romantic
- Avoid "floating touch" where hands seem to hover without proper grip/pressure
- If cropping touch point, ensure anatomy makes sense (can't see hand through jacket sleeve)

**Anti-AI Benefit**: AI generates "touch" as overlaying elements without understanding pressure, grip, or contact physics. Real touch has weight and pressure.

**Example Prompt Fragment**:
```
"...casual couple photo, male friend's arm around female's shoulder, 
hand visible at collarbone, both looking off-camera together, 
warm evening light, shot on Sony 35mm f/1.4..."
```

---

#### SOC-14: SOCIAL MOTION BLUR (ACTIVITY EVIDENCE)

**Problem**: AI renders static, posed moments. Real social photos capture motion—people in the middle of doing things, not just being.

**Photography Reference**:
- Street: Pedestrians mid-stride, legs in motion
- Events: Someone laughing mid-breath, hair moving in wind
- Sports: Action captured at peak motion
- Dance: Bodies in dynamic pose, fabric/movement blur

**Why it works**: Motion = life happening. A static person looks like a statue; a person in motion looks like a moment captured from flowing time.

**Human Behavioral Logic**: We photograph action, not stillness. "Someone dancing," "someone running," "someone mid-laugh" tells us time is passing, life is happening.

**Visual Evidence**:
- Pedestrian mid-stride, shoe blurred
- Hair/fabric movement blur (wind or motion)
- Facial expression mid-change (laugh building)
- Hand gesture mid-motion (conversation gesture)
- Body tilt suggesting walking/moving

**Prompt Vocabulary**:
```
- "person mid-stride crossing street"
- "hair slightly blurred from wind movement"
- "hand gesture frozen mid-point during conversation"
- "body tilt suggesting forward momentum"
- "smile caught mid-laugh, expression not yet settled"
```

**Integration Rules**:
- Motion blur should be CONSISTENT with direction of movement
- Blur direction should be HORIZONTAL for walking, VERTICAL for jumping
- Expression blur (mid-laugh) should be subtle, not extreme
- Blur on hands/clothes is good; blur on face should be minimal
- If person is running, at least one foot should be visible mid-step

**Anti-AI Benefit**: AI tends to either over-freeze (static statue) or over-blur (unreadable). The specific calibrated motion blur that shows action but maintains legibility is learned from real photography.

**Example Prompt Fragment**```
"...street photography style, woman walking forward with pace blur 
on legs, shopping bag swinging, hair catching wind, candid shot, 
available light, shot on Leica Monochrom..."
```

---

#### SOC-15: ATTENDANT SHADOW (SPATIAL OCCUPATION)

**Problem**: AI rarely renders meaningful shadows. Real photos use shadows as evidence of SPATIAL OCCUPATION—someone was here, something exists beyond what we see.

**Photography Reference**:
- Street: Long shadows suggesting other people not in frame
- Café: Shadow of someone sitting beside subject (chair shadow)
- Window: Shadow of interior activity on curtain
- Beach: Two shadow positions (two people implied, only one visible)

**Why it works**: Shadows are PROOF of three-dimensional existence. A shadow says "something is occupying that space, blocking that light." It's indirect evidence of social presence.

**Human Behavioral Logic**: Real photographers wait for the right shadow—the shadow that implies a person without showing the person. It's visual shorthand for "someone else exists here."

**Visual Evidence**:
- Shadow of chair beside occupied chair (two seats, one taken)
- Long afternoon shadow crossing frame (someone standing off-camera)
- Multiple shadow positions suggesting group (only some in frame)
- Shadow of hand reaching into frame

**Prompt Vocabulary**```
- "two chair shadows on pavement, one occupied"
- "long shadow crossing frame from off-camera figure"
- "shadow suggesting standing person beside seated subject"
- "dual shadow positions implying couple"
- "hand shadow entering from frame edge"
```

**Integration Rules**:
- Shadow direction should be CONSISTENT with implied light source position
- Shadow scale should be PROPORTIONAL to implied figure (shadow too large = unnatural)
- Single shadow is mysterious; multiple shadows = social group
- Avoid "floating shadow" with no apparent source

**Anti-AI Benefit**: AI treats shadows as lighting effects, not social evidence. The concept of "shadow as proof of presence" is a high-level abstraction.

**Example Prompt Fragment**:
```
"...lifestyle photo, afternoon sun casting long shadows, two chair 
shadows visible on café terrace, one occupied by subject, other empty, 
warm golden hour light, shot on Canon 85mm f/1.8..."
```

---

#### SOC-16: ATTENTIONAL FOCUS (LOOKING AT SAME THING)

**Problem**: AI shows people with no common focus. Real social photos show multiple people ALL looking at the SAME thing—creating shared social experience.

**Photography Reference**:
- Concert: Everyone looking at stage (shared experience)
- Street: Group looking at something interesting (rubbernecking)
- Dinner: All looking at table center (shared meal)
- Tutorial: Everyone looking at same phone screen

**Why it works**: Shared attention = shared experience = social bond. When we see a group all looking at one thing, we feel the social cohesion.

**Human Behavioral Logic**: We photograph moments of collective attention—"everyone saw this" is a social statement.

**Visual Evidence**:
- Three people all looking at same off-screen point (phone, window, street)
- Concert crowd heads tilted up in same direction
- Couple at dinner both looking at plate then up at each other
- Street scene with multiple people tracking same moving object

**Prompt Vocabulary**:
```
- "group of three all looking at same point off-camera"
- "crowd at concert all heads tilted upward"
- "couple at table looking at each other then at phone together"
- "multiple pedestrians tracking same moving figure"
- "friends gathered around phone screen, heads close"
```

**Integration Rules**:
- Multiple people's gaze should be IDENTICAL direction
- Gaze should be at SPECIFIC thing (phone screen, stage, person) not vague
- Eye contact between in-frame subjects should break shared gaze occasionally (natural)
- Maximum 5 gaze-points in frame to avoid "crowd" look

**Anti-AI Benefit**: AI tends to have subjects look in slightly different directions (averaging). Getting multiple people to look EXACTLY at the same point is difficult and signals authentic social moment.

**Example Prompt Fragment**:
```
"...candid moment, three friends on street all looking at same 
point off-camera right, expressions of amusement, heads close 
together, shallow depth of field, natural light..."
```

---

### Category C: Social Context Density (SOC-17 through SOC-22)

---

#### SOC-17: ENVIRONMENTAL SOCIAL EVIDENCE (SPACE DESIGNED FOR OTHERS)

**Problem**: AI shows spaces as empty stages. Real photos show spaces designed for SOCIAL USE—chairs arranged for conversation, tables for gathering.

**Photography Reference**:
- Restaurant: Two chairs at table for two (implying date/friend)
- Bar: Multiple stools at counter, some pushed back (recently occupied)
- Park: Bench designed for three (family implied)
- Beach: Two lounge chairs together, towels spread (couple/friends)

**Why it works**: Furniture arrangement implies social purpose. A table for two = romantic/friendship. A bench for three = family/groups. Empty but arranged = recent occupation.

**Human Behavioral Logic**: We photograph in spaces that show social intent—the café was designed for conversation, the bar for gathering.

**Visual Evidence**:
- Table set for two (two cups, two napkins, two chairs)
- Bar counter with some stools pushed back (people recently left)
- Park bench with space for three, one occupied
- Cinema seats with drinks in adjacent cup holders

**Prompt Vocabulary**:
```
- "café table set for two, one chair occupied"
- "bar counter with three stools pushed back, one person sitting"
- "park bench designed for three, two spots empty"
- "beach lounge chairs side by by, towels spread"
- "restaurant table with multiple place settings"
```

**Integration Rules**:
- Furniture should be ARRANGED for social use (not randomly placed)
- Empty seats should show EVIDENCE of recent occupation (jacket, drink, bag)
- The number of seats should EXCEED the number of people in frame (implying others)
- Arrangement should feel CASUAL, not formal (staged = less real)

**Anti-AI Benefit**: AI generates spaces as neutral backgrounds. The concept of "designed for social use" requires understanding of human behavior and space design.

**Example Prompt Fragment**:
```
"...cozy izakaya scene, small table set for two with Yakitori 
and beer, one seat occupied, other chair slightly pulled out 
with jacket draped, warm lantern light..."
```

---

#### SOC-18: TEMPORAL SOCIAL EVIDENCE (WHAT JUST HAPPENED)

**Problem**: AI shows frozen moments with no past or future. Real photos show evidence of TIME PASSING—things in progress, not complete.

**Photography Reference**:
- Meal: Half-eaten plate, drink with ice melted, chopsticks resting
- Party: Decorations half-set up, presents half-wrapped
- Work: Open laptop, coffee cup half-finished, papers scattered
- Beach: Sand marked by body imprint, towel half-folded

**Why it works**: Temporal evidence says "this is a PAUSE in ongoing life, not a frozen moment." It's proof that time exists and has passed.

**Human Behavioral Logic**: We photograph things IN PROGRESS—we don't photograph finished, complete moments. Half-eaten = hunger, not performance.

**Visual Evidence**:
- Food half-eaten, drink with bite mark, napkin used
- Cigarette butt in ashtray (someone was here recently)
- Body imprint in sand beside subject
- Open book with corner folded, glasses beside it
- Laptop open with cursor blinking (activity paused, not abandoned)

**Prompt Vocabulary**:
```
- "half-eaten ramen bowl, chopsticks resting"
- "beer can with bite, ice mostly melted"
- "sand with body impression beside subject"  
- "open book with spine cracked, reading glasses beside"
- "laptop open, cursor blinking, coffee half-sipped"
```

**Integration Rules**:
- Temporal evidence should be CONSISTENT with subject's activity (half-eaten food when subject is eating)
- "Paused" not "abandoned" (cursor blinking = paused; empty cup = finished)
- Avoid "frozen perfect" food shots (real people don't photograph full untouched meals)
- Melted ice, used napkins, worn pages = authentic time passage

**Anti-AI Benefit**: AI generates "peak moment" perfection. Real life is half-finished, melting, wearing down. Temporal evidence says "time is passing and I'm in it."

**Example Prompt Fragment**:
```
"...lifestyle photo, laptop open on café table, coffee cup half-finished 
with lipstick mark, open notebook with handwritten notes, 
subject looking out window with thinking expression..."
```

---

#### SOC-19: SOCIAL GROUP FORMATION (COUPLE/FRIEND/FAMILY CODING)

**Problem**: AI shows individuals or chaotic crowds. Real photos show specific group structures—couples face each other, friends form clusters, families stand together.

**Photography Reference**:
- Couples: Face-to-face, body angles pointed at each other
- Friends: Cluster formation, not line-up
- Family: Parent-child height gradient, protective positioning
- Colleagues: Formal spacing, facing same direction

**Why it works**: Body positioning encodes relationship type. Couples lean toward each other. Friends form clusters. Family has height/size hierarchy. AI doesn't understand these formations.

**Human Behavioral Logic**: We unconsciously arrange ourselves by relationship—couples face each other for conversation; friends cluster for shared activity; family stands protectively.

**Visual Evidence**:
- Two people facing each other (couple/friend close)
- Circular cluster of three (friends/social group)
- Parent behind child (protective)
- Line formation (colleagues/formal)
- Triangle formation (family hierarchy)

**Prompt Vocabulary**:
```
- "couple facing each other at café table, knees almost touching"
- "three friends in loose circular cluster, phones out"
- "mother standing slightly behind child, hand on shoulder"
- "colleagues in line formation facing same direction"
- "family of three in triangle formation"
```

**Integration Rules**:
- Body angle should be CONSISTENT with relationship (couple = facing; colleagues = parallel)
- Cluster should feel CASUAL not arranged (real friends don't stand in lines)
- Parent-child spatial relationship = protective (adult behind or beside, not ahead)
- Avoid "all facing camera" (posed formal, not social)

**Anti-AI Benefit**: AI generates spatial arrangements randomly. Understanding that specific formations encode specific relationships requires cultural learning.

**Example Prompt Fragment**:
```
"...casual gathering, three friends in loose triangle formation, 
phones in hands, knee almost touching knee, leaning in 
conversation, warm lighting, shot on iPhone..."
```

---

#### SOC-20: PUBLIC INTIMACY (WHERE STRANGERS WITNESS BOND)

**Problem**: AI doesn't understand the spectrum from public formality to private intimacy. Real photos show couples being affectionate in public spaces.

**Photography Reference**:
- Couple on street: Holding hands, arms linked, close walking
- Public transport: Couple sitting close, heads together
- Café: Partners facing each other, hands touching across table
- Park: Intimate conversation, bodies angled in, voices low

**Why it works**: Public displays of affection (even subtle ones) signal strong bonds. Hand-holding, foreheads touching, close proximity = romantic or very close friendship.

**Human Behavioral Logic**: We photograph our close relationships even in public—we want to capture the bond, not just the location.

**Visual Evidence**:
- Holding hands on street
- Arms linked while walking
- Foreheads touching in public
- Hands touching across table
- Walking with bodies pressed close

**Prompt Vocabulary**:
```
- "couple holding hands while walking"
- "arms linked, bodies pressed close walking"
- "foreheads touching at café table"
- "hands touching across dinner table"
- "couple sitting close on public bench, shoulders touching"
```

**Integration Rules**:
- Public intimacy should be SUBTLE (hand-holding more than kissing)
- Age-appropriate intimacy (young couples vs. elderly couples)
- Cultural context (more intimate in some cultures than others)
- Avoid "over-share" (PDA that makes viewer uncomfortable)

**Anti-AI Benefit**: AI tends toward either no contact or exaggerated contact. The calibrated subtle public intimacy is learned from real-world observation.

**Example Prompt Fragment**:
```
"...street photography, young couple walking with arms linked, 
close bodies, the woman's head slightly leaning on man's shoulder, 
evening city lights, candid shot..."
```

---

#### SOC-21: PROFESSIONAL SOCIAL CONTEXT (WORK/ROLE EVIDENCE)

**Problem**: AI shows people without professional identity. Real photos show people in ROLE—chef in kitchen, writer at desk, artist in studio.

**Photography Reference**:
- Chef: Holding ingredient, wearing apron, in kitchen environment
- Writer: Papers scattered, coffee beside laptop, at desk
- Artist: Paint on hands, surrounded by materials, in workspace
- Musician: Instrument nearby, sheet music open, in practice space

**Why it works**: Professional identity is a key social dimension. We are our work. Showing someone in their professional context adds social depth.

**Human Behavioral Logic**: We photograph people DOING their work—the photographer documenting the chef cooking, not just the chef standing there.

**Visual Evidence**:
- Work attire/costume visible
- Tools of profession present
- Environment implies profession
- Action of work in progress
- Evidence of expertise (worn hands, organized tools)

**Prompt Vocabulary**:
```
- "chef holding fresh ingredient in kitchen, apron dusted with flour"
- "writer at desk surrounded by papers, coffee rings on notebook"
- "artist at work, paint-stained hands, canvas in progress"
- "musician mid-practice, sheet music open, instrument visible"
- "barista making latte art, steam rising, café background"
```

**Integration Rules**:
- Profession should be VISUALLY OBVIOUS (tools, environment, attire)
- Action beats static posing ("making" beats "standing with tools")
- Evidence of expertise > formal credentials (worn hands > degree on wall)
- Avoid "stereotypical" poses (chef smiling at camera = stock photo)

**Anti-AI Benefit**: AI tends to show generic "person with objects." Understanding that specific tools/professions create specific social contexts requires domain knowledge.

**Example Prompt Fragment**:
```
"...documentary style, sushi chef's hands forming rice ball, 
apron with stains, counter with ingredients, serious 
concentration face, natural restaurant lighting..."
```

---

#### SOC-22: CULTURAL SOCIAL CONTEXT (RITUAL/PROCESS)

**Problem**: AI shows generic scenes. Real photos show culturally specific social rituals—tea ceremony, meal prep, greeting ritual.

**Photography Reference**:
- Japanese: Tea ceremony steps, izakaya ordering ritual
- Chinese: Dim sum serving, family meal arrangement
- Korean: BBQ cooking at table, soju pouring ritual
- Western: Wine tasting, bread breaking

**Why it works**: Cultural rituals are deeply social—they encode group membership, tradition, belonging. Photographing someone in the middle of a ritual shows social role.

**Human Behavioral Logic**: We photograph meaningful cultural moments—not just "eating" but "eating in this specific cultural way that shows who I am."

**Visual Evidence**:
- Ritual object positions (teapot pointing where, chopsticks placed how)
- Sequence evidence (something happening in traditional order)
- Group members in traditional roles
- Culturally specific clothing/objects
- Gesture showing ritual knowledge

**Prompt Vocabulary**:
```
- "hands pouring tea in traditional ceremony position"
- "soju being poured by elder, younger person's hand below cup"
- "dim sum being served from cart, family watching"
- "chopsticks positioned correctly beside bowl"
- "hands clapping before meal, traditional gesture"
```

**Integration Rules**:
- Cultural context should be ACCURATE (ritual objects positioned correctly)
- If uncertain, show GENERAL cultural context rather than specific ritual error
- Ritual gesture should be in PROGRESS, not completed
- Group members should be in TRADITIONAL positions (younger serving elder)

**Anti-AI Benefit**: AI has difficulty with culturally specific spatial arrangements. Getting ritual object positions correct requires cultural training data.

**Example Prompt Fragment**:
```
"...intimate family dinner, grandmother serving soup with ladle, 
younger family members waiting with bowls, steam rising, 
traditional layout, warm interior light..."
```

---

### Category D: Off-Screen Human Existence (SOC-23 through SOC-25)

---

#### SOC-23: AUDITORY IMPLICATION (SOUND EVIDENCE)

**Problem**: AI shows silent images. Real photos imply SOUND—the visual evidence of something that makes noise, or the reaction to sound.

**Photography Reference**:
- Concert: Hands over ears (protecting from loud music)
- Street performer: Crowd with phones recording (sound happening)
- Restaurant kitchen: Chef reacting to sizzle
- Bar: Person wincing at loud laugh

**Why it works**: Sound implies activity and environment. Visual evidence of loudness = social context (concert, construction, celebration).

**Human Behavioral Logic**: We photograph reactions to sound—someone covering ears, laughing at joke, wincing at noise. These are social moments.

**Visual Evidence**:
- Hands over ears (loud environment)
- Phone held up recording (sound worth capturing)
- Mouth open mid-speech (conversation happening)
- Wincing expression (too loud for comfort)
- Eyes closed (music too loud, surrendering to it)

**Prompt Vocabulary**:
```
- "hands over ears at concert"
- "phone held up recording street musician"
- "expression wincing at loud sudden noise"
- "mouth open mid-laugh, eyes squinting"
- "person swaying with eyes closed, music overwhelming"
```

**Integration Rules**:
- Sound evidence should match ENVIRONMENT (concert = hands over ears; quiet café = no)
- Reaction should be PROPORTIONAL to implied sound level
- Audio implies SPATIAL BOUNDARY (someone nearby is making this sound)
- Avoid "deafening silence" visuals (unless silence itself is the story)

**Anti-AI Benefit**: Sound is non-visual—implying it requires metaphorical visual thinking. AI doesn't understand that "hands over ears" means "it's loud here."

**Example Prompt Fragment**:
```
"...street festival scene, woman covering ears with expression 
of overwhelmed joy, colorful crowd around her, music notes 
implied in air with motion blur, available light..."
```

---

#### SOC-24: OFF-SCREEN SHADOW/VOICE EVIDENCE

**Problem**: AI shows bounded frames. Real photos show evidence of someone BESIDE or BEYOND the frame—shadows falling across, voice implied by reaction.

**Photography Reference**:
- Someone's shadow falling across subject (off-screen person standing)
- Person responding to unheard comment (voice implied)
- Gaze directed at empty space (someone standing there)
- Hand gesture answering unseen question

**Why it works**: Off-screen shadow or reaction implies another person EXISTS even though not photographed. It's the photographic equivalent of dramatic irony.

**Human Behavioral Logic**: We photograph people responding to things we can't see—proof that the world extends beyond the frame.

**Visual Evidence**:
- Shadow of another person falling across subject
- Person mid-response to unheard comment
- Gaze at empty space with expression
- Hand gesture answering invisible question

**Prompt Vocabulary**:
```
- "shadow of unseen person falling across subject from left"
- "response gesture to comment not heard by viewer"
- "laughing at something someone just said off-camera"
- "gaze fixed on empty space as if someone standing there"
- "hand reaching toward something outside frame"
```

**Integration Rules**:
- Shadow direction should be CONSISTENT (from visible off-camera direction)
- Subject's reaction should be CONTEXTUALLY APPROPRIATE (responding to comment = smile; responding to threat = alarm)
- Off-screen presence should have SPATIAL LOGIC (standing where shadow falls)
- Avoid "ghost" feeling—presence should be warm, not spooky

**Anti-AI Benefit**: AI doesn't understand dramatic irony. The concept of "someone exists but isn't shown" requires viewer intelligence that AI can't replicate.

**Example Prompt Fragment**:
```
"...lifestyle photo, woman on bench with shadow of another person 
falling across her from right side, she is looking toward that 
shadow with smile, afternoon light creating long shadows..."
```

---

#### SOC-25: TRANSITIONAL PRESENCE (ABOUT TO ARRIVE/DEPART)

**Problem**: AI shows static scenes. Real photos capture TRANSITION—someone arriving, someone about to leave. Life in between states.

**Photography Reference**:
- Arrival: Person looking at door/phone, checking time, standing near entrance
- Departure: Person at door, bag in hand, saying goodbye to someone off-frame
- Waiting: Person checking phone, looking at entrance
- Meeting: Two people making eye contact across space

**Why it works**: Transitional states have narrative tension—someone is about to enter or leave the subject's life momentarily. This creates anticipation.

**Human Behavioral Logic**: We photograph the moment before and after—waiting for friend, saying goodbye to lover, meeting eyes across room.

**Visual Evidence**:
- Checking phone/wristwatch (waiting for arrival)
- Standing near entrance looking at door (about to meet)
- Bag in hand at door (about to leave)
- Two people making eye contact across space (meeting in progress)
- Person mid-step entering frame (arriving)

**Prompt Vocabulary**:
```
- "looking at phone with anticipation, checking entrance"
- "standing near door with bag, saying goodbye to off-camera person"
- "two people making eye contact across crowded room"
- "person mid-step entering frame, arriving"
- "standing with suitcase handle, watching someone approach"
```

**Integration Rules**:
- Transitional state should be UNAMBIGUOUS (looking at door = waiting; bag = leaving)
- Direction of movement should be VISUALLY CLEAR (arriving = into frame; leaving = out of frame)
- "About to" moments have higher narrative tension than static states
- Avoid "frozen" transitions—show motion/blur to suggest movement

**Anti-AI Benefit**: AI tends to show completed states (arrived, departed) not transitional ones. "About to" requires temporal understanding that AI lacks.

**Example Prompt Fragment**:
```
"...street scene, young man standing near café entrance looking 
at phone then up at door, suitcase handle in other hand, 
arrival expression, morning light, shot on Leica..."
```

---

## PART 4: INTEGRATION ARCHITECTURE

### Token Combination Rules

1. **Primary + Secondary + Ambient Structure**
   - Primary: One strong social density token (cropped companion, touch, gaze)
   - Secondary: One ambient token (second drink, stranger crossing, shadow)
   - Ambient: Environmental evidence (furniture arrangement, cultural context)

2. **Density Budget**
   - Maximum 4-5 social density tokens per image
   - Overload = chaos, not authenticity
   - Some tokens are self-sufficient (SOC-09 cropped companion = full social density)

3. **Narrative Consistency**
   - All tokens should point to SAME social narrative
   - Table for two + second drink + couple facing = romantic date
   - Table for four + work laptop + name card = professional lunch

### Token Override Hierarchy

When tokens conflict, RESOLVE IN ORDER:
1. Proximity/touch > gaze (touch is stronger social bond signal)
2. Transitional > static (arrival/departure > arrived/departed)
3. Specific > generic (specific stranger > anonymous crowd)
4. In-progress > complete (mid-action > frozen peak)

### Anti-AI Signature Detection

The following token COMBINATIONS are strongest AI-detection resisters:
- SOC-01 (cropped companion) + SOC-09 (partial body) = authentic social framing
- SOC-06 (camera holder) + SOC-16 (shared gaze) = meta-documentation
- SOC-08 (social object) + SOC-18 (temporal evidence) = time passing
- SOC-23 (auditory) + SOC-24 (off-screen shadow) = world extends beyond frame

---

## PART 5: IMPLEMENTATION GUIDELINES

### Prompt Construction for V18

**Structure**:
```
[Subject] + [Setting] + [SOC Primary] + [SOC Secondary] + [SOC Ambient] + [Technical]
```

**Example (full prompt)**:
```
"casual portrait of young woman in late afternoon café light, 
friend's shoulder cropped at left frame edge (SOC-01), 
other person's hand visible holding coffee cup in background (SOC-02), 
second untouched coffee cup on table beside her (SOC-04), 
café table set for two with chair slightly pulled out (SOC-17), 
shot on Fujifilm X100V, f/2.0, natural light, authentic moment"
```

### Quality Checklist

For each generated image, VERIFY:
- [ ] At least one SOC token from Category A (visible social presence)
- [ ] Evidence of implied others (off-screen shadow, extra drink, etc.)
- [ ] Social distance/proximity calibrated to relationship type
- [ ] Temporal evidence if scene is interior (food half-eaten, drink partly finished)
- [ ] No static "posed for camera" composition

---

## PART 6: SUMMARY

### Why This Works

V17 failed because it treated social context as vague atmosphere. V18 succeeds because it treats social context as **specific, visually verifiable evidence**. Every token represents a real pattern from billions of real human photographs.

The Social Density Engine encodes:
1. **Physical proximity** (close enough to touch)
2. **Temporal pause** (scene is paused, not frozen)
3. **Narrative extension** (story continues beyond frame)
4. **Specific others** (not generic crowd, but specific implied person)
5. **Cultural specificity** (this ritual, not generic celebration)

### Key Innovation

The engine shifts from SUBJECT-CENTERED to EVIDENCE-CENTERD prompting. Instead of "photo of person with friends," we prompt "photo showing evidence that friends exist/were here/are coming."

This is why real photos feel alive: they contain invisible social infrastructure that AI has been missing.

---

*Document Version: 1.0*  
*Research Classification: V18 Social Density Engine*  
*Status: Complete - 25 Tokens Designed*