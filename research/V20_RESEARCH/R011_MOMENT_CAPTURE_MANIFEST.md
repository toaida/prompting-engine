# R011_MOMENT_CAPTURE_MANIFEST
### Production-Guided Research Task
### Owner: Lucy
### Priority: P1
### Status: Research Complete — Pending GPT Review + Production Testing

---

## Research Objective

Solve the recurring production failure: images feel posed, as if somebody asked her to stand there. The goal is to make images feel captured: a real-life moment interrupted by a camera.

No new engine, character system, or camera system is proposed. This research focuses only on moment capture, event logic, interruption logic, and reaction logic.

## Research Question

What makes a photograph feel “captured” instead of “posed”?

## Research Sources Considered

- Japanese gravure off-shot photography
- Japanese photobooks
- Celebrity candid photography
- Friend-shot culture
- iPhone snapshots
- Xiaohongshu candid photography
- Disposable camera culture
- Daily social photography

---

# 1. Research Findings

### An ordinary event must exist before the photo

**Finding**
An ordinary event must exist before the photo

**Why it works**
Candid photographs feel captured when the subject was already doing a mundane task before the camera appeared. Without a task, the body defaults to posing.

**Prompt Translation**
```text
She was already [ordinary task] when the photo was taken.
```

**Expected Production Impact**
Reduces static model-like standing and gives every image a reason to exist.

**Confidence**
0.93

### A small interruption creates the captured moment

**Finding**
A small interruption creates the captured moment

**Why it works**
A real moment changes because something happens: a friend calls, phone vibrates, queue number is called, train beeps, wind moves hair. This makes the reaction feel caused rather than performed.

**Prompt Translation**
```text
The moment is interrupted because [small social / phone / environmental trigger] happens.
```

**Expected Production Impact**
Replaces staged look-backs with cause-driven reactions.

**Confidence**
0.91

### The reaction should be unfinished

**Finding**
The reaction should be unfinished

**Why it works**
Completed smiles, completed turns, and completed poses feel directed. Transitional reactions feel photographed before the subject had time to perform.

**Prompt Translation**
```text
Her reaction is unfinished: [smile just begins / head starts turning / hand freezes halfway / phone lowers slightly].
```

**Expected Production Impact**
Cuts portrait-session feeling and increases interrupted-life feeling.

**Confidence**
0.92

### Face and body should be out of sync

**Finding**
Face and body should be out of sync

**Why it works**
Real reactions cascade: eyes notice first, head follows, shoulders and hands remain in the original task. If the whole body aligns with the camera at once, it feels posed.

**Prompt Translation**
```text
Her eyes notice first, her head starts to turn, but her shoulders and hands are still committed to the original action.
```

**Expected Production Impact**
Prevents squared-shoulder camera-facing model poses.

**Confidence**
0.90

### Task residue must remain visible

**Finding**
Task residue must remain visible

**Why it works**
Objects and limbs should still show what she was doing: phone open, receipt in fingers, umbrella half-folded, bag zipper open. Task residue proves the camera interrupted an ongoing activity.

**Prompt Translation**
```text
Keep task residue visible: [phone still open / receipt in fingers / umbrella half-folded / bag zipper open / cup not yet sipped].
```

**Expected Production Impact**
Makes props functional and reduces influencer/ad-like object placement.

**Confidence**
0.94

### Environmental residue strengthens realism

**Finding**
Environmental residue strengthens realism

**Why it works**
A real interruption also leaves spatial traces: chair shifted, bag open, receipt on table, drink ring, door gap. This makes the event exist in the world, not only in her pose.

**Prompt Translation**
```text
Keep environmental residue visible: [chair shifted / bag open / receipt on table / umbrella dripping / door gap / lift button still lit].
```

**Expected Production Impact**
Improves lived-in continuity and reduces staged-clean scene feeling.

**Confidence**
0.86

### Camera eye contact is allowed only with a cause

**Finding**
Camera eye contact is allowed only with a cause

**Why it works**
Looking at the camera is not automatically posed. It becomes posed when there is no reason for the look and no task residue. With a friend calling or camera raised unexpectedly, brief eye contact can feel real.

**Prompt Translation**
```text
She briefly glances toward the camera because [interruption], while [task residue] remains visible.
```

**Expected Production Impact**
Preserves useful friend-shot recognition while avoiding portrait stare.

**Confidence**
0.88

### Ambient causes can replace direct camera direction

**Finding**
Ambient causes can replace direct camera direction

**Why it works**
Not every reaction should be caused by a photographer. MTR beeps, elevator chimes, rain, wind, scooter noise, or phone vibration create reactions without making the camera feel like a director.

**Prompt Translation**
```text
The interruption comes from [ambient sound/environmental change], not from posing for the camera.
```

**Expected Production Impact**
Adds candid variety and reduces repeated “friend called her name” formula.

