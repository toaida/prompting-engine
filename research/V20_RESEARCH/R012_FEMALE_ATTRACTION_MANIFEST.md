# R012_FEMALE_ATTRACTION_MANIFEST
### V20 research task
### Owner: Lucy
### Priority: P1
### Status: Research complete — production validation required

---

## objective

Understand which non-explicit female behaviours consistently attract and retain male viewer attention in photography and social media content.

This file does not study pornography, explicit content, fetish material, or technical photography quality. It studies attraction psychology inside safe lifestyle photography: micro-expression, camera awareness, feminine body language, outfit psychology, and viewer retention.

The working question is simple:

```text
What makes a viewer continue looking at the same girl?
```

Not:

```text
What makes a technically good photograph?
```

---

## research basis

This manifest combines existing lil.troublr V19/V20 systems with external psychology and perception research.

Internal sources used:

- `V19_RESEARCH/FACE_ATTENTION_ENGINE.md`
- `V20_RESEARCH/ATTENTION_ROUTING_ENGINE.md`
- `V20_RESEARCH/CAMERA_RELATIONSHIP_ENGINE.md`
- `V20_RESEARCH/BODY_LANGUAGE_ATTRACTION_ENGINE.md`
- `V20_RESEARCH/R011_MOMENT_CAPTURE_MANIFEST.md`

External research anchors:

- Direct gaze captures attention and can increase perceived attractiveness: <https://pmc.ncbi.nlm.nih.gov/articles/PMC4072644/>
- Eye and gaze processing are central to social cognition: <https://pmc.ncbi.nlm.nih.gov/articles/PMC3925117/>
- Smile authenticity is judged through dynamic facial movement and facial mimicry, not static prettiness alone: <https://pmc.ncbi.nlm.nih.gov/articles/PMC4053432/>
- Duchenne and non-Duchenne smiles signal different social distance and warmth: <https://pmc.ncbi.nlm.nih.gov/articles/PMC5554339/>
- Human body movement matters in mate selection and social perception; the way a movement is performed can matter more than the category of pose: <https://pmc.ncbi.nlm.nih.gov/articles/PMC10480986/>

---

# 1. findings

## finding 1: attraction begins with social readability, not exposure

Male viewer attention is held when the viewer can read a living social state from the image.

The strongest images do not merely say:

```text
She is beautiful.
```

They say:

```text
She just noticed something.
She is deciding whether to smile.
She is reacting to a friend.
She is comfortable enough to forget the camera.
She knows the camera exists, but life is still happening.
```

This matters because attraction is partly a decoding loop. The viewer keeps looking because the image offers a small emotional puzzle.

Prompt implication:

```text
Write behaviour before beauty.
Write reaction before pose.
Write social cause before facial expression.
```

Failure mode:

```text
beautiful girl smiling at camera, attractive pose, perfect lighting
```

Why it fails:

The emotional question is already solved. There is no reason to keep looking.

---

## finding 2: the highest-retention expression is incomplete

Completed expressions are easy to process. Incomplete expressions hold attention because the viewer mentally finishes them.

High-retention micro-expressions:

- smile just beginning
- laugh caught halfway
- mouth corner lifted on one side
- eyes noticing before mouth reacts
- embarrassed smile being suppressed
- playful smirk before full smile
- shy look-away with the smile still visible

Low-retention expressions:

- full symmetrical smile held for camera
- influencer pout
- blank glamour stare
- overacted laugh
- exaggerated wink
- face arranged into a known selfie expression

The best expression often lives between two emotional states:

```text
neutral → recognition
laughing → camera-aware
shy → amused
confident → teasing
focused on task → interrupted by friend
```

Prompt implication:

```text
Capture the expression before it completes.
```

Useful wording:

```text
her smile has just started, not fully formed
one corner of her mouth lifts before the rest of her face follows
eyes notice the camera first, mouth still deciding whether to smile
caught between laughing at her friend and realizing the camera is on her
```

---

## finding 3: eye contact works only when it has a cause

Direct gaze is powerful. Research on gaze direction shows direct gaze faces are viewed longer than averted-gaze faces, and can be rated as more attractive.

