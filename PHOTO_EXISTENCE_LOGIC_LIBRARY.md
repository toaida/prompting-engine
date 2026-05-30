# PHOTO EXISTENCE LOGIC LIBRARY
### V17 — Why This Photo Exists
### Status: ACTIVE — Runtime System

---

## PHILOSOPHY

**Core Rule:** Every generated image MUST have a believable reason to exist.

AI-generated images fail the "would this photo be taken?" test. The subject stares beautifully into nothing. The moment has no purpose. The viewer senses it immediately — the image has no existential justification.

**The Fix:** Anchor every image to a real human behavior that generates the photo naturally.

---

## EXISTENCE LOGIC TEMPLATE

Every prompt layer 2-4 should include ONE existence reason:

```
BECAUSE [human behavior] → [photo type] → [believable context]
```

---

## EXISTENCE REASONS BY SPACE

### 🏨 HOTEL ROOM

| Reason | Trigger | Visible Evidence |
|--------|---------|------------------|
| Outfit check before leaving | Standing at mirror, phone tilted | Phone in hand, mirror reflection, one shoe on |
| Just woke up, phone check | In bed, morning light, blanket up | Phone on chest, squinting, unmade bed |
| Waiting for friend | Sitting on bed edge, bored pose | Key card on table, door closed, one bag packed |
| Post-shower, towel dry | Bathroom, steam, mirror fog | Wet hair dark, towel on shoulder, robe |
| Late night room service | On bed, tray on lap, TV on | Half-eaten food, remote, late-night lighting |
| Just arrived, still wearing travel clothes | Standing by window, backpack on | Carry-on visible, passport on desk, shoes still on |
| Testing new swimsuit fit | In room, different angles | Full-length mirror, multiple bags visible |

### 🌊 BEACH / POOL

| Reason | Trigger | Visible Evidence |
|--------|---------|------------------|
| Checking fit of new swimsuit | Turning to see back | Phone held, checking reflection |
| Resting after swimming | Towel recline, tired expression | Wet hair flattened, body still wet |
| Applying sunscreen to back | Arms behind, reaching | Bottle visible, mirror or friend behind |
| Just out of water, cold | Shivering, skin goosebumps | Wet skin, towel being held |
| Waiting for friends to arrive | Alone on beach, looking at phone | Chair reserved, bags, looking toward path |
| Killing time, scrolling phone | Sitting on towel, casual | Phone in hand, bag nearby, half-drunk water |
| Putting on cover-up | Just stood up from towel | One leg dressed, one not, sand on feet |

### 🚇 MTR / PUBLIC TRANSIT

| Reason | Trigger | Visible Evidence |
|--------|---------|------------------|
| Waiting for MTR | Standing on platform, bored | Octopus card in hand, looking at arrival board |
| Killing time between transfers | Sitting in corridor | Shopping bag, waiting expression |
| Just got off MTR, checking phone | Standing in car, doors open | Phone in hand, one bag, about to exit |
| Late night MTR alone | Sitting, tired | Headphones, minimal bags, empty car |
| MTR too crowded, standing | Standing with pole, annoyed | Pole grip, near door, peak hour |
| Taking MTR to meet friends | Looking at phone | Dressed up, bag, pre-event |
| MTR exit, checking directions | Looking up at signs | Map on phone, confused expression |

### 🏠 APARTMENT / HOME

| Reason | Trigger | Visible Evidence |
|--------|---------|------------------|
| Post-shower, getting ready | Bathroom mirror, steam | Towel on head, skincare visible |
| Testing new outfit | Standing in bedroom mirror | Full-length mirror, multiple outfit choices on bed |
| Morning coffee routine | Kitchen, lazy morning | Mug in hand, pajamas, morning light |
| Bored on couch | Lying on couch, phone above | Lazy posture, TV on in background |
| Late night snack | Kitchen counter, fridge open | Fridge light, snack in hand |
| Sunday morning in bed | Just woke up, blanket | Morning light, unmade bed, no makeup |
| Sending photo to boyfriend | In bedroom, preparing to send | Phone in hand, mirror angle, expression of anticipation |
| Just bought new clothes, trying on | In room, bags still visible | Shopping bags, scattered clothes |

### ☕ CAFÉ / RESTAURANT

| Reason | Trigger | Visible Evidence |
|--------|---------|------------------|
| Waiting for food | Phone on table, looking up | Place setting, waiting expression |
| Killing time between appointments | Solo table, coffee | Book or phone, no food yet |
| Friend photo for social media | Friend taking photo | Looking at friend, not camera, café background |
| Testing makeup before date | Bathroom mirror | Makeup spread, phone propped |
| Just ordered, food arriving | Excited expression | Server approaching, anticipation |