**Confidence**
0.84

### Wall-leaning needs a task

**Finding**
Wall-leaning needs a task

**Why it works**
Wall-leaning is an influencer cliché unless she is waiting, checking a message, listening, searching for something, or reacting to someone.

**Prompt Translation**
```text
She is leaning near the wall because [waiting/checking/searching/listening], not posing; her hands still show [task].
```

**Expected Production Impact**
Prevents generic street-style influencer outputs.

**Confidence**
0.89

### The prompt must start with place/activity before attractiveness

**Finding**
The prompt must start with place/activity before attractiveness

**Why it works**
If the prompt begins with beauty, body, outfit, or pose, the model treats the scene as a photoshoot. Starting with place and task anchors the output in life logic.

**Prompt Translation**
```text
[place + atmosphere]. She was [event/task] when [interruption]. Her reaction is [unfinished reaction].
```

**Expected Production Impact**
Keeps production prompts aligned with captured daily-life imagery.

**Confidence**
0.90


---

# 2. Event Pattern Library

Minimum requested: 50 examples. Delivered: 60 examples.

These describe what was happening before the camera caught her.

1. putting phone away after replying
2. choosing a drink from a convenience-store fridge
3. looking for keys at the apartment door
4. fixing hair after wind
5. checking a queue number
6. opening a bag to find wallet
7. searching for Octopus card
8. folding a wet umbrella
9. checking if a taxi arrived
10. wiping rain from phone screen
11. waiting for a friend outside a café
12. comparing receipt with takeaway order
13. holding a table while friend sits down
14. looking for an empty MTR seat
15. gripping a train strap during movement
16. checking next station map
17. peeking at minibus route sign
18. pulling bag strap back onto shoulder
19. putting earbuds back into case
20. taking hair tie off wrist
21. lifting cup but pausing before drinking
22. opening snack packet
23. checking compact mirror quickly
24. putting phone back into tote
25. reading a menu while half-listening
26. trying to hear what friend said
27. holding door open behind her
28. stepping over a puddle
29. waiting at pedestrian crossing
30. checking traffic before crossing
31. looking for table number
32. brushing dust from shorts
33. adjusting one earring
34. checking lip balm in bad light
35. holding receipt while checking order
36. looking for charger cable
37. pulling tote higher on shoulder
38. removing mask and putting it away
39. checking humidity-frizzed hair
40. standing up from bench mid-conversation
41. leaning down to pick up dropped item
42. half-opening fridge door then pausing
43. checking notification while walking
44. turning away from bright sign
45. waiting for elevator doors
46. pressing lift button while still talking
47. holding takeaway bag and checking label
48. moving drink away from table edge
49. picking tissue from packet
50. folding shopping receipt
51. opening apartment mailbox
52. checking coins/cards at counter
53. adjusting cardigan sleeve
54. putting sunglasses into bag
55. looking through purse for lipstick
56. checking door number
57. moving aside for passerby
58. drying hair while sitting on sofa
59. checking wet shoes after rain
60. reaching for phone charger under table

---

# 3. Interruption Pattern Library

Minimum requested: 30 examples. Delivered: 40 examples.

These describe what changed the moment.

1. hears her name from off-frame
2. phone vibrates in her hand
3. friend arrives unexpectedly
4. elevator doors open
5. someone calls her
6. friend says wait one photo
7. door opens beside her
8. waiter calls queue number
9. taxi pulls up
10. MTR doors beep
11. umbrella bumps against bag
12. wind blows hair across face
13. rain starts again
14. drink almost tips over
15. bag strap slips
16. receipt falls
17. friend laughs off-frame
18. someone enters frame edge
19. traffic light changes
20. car headlights sweep across face
21. phone screen lights up
22. camera flash surprises her
23. shop clerk asks question
24. friend points nearby
25. someone asks to squeeze past
26. seat becomes available
27. dog passes close
28. scooter passes loudly
29. train jerks
30. escalator reaches top
31. food arrives
32. order placed on counter
33. friend says look here
34. camera is raised unexpectedly
35. another friend enters frame
36. bag zipper catches
37. hair sticks to cheek
38. street sign flickers
39. lift chime sounds
40. sudden gust of wind

---

# 4. Reaction Pattern Library

Minimum requested: 30 examples. Delivered: 40 examples.

These describe how she reacts before the reaction becomes a completed pose.