But in prompt generation, direct gaze is dangerous because AI turns it into posing.

Direct eye contact works when:

- she just noticed the camera
- a friend called her name
- the photographer interrupted an action
- she caught the photographer taking the photo
- she is responding to someone she trusts
- the gaze is brief, transitional, or emotionally caused

Direct eye contact fails when:

- she stares without reason
- body is squared to camera
- hands have no task
- background has no event residue
- expression is held like a profile photo

Prompt implication:

```text
Eye contact must be explained by an event.
```

Useful wording:

```text
she glances into the camera because her friend just said her name
brief eye contact, only for a second, while her hands remain busy with the bag zipper
she catches the camera and gives a small sideways smile before looking back down
```

Avoid:

```text
seductive eye contact
intense stare
posing directly at the camera
looking into the camera beautifully
```

---

## finding 4: asymmetric smiles feel more human than perfect smiles

Perfect symmetry reads as artificial. A slight asymmetry makes the expression feel like it is happening, not being held.

Attractive asymmetry signals:

- one mouth corner lifts first
- one cheek compresses more than the other
- one eye narrows slightly from a real smile
- eyebrow imbalance during recognition
- head tilt creates uneven facial tension
- shoulder position changes expression context

The key is subtlety. Too much asymmetry becomes sarcasm, contempt, or cartoon acting.

Prompt implication:

```text
Use low-intensity asymmetry as proof of human timing.
```

Useful wording:

```text
slight asymmetric smile, one corner lifting first
one cheek raised from a half-contained laugh
one eyebrow slightly higher because she just caught the camera
```

Avoid:

```text
smirk aggressively
crooked grin
villain smile
exaggerated asymmetric face
```

---

## finding 5: shy reactions attract when they contain permission, not fear

Shy behaviour can be attractive because it creates vulnerability and social warmth. But it must not read as discomfort, coercion, fear, or being cornered.

Good shy reaction:

```text
she noticed the camera, looks down for half a second, smiles despite herself, then keeps doing what she was doing
```

Bad shy reaction:

```text
she is embarrassed, trapped, hiding, pressured, or trying to escape the camera
```

Safe shy signals:

- quick look away with a smile still visible
- hand briefly near mouth, then relaxed
- shoulder turns away slightly, then returns
- eyes glance down at her own hands
- smile appears after the look-away, not before

Prompt implication:

```text
Shy must mean socially warm, not unsafe.
```

Useful wording:

```text
shy but amused
caught off guard but happy about it
briefly looks down, smiling to herself
not ready for the photo, but comfortable with the friend taking it
```

Avoid:

```text
scared
nervous in a threatened way
submissive
helpless
cornered
```

---

## finding 6: playful reaction flips the power dynamic

Playfulness retains attention because the viewer feels the subject has agency. She is not passively being looked at. She notices, judges, teases, and returns energy.

Strong playful patterns:

- catches the camera
- mock accusation
- slight squint
- sideways smile
- points at the photographer casually
- half-laughing "what are you doing?" face
- continues the original action while acknowledging the camera

Prompt implication:

```text
Make playfulness a reaction, not a performance.
```

Useful wording:

```text
she catches her friend taking the photo and gives a small accusing smile
eyes narrow with playful recognition, mouth pulling sideways before she laughs
one hand still holding the cup while she points at the camera with the other
```

Avoid:

```text
sexy teasing pose
seductive performance
finger on lips
forced wink
```

---

## finding 7: confidence is relaxed control, not dominance theatre

Attractive confidence is not always big posture. In lifestyle content, the stronger signal is relaxed control: she is comfortable in the space, not begging the camera for approval.

Good confidence signals:

- stable weight distribution
- relaxed shoulders
- unhurried hand movement
- casual gaze return
- posture settled into environment
- camera awareness without self-conscious correction
- outfit worn as normal clothing, not displayed as costume

Bad confidence signals:

- chin lifted too high
- shoulders forced back
- runway posture in daily environment
- all limbs arranged for display
- direct stare with no task
- perfect model symmetry

Prompt implication:

```text
Confidence should look like comfort under observation.
```

Useful wording:

```text
she notices the camera without fixing herself
relaxed weight on one leg, shoulders soft, still listening to her friend
comfortable enough to keep eating while the camera is there
```

---

## finding 8: camera awareness should be peripheral or reactive, not influencer-performance

The strongest safe lifestyle attraction usually sits between these camera states:

```text
LEVEL 1: knows camera exists, keeps living
LEVEL 2: notices camera and reacts genuinely
```

Less useful states:

```text
LEVEL 0: unaware — can work, but often lacks connection
LEVEL 3: engaged — useful sometimes, but risks posing
LEVEL 4: performing — usually influencer-coded
```

The best image often catches the transition:

```text
task → camera recognition → micro-expression → return to task
```

Prompt implication:

```text
The camera should be part of the social scene, not the reason the whole scene exists.
```

Useful wording:

```text
she knows her friend is taking a photo but does not stop what she is doing
camera exists in her peripheral awareness, not controlling her body
she reacts naturally for one second, then returns to the original task
```

Avoid:

```text
influencer pose
posing for Instagram
perfect selfie performance
glamour photoshoot energy
```

---

## finding 9: feminine body language is created by weight, softness, and task residue

Attraction in body language does not come from static body display. It comes from visible physics: weight being carried, shifted, supported, or relaxed.

High-value feminine body language:

- weight resting on one hip because she is waiting
- shoulder softening because she is listening
- hair touched because wind or humidity moved it
- leaning because a wall, railing, chair, or friend is supporting her
- sitting because she is tired, waiting, eating, checking phone, or talking
- hands still occupied by a real object
- body angled because attention is split between camera and task

Prompt implication:

```text
Body language must have a physical reason.
```

Useful wording:

```text
weight shifted onto one leg from waiting too long
one shoulder slightly raised because the bag strap is slipping
leaning on the railing while still looking at the ferry lights
sitting sideways on the low step, knees angled because the space is narrow
```

Avoid:

```text
sexy posture
hourglass pose
arched body
body-first composition
perfect feminine pose
```

---

## finding 10: hair-touching works only when it is functional

Hair-touching is attractive when it looks like a real maintenance action. It fails when it becomes an obvious beauty gesture.

Good hair-touch causes:

- wind moved fringe
- humidity made flyaways stick
- she is tucking hair behind ear to listen
- she is clearing hair from face while eating
- she is checking mirror reflection quickly
- wet hair needs pushing back
- bag strap caught a strand

Prompt implication:

```text
Hair touch needs a cause and should interrupt another action.
```

Useful wording:

```text
tucking one loose strand behind her ear while still listening
pushing wind-blown hair away from her cheek, smile not fully formed
fingers caught halfway in her hair because someone called her name
```

Avoid:

```text
sensually touching hair
running fingers through hair for the camera
hair flip pose
```

---

## finding 11: outfit attraction comes from social plausibility

Outfit psychology is not about maximum reveal. It is about whether the outfit makes her socially desirable in that scene.

Strong outfit signals:

- fitted vs oversized contrast
- casual femininity
- daily practicality
- clean but not over-styled
- fabric responding to posture
- outfit appropriate to location
- one memorable detail, not a costume stack

Examples:

- fitted ribbed top under oversized cardigan
- loose shirt with fitted shorts
- soft knit top with practical tote bag
- simple dress with sneakers in a real street setting
- oversized hoodie with neat hair and small earrings
- casual tank with open shirt layer and lived-in bag

Why it works:

The viewer reads her as someone who exists in a social world. She dressed for life, friends, weather, errands, dinner, transit, or a casual night out. That beats a technically attractive but socially empty outfit.

Prompt implication:

```text
Outfit must explain lifestyle, not just body shape.
```

Useful wording:

```text
fitted-and-loose contrast: ribbed white top under oversized pale blue shirt
casual feminine outfit chosen for a humid HK afternoon, not a photoshoot
soft cardigan slipping slightly from normal movement, not styled to reveal
```

Avoid:

```text
revealing outfit
body-hugging dress for male attention
sexy clothing
maximum curves
```