### 🌃 STREET / OUTDOOR

| Reason | Trigger | Visible Evidence |
|--------|---------|------------------|
| Waiting for Uber | Standing on street, checking phone | Car app open, looking at road |
| Taking photo of outfit of the day | Street mirror or reflective surface | Phone angled, checking reflection |
| Resting after shopping | Bench, shopping bags | Multiple bags, sitting tired |
| Meeting friends at landmark | Standing, looking for them | Scanning crowd, waiting expression |
| Just got haircut | In front of salon mirror | Different hair, checking angles |
| Trying on sunglasses | At display | Glasses on face, phone for comparison |

### 🏨 HOT SPRING / ONSEN

| Reason | Trigger | Visible Evidence |
|--------|---------|------------------|
| Cooling off after bath | At outdoor onsen edge | Steam, towel on head, flushed skin |
| Post-bath robe moment | Walking to room | Yukata, wooden sandals, relaxed |
| Testing new hairstyle post-bath | Mirror in changing area | Wet hair, natural expression |

---

## INTEGRATION RULES

### Rule 1: Existence Reason MUST Be in Layers 2-4

```
GOOD: "Post-swim rest on beach towel — friend just went to buy drinks, alone on beach, killing time"
BAD: "Model on beach in swimsuit"
```

### Rule 2: Evidence Must Be Visible

The existence reason should produce visual evidence:
- Phone in hand = photo being taken/sent
- One shoe on = just woke up or about to leave
- Half-drunk water = been here a while
- Key card on table = just arrived or about to check out

### Rule 3: Expression Matches Reason

| Reason | Expression |
|--------|------------|
| Waiting for someone | Scanning, checking phone |
| Just arrived | Alert, looking around |
| Resting | Relaxed, eyes half-closed |
| Preparing to send | Anticipating, slight smile |
| Bored | Distant gaze, neutral |

### Rule 4: Combine With Camera Awareness

- **Existence + Level 1:** Friend asked for photo → subject knows, still natural
- **Existence + Level 2:** Checking outfit → friend is there, they see it too
- **Existence + Level 3:** Sending to boyfriend → subject in moment, phone dominant
- **Existence + Level 4:** Documentary of journey → subject unaware, behavior natural

### Rule 5: Avoid Staged Reasons

```
AVOID: "Posing for photo"
GOOD: "Checking how her hair looks after the wind"
GOOD: "Waiting for Uber, checking app"
GOOD: "Looking up from phone because she heard her name"
```

---

## COMPOUND EXISTENCE EXAMPLES

### Beach Sending Photo
```
BECAUSE: Testing new swimsuit fit, sending photo to boyfriend
→ Front camera angle, phone visible
→ Slightly self-conscious but excited expression
→ Beach towel in frame as context
→ FRIEND-SHOT (friend took photo)
```

### MTR Late Night
```
BECAUSE: Late night MTR home after drinks, tired
→ Empty car, headphones in, eyes closed
→ One shopping bag on lap
→ Looking exhausted but peaceful
→ FORGOTTEN-CAMERA (accidental capture by surveillance or friend)
```

### Hotel Mirror Check
```
BECAUSE: Checking outfit before going out with friends
→ Standing at hotel mirror, one shoe on
→ Phone in hand (taking reference photo)
→ Key card visible on table
→ Full-length mirror capturing dress
→ CAMERA-SELFIESQUE (phone is the camera)
```

### Post-Shower Apartment
```
BECAUSE: Just showered after beach, phone check in bedroom
→ Hair wet and dark, towel on shoulders
→ Still wearing cover-up or robe
→ Morning light from window
→ Skincare routine visible on desk
→ LEVEL 3 (not performing, just existing)
```

---

## ANTI-AI COMPOUND

Combine with memory systems for maximum believability:

```
EXIST-01 (Photo Existence) + MEM-03 (Emotional Timing)
→ Photo exists because of human behavior, moment captured mid-behavior

EXIST-02 (Existence Evidence) + FAB-01 (Fabric Physics)  
→ Physical evidence visible, fabric shows real wear

EXIST-03 (Existence + Expression) + COL-02 (Fuji Pro 400H)
→ Natural moment with dreamy film rendering
```

---

## QUICK REFERENCE CARD

**When generating:** Ask — "Would someone actually take this photo? Why?"

**If no reason:** Add one from this library.

**If reason is weak:** Strengthen with visible evidence.

**Expression must match:** Waiting ≠ excited, tired ≠ alert.

---

*End of PHOTO_EXISTENCE_LOGIC_LIBRARY.md*