1. eyes brighten before full smile
2. smile begins but is incomplete
3. brief glance upward
4. half-turn over shoulder
5. mouth slightly open as if answering
6. eyebrows lift in recognition
7. small annoyed laugh
8. caught mid-blink but still natural
9. hand freezes halfway
10. shoulder rotates before hips
11. chin lifts toward sound
12. eyes move first then head follows
13. body continues walking while face turns back
14. fingers pause on phone screen
15. hand tightens around strap
16. one hand lifts toward hair
17. laugh starts but does not peak
18. expression between confusion and amusement
19. one-sided smile
20. brows pinch while checking
21. quick side-eye at friend
22. soft exhale after being called
23. face relaxes after recognizing friend
24. mouth closes around unfinished sentence
25. eyes squint from sudden light
26. hand covers part of face while laughing
27. neck turns but shoulders stay forward
28. weight shifts to one leg
29. phone lowers a few centimeters
30. bag hand pauses mid-zip
31. half-step stops before landing
32. looks down first then up
33. brief eye contact without performance
34. face turns while body remains in task
35. tiny grin before deciding whether to pose
36. subtle embarrassment after noticing camera
37. forehead relaxes from concentration
38. eyes narrow at bright screen
39. smile fades as attention returns
40. hand points slightly toward interruption

---

# 5. Failure Pattern Library

These patterns create posing feeling, influencer feeling, advertisement feeling, or AI feeling.

1. standing still with no task
2. leaning on wall only to look attractive
3. direct camera stare with no reason
4. hands in pockets symmetrically
5. perfect S-curve model pose
6. both shoulders squared to camera
7. chin down eyes up glamour expression
8. hair perfectly arranged despite wind/rain
9. clothes too smooth with no activity wrinkles
10. background arranged like set
11. object held as prop with no use
12. phone held but screen/task absent
13. waiting pose without what she waits for
14. walking pose with frozen legs
15. looking back without cause
16. full smile at camera like portrait
17. no off-frame cause
18. no interrupted action
19. hands visible but idle
20. perfectly balanced composition
21. studio lighting in everyday scene
22. glossy skin and symmetrical face
23. overly cinematic rain/neon
24. fashion editorial wall lean
25. advertisement-like product visibility
26. every background sign readable
27. over-clean room
28. empty staged street
29. body-display pose instead of activity
30. outfit described more than event
31. planned flattering camera angle only
32. subject centered with perfect eye contact
33. moving scene without motion blur
34. all limbs posed cleanly
35. no before/after transition
36. expression already at peak
37. scene has no social reason
38. friend-shot claimed without friend behavior
39. casual snapshot with professional lighting
40. AI-perfect floating hands
41. dramatic magazine vocabulary
42. luxury styling with ordinary-life claim
43. model pose in local routine scene
44. camera eye contact with no task residue
45. body angled for display rather than task
46. symmetrical object placement
47. no mistakes or interruption
48. hair/clothes unaffected by environment
49. background has no social trace
50. all surfaces spotless

---

# 6. Production Prompt Rules

## Copy-Paste Rule Block

```text
Make this feel like a real moment interrupted by a camera, not a posed photoshoot.

Event: she was [specific ordinary task].
Interruption: [small social / phone / environmental / movement trigger] happens.
Reaction: [partial cascading response], not a completed pose.
Task residue: [physical trace of the original task] remains visible.
Environment residue: [small spatial trace: chair shifted / bag open / receipt on table / umbrella dripping / drink ring / door gap].

Her eyes notice first, her head starts to turn, but her shoulders, hands, hips, or feet still belong to the original action. The image should feel like someone happened to take this photo before she had time to pose.

Avoid performance: no model pose, no perfect smile, no fully squared shoulders, no symmetrical stance, no hands-in-pockets posing, no fashion editorial feeling, no studio lighting, no influencer wall-leaning unless a real task or interruption explains it, no camera eye contact unless task residue and interruption cause are visible.
```

## Quick Fill-In Formula

```text
[place + atmosphere]. She was [event/task] when [interruption]. Her reaction is [unfinished reaction]. Her body still shows [task residue]. The space still shows [environment residue]. The photo feels accidentally captured by a friend, slightly off-center, with ordinary-life timing and no completed pose.
```

## Positive Prompt Example

```text
A casual iPhone snapshot inside a convenience store. She was choosing a drink from the fridge when her friend called her name from behind. Her right hand is still on the fridge handle, the glass remains between her hand and the drinks, and the fridge shelves stay softly behind the reflection. Her eyes notice first and her smile is only beginning. Her shoulders are still angled toward the fridge, not fully turned to pose. The moment feels interrupted, not staged.
```

## Negative Prompt Example

```text
She stands beautifully in a convenience store, looking at the camera with a soft smile, elegant pose, perfect composition, detailed product shelves.
```

Why it fails: no event, no interruption, no unfinished reaction, and product shelves become advertisement-like.

---

# GPT Review Request

GPT should review the findings, extract production rules, decide merge/reject, and create prompt implementation. Canon status remains blocked until production evidence exists.

## Success Metric

Reduce “posed feeling” in the next 20 production images by at least 50%.

## Canon Status

Blocked. Research does not enter canon. Production evidence required.