---

## finding 12: viewer retention comes from unresolved social meaning

The viewer keeps looking when the image withholds a small piece of meaning.

Retention questions:

- Why is she smiling like that?
- What did her friend just say?
- What is she looking at off-frame?
- Did she notice the camera or not?
- Is she about to laugh?
- Why is she slightly embarrassed?
- What was she doing before the photo interrupted her?

The best image should answer one thing and leave one thing unresolved.

Weak image:

```text
She is pretty and posing.
```

Strong image:

```text
She was searching her bag, heard her friend call her name, looked up too quickly, smiled before she fully understood the joke, and one hand is still inside the bag.
```

Prompt implication:

```text
Every attractive image needs a tiny unresolved social event.
```

---

# 2. prompt rules

## rule 1: behaviour first, beauty second

Write:

```text
She was already [doing task] when [small event] happened.
```

Then add attractiveness through expression, posture, outfit, and social warmth.

Do not start with body, sexiness, attractiveness, or exposure.

---

## rule 2: micro-expression must have timing

Bad:

```text
teasing smile
```

Good:

```text
a teasing smile just beginning on one side of her mouth after she catches the camera
```

The expression needs:

- trigger
- onset
- partial completion
- body still in old task

---

## rule 3: camera awareness must be named

Use one of these states:

```text
camera peripheral
camera reactive
camera recognition
friend-shot awareness
brief lens glance
caught-camera response
```

Avoid vague camera language like:

```text
looking at camera attractively
posing naturally
candid pose
```

---

## rule 4: eye contact must be short or socially justified

Good eye contact:

```text
brief eye contact because her friend called her name
```

Bad eye contact:

```text
staring into the camera with confidence
```

---

## rule 5: body language must be caused by environment or task

Every posture needs a reason.

Examples:

```text
leaning because the queue is taking too long
shoulder raised because tote strap is slipping
sitting sideways because the step is narrow
weight shifted because she is waiting for the lift
hair tucked because humidity loosened strands near her cheek
```

---

## rule 6: outfit must be socially believable

The outfit should answer:

```text
Where is she going?
What kind of day is this?
Who might she be meeting?
Why would she dress like this here?
```

If the outfit cannot answer these questions, it will feel like costume styling.

---

## rule 7: no influencer performance language

Avoid:

```text
model pose
sexy pose
seductive look
perfect body
glamour shot
posing for Instagram
```

Use:

```text
friend-shot
ordinary task
camera recognition
unfinished smile
task residue
environmental cause
comfortable under observation
```

---

## rule 8: attractiveness should emerge from social desirability

Social desirability cues:

- has friends
- belongs in the place
- looks comfortable in public
- has a life outside the photo
- reacts warmly to people
- outfit fits her daily context
- not trying too hard
- not isolated as an object

Prompt line:

```text
she feels socially alive, like someone whose day continued before and after this frame
```

---

## rule 9: include one unresolved viewer question

Add one line such as:

```text
the viewer cannot tell what her friend just said
something off-frame made her smile before the camera mattered
her expression is halfway between recognition and laughter
```

---

## rule 10: protect SFW boundary

Do not use:

```text
pornographic framing
explicit anatomy
fetish cues
youth-coded styling
school-coded clothing
helplessness
coercion
body-first camera angle
```

Use:

```text
adult lifestyle realism
safe social photography
non-explicit attraction
face-led attention
body language through task and physics
```

---

# 3. positive examples

## example 1: friend calls name

```text
Adult Hong Kong woman in a casual fitted white ribbed top under an oversized pale blue shirt, standing outside a small cha chaan teng at night. She was searching inside her tote bag when her friend called her name. Her eyes lift toward the camera first, head only halfway turned, one corner of her mouth just starting to smile. One hand is still inside the open bag, receipt folded between two fingers. Relaxed weight on one leg from waiting, shoulders soft, camera-aware for only a second before returning to the bag. Slight asymmetric smile, warm but unfinished. Social, everyday, non-explicit attraction.
```

Why it works:

- task exists before photo
- camera eye contact has cause
- micro-expression is unfinished
- outfit has fitted vs oversized contrast
- body remains committed to original action

---

## example 2: caught-camera playful response

```text
Adult woman sitting sideways on a low concrete step near a Hong Kong ferry pier, loose cardigan over a fitted grey tank, simple earrings, small crossbody bag beside her. She was laughing at something off-frame when she suddenly catches her friend taking the photo. Her eyes narrow slightly with playful accusation, one eyebrow a little higher, mouth pulling sideways before the laugh fully returns. One hand still holds a paper cup, the other hand half-raised as if about to point at the photographer. Shoulders relaxed, knees angled naturally because the step is narrow. The viewer cannot tell what the friend just said.
```

Why it works:

- playful without performance
- subject has agency
- smile is asymmetric and mid-transition
- seated posture is physically justified
- social cause creates retention

---

## example 3: shy but comfortable

```text
Adult woman in an oversized cream hoodie with fitted black shorts and white sneakers, waiting near an apartment lift lobby. She was checking a message when the lift chime sounded and her friend raised the camera. She glances up for half a second, then looks down at her phone with a shy amused smile still visible. Her thumb remains on the phone screen, tote strap slipping slightly from one shoulder. Hair has a few humidity flyaways near the temple. She is caught off guard but comfortable, not hiding, not performing.
```

Why it works:

- shy reaction is safe and warm
- phone creates task residue
- lift chime creates ambient cause
- outfit is casual and socially plausible
- face and hands are out of sync

---

## example 4: confident but not staged

```text
Adult woman leaning lightly against a tiled wall outside a convenience store after buying a drink, fitted black knit top with loose straight-leg jeans, small silver necklace, plastic bag hooked around two fingers. She notices the camera without fixing herself. Her expression barely changes, just a small knowing smile at one corner, eyes meeting the lens for a second while her body stays angled toward the street. Weight settled into the wall from waiting, shoulders relaxed, drink condensation visible on her fingers. The confidence comes from comfort, not posing.
```

Why it works:

- confidence is relaxed control
- wall lean has a task reason
- direct gaze is brief
- outfit is everyday attractive
- object residue proves real context

---

## example 5: hair-touch with cause

```text
Adult woman at an outdoor café table on a humid afternoon, soft knit sleeveless top under an open linen shirt, casual skirt, canvas tote on the chair. A gust from the street pushes a few strands across her cheek while she is reaching for her iced drink. Fingers caught halfway tucking hair behind her ear, eyes glancing toward her friend, smile only beginning because someone just made a small joke. The shirt sleeve sits unevenly from movement, drink ring visible on the table, phone face-up beside the cup.
```

Why it works:

- hair-touch is functional
- smile has social trigger
- outfit is feminine but everyday
- environment causes body behaviour
- attention route goes face → hand → object → social question

---

# 4. failure examples

## failure 1: perfect camera smile

```text
Beautiful woman looking directly at the camera with a perfect smile, standing in a stylish outfit, elegant pose, attractive body language.
```

Why it fails:

- no event
- no task residue
- smile is complete
- body is arranged for camera
- viewer has nothing to decode

Fix:

```text
She was tightening the strap of her tote when her friend called her name; eyes lift first, smile just beginning, fingers still holding the strap.
```

---

## failure 2: forced shy performance

```text
Shy girl covering her face, embarrassed, looking away from the camera.
```

Why it fails:

- can read as unsafe or pressured
- no comfort signal
- no reason for camera
- too generic

Fix:

```text
Adult woman glances down at her phone with a shy amused smile after noticing her friend taking the photo; she is caught off guard but comfortable.
```

---

## failure 3: hair-touch as beauty pose

```text
Woman sensually touching her hair and staring into the camera.
```

Why it fails:

- performance-coded
- body-first energy
- no environmental cause
- too explicit in intent even without explicit content

Fix:

```text
Humidity loosened a few strands near her cheek, and her fingers pause halfway through tucking them behind her ear while she laughs at someone off-frame.
```

---

## failure 4: outfit without social logic

```text
Attractive woman in tight clothes showing her figure on the street.
```

Why it fails:

- body-first
- no destination
- no social world
- outfit reads as display, not lifestyle

Fix:

```text
Fitted ribbed top under an oversized shirt, chosen for a humid evening walk to dinner; the shirt sleeve sits unevenly because she has been carrying a tote all afternoon.
```

---

## failure 5: confidence as dominance theatre

```text
Confident woman staring intensely into camera, shoulders back, chin raised, powerful pose.
```

Why it fails:

- reads like editorial direction
- too static
- no ordinary task
- eye contact has no cause

Fix:

```text
She notices the camera without correcting her posture, relaxed weight against the railing, one hand still holding a drink, small knowing smile forming only on one side.
```

---

# 5. prompt-ready manifest

Use this block when generating safe attractive lifestyle prompts.

```text
FEMALE_ATTRACTION_MANIFEST_R012:
Create non-explicit attraction through social readability, not exposure.
The image must show an adult woman inside an ordinary lifestyle moment.
An ordinary task must exist before the camera: checking phone, searching bag, waiting, eating, talking, choosing an item, adjusting strap, tucking hair, sitting down, listening to a friend.
A small event interrupts the task: friend calls her name, camera is noticed, phone vibrates, lift chime sounds, wind moves hair, someone off-frame says something, queue moves, ferry arrives, drink spills slightly.
Her reaction must be unfinished: smile just beginning, one mouth corner lifting first, eyes noticing before mouth reacts, laugh caught halfway, quick shy look-down with smile still visible, playful accusing glance before laughter returns.
Camera awareness should be peripheral or reactive. She knows the camera exists but does not perform like an influencer. Brief eye contact is allowed only when caused by a social or environmental trigger.
Body language must be physically caused: relaxed weight shift, soft shoulders, leaning because she is waiting, sitting because the step is narrow, hair touch because wind or humidity moved it, shoulder raised because a strap is slipping, hands still occupied by the original task.
Outfit should create everyday social desirability: fitted vs oversized contrast, casual femininity, clean but not over-styled, location-appropriate, fabric responding to posture and weather. Outfit explains lifestyle, not anatomy.
The frame should leave one unresolved viewer question: what did her friend say, what is off-frame, did she notice the camera, is she about to laugh, why is she smiling like that.
Avoid explicit content, pornography, fetish cues, youth-coded styling, school-coded styling, helplessness, coercion, body-first composition, seductive performance language, influencer posing, glamour photoshoot energy.
```

---

# 6. compact prompt rule set

For production prompts, use this order:

```text
1. adult identity + place
2. ordinary task already happening
3. small interruption
4. micro-expression onset
5. face/body out-of-sync detail
6. task residue in hands/objects
7. feminine body language caused by weight/environment
8. outfit psychology: fitted/loose, casual, socially plausible
9. camera awareness level: peripheral/reactive
10. unresolved viewer question
11. SFW boundary and anti-influencer guardrail
```

Template:

```text
Adult woman in [specific place], wearing [socially plausible outfit with fitted/loose contrast]. She was already [ordinary task] when [small interruption] happened. Her eyes [notice / glance / look down] before the rest of her face catches up; [micro-expression] is just beginning, not fully formed. Her body is still committed to [original task]: [hand/object/task residue]. [Posture/weight/shoulder/hair behaviour] is caused by [environment/task]. Camera awareness is [peripheral/reactive], not influencer performance. The viewer cannot fully tell [unresolved social question]. Safe lifestyle photography, non-explicit attraction, adult, social realism.
```

---

# 7. production checklist

Before using a prompt, check:

- Is there an ordinary task before the photo?
- Is there a small interruption?
- Is the expression unfinished?
- Does eye contact have a cause?
- Are face and body out of sync?
- Is there visible task residue?
- Is the body language physically justified?
- Does the outfit belong to the location and day?
- Does the image leave one small question unresolved?
- Does the prompt avoid explicit, fetish, youth-coded, or influencer-performance language?

If any answer is no, rewrite before generation.

---

# 8. one-line operating principle

```text
Attraction retention = adult social warmth + unfinished micro-expression + caused body language + believable outfit + one unresolved social question.
```
