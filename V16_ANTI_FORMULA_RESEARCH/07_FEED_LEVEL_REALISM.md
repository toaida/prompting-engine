# AREA 07: FEED-LEVEL REALISM SYSTEM

## The Problem

Current engine: Images are individually optimized — each photo looks great. But as a feed? Problems emerge:
- Too consistent aesthetic
- No "bad" photos
- No filler
- No transitional moments
- No repetition patterns of real life

Real KOL IG feeds: **lived-in, continuous, socially real.** They include ugly-cute shots, filler, repetition, random snapshots. The feed tells a story of one girl living multiple days.

---

## FEED_REALISM_LIBRARY

### Category A: Filler/Low-Effort Content (EXPANDED)

**Why real:** Not every photo is a production. Some are just "I'm here."

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| A1: QUICK_SELFIE | 2 seconds in bathroom mirror | Low quality, spontaneous | [QUICK_SELFIE] |
| A2: FOOD_DOCUMENT | Food photo, subject secondary | "Look what I ate" | [FOOD_DOCUMENT] |
| A3: RANDOM_SNAPSHOT | Nothing special, moment captured | "I was here" energy | [RANDOM_SNAPSHOT] |
| A4: BACKGROUND_CAPTURE | Subject accidentally in shot | Forgot to check frame | [ACCIDENTAL_BACKGROUND] |
| A5: CLOSEUP_DETAIL | Just a hand, object, feet | Partial, intimate | [BODY_PART_CLOSEUP] |
| A6: SCREENSHOT_REPOST | Reposted story, screen captured | Meta, digital | [SCREENSHOT_REPOST] |
| A7: OCTOPUS_RECEIPT | Octopus reload receipt | Daily life, transit | [OCTOPUS_RECEIPT] |
| A8: GARBAGE_BAG_TAG | Trash bag charge receipt visible | 垃圾徵費 daily | [GARBAGE_TAG] |
| A9: TAKEAWAY_LUNCH | Delivery packaging, open box | 外賣 culture | [TAKEAWAY_LUNCH] |
| A10: QUEUE_TICKET | Number ticket from queue | MTR/minivan wait | [QUEUE_TICKET] |

### Category B: Repetition/Life Continuity

**Why real:** Real girls repeat things — outfits, locations, people. This is identity.

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| B1: SAME_LOCATION_AGAIN | Back to same cafe/park/place | "This is my spot" | [SAME_PLACE_AGAIN] |
| B2: SAME_OUTFIT_REPEAT | Wearing yesterday's clothes | "Did laundry yet?" | [SAME_OUTFIT_REPEAT] |
| B3: SAME_FRIEND_GROUP | Same people appearing | Social continuity | [SAME_FRIEND_AGAIN] |
| B4: CONTINUING_STORY | Sequel to previous post | Narrative continuity | [CONTINUING_STORY] |
| B5: RETURNING_AFTER_BREAK | Back after hiatus | "I'm still here" | [RETURNING_AFTER_BREAK] |

### Category C: "Ugly-Cute" Moments

**Why real:** Perfect beauty is suspicious. Cute-but-not-perfect humanizes.

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| C1: BUNNY_SNORING | Cute sleeping face, mouth open | Vulnerability, honesty | [SLEEPING_BUNNY_SNORE] |
| C2: BAD_ANGLE_HANDSOME | Technically bad photo but cute subject | "Still pretty right?" | [BAD_ANGLE_STILL_CUTE] |
| C3: UNCOMBED_HAIR | Just woke up, hair everywhere | Morning honesty | [MESSY_MORNING_HAIR] |
| C4: FOOD_ON_FACE | Eating messily, food on cheek | Playful, unperformed | [FOOD_ON_CHEEK] |
| C5: EYES_CLOSED_SQUINT | Squinting in bright light, laughing | Unflattering but real | [SQUINT_LAUGH] |
| C6: WEIRD_FACIAL_EXPRESSION | Random silly face | Playful, not performing | [SILLY_FACE] |
| C7: DOUBLE_CHIN_MOMENT | Head angle creates double chin | Honest moment | [DOUBLE_CHIN_HONEST] |

### Category D: Transitional Moments

**Why real:** Life is transitions. Between places, moods, activities.

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| D1: GETTING_READY | In bathroom, getting prepared | Pre-event ritual | [GETTING_READY] |
| D2: TAXI_RIDE_TRANSIT | In car, arriving somewhere | In-between moment | [TAXI_TRANSIT] |
| D3: WAITING_FOR_SOMEONE | Standing/waiting, looking around | Anticipation | [WAITING_SOMEONE] |
| D4: POST_EVENT_COME_DOWN | After party, still in clothes | Comedown energy | [POST_EVENT_DOWN] |
| D5: MID_CONVERSATION | Talking to someone, not posing | Social moment | [MID_CONVERSATION] |
| D6: CHECKING_PHONE | Pulled out phone, checking | Distracted, normal | [CHECKING_PHONE] |
| D7: ENTERING_FRAME | Walking into photo, not set up | Environmental entry | [ENTERING_FRAME] |

### Category E: Social Proof/Group Dynamics

**Why real:** Real life includes other people. Social context = authenticity.

| Type | Description | Realism Signal | Token |
|------|-------------|----------------|-------|
| E1: GROUP_PHOTO_CROP | Someone cropped out, face visible | Someone else's photo | [GROUP_PHOTO_CROPPED] |
| E2: IN_BACKGROUND_OTHERS | Other people in frame | Social context | [OTHERS_IN_BACKGROUND] |
| E3: CELEBRATION_MOMENT | Birthday, achievement, milestone | Social event | [CELEBRATION_MOMENT] |
| E4: FRIEND_SOLO_WITH | Solo but friend took it | "My friend took this" | [FRIEND_TOOK_PHOTO] |
| E5: OVERHEARD_STORY | Photo of someone else, story about them | Social awareness | [STORY_ABOUT_OTHER] |

---

## Photodump Pacing System (EXPANDED)

### Principle

Photodump = multiple related photos that feel like documentation, not production.

### Photodump Sub-Types

```
PHOTODUMP_SESSION now has structured sub-types:

[PHOTODUMP_SAME_OUTFIT] — 3-4 shots, same clothes, different activities/angles
[PHOTODUMP_LOCATION] — 3-4 shots, same location, different times/angles
[PHOTODUMP_MOMENT] — sequential moments, like mini-story (before/after)
[PHOTODUMP_MIXED] — random selection, like phone dump

Rules within session:
- At least 1 distance change (close → medium → wide OR vice versa)
- At least 1 "lower quality" shot (grainy, slightly blurry, awkward)
- Max 1 "hero" quality shot per session
```

### Pacing Rules

```
PHOTODUMP_COMPOSITION:

1. MIX_QUALITY: 2-3 "good" photos + 1-2 "filler" photos
2. VARIED_DISTANCE: One close, one medium, one wide
3. MIXED_EXPRESSIONS: 1 candid, 1 smiling, 1 distracted
4. REPEATED_LOCATION: All at same place, different angles
5. CONTINUITY_SHOT: Sequential moment captured
```

### Feed Architecture

```
FEED_ARCHITECTURE:

WEEK_ARCHITECTURE:
- 1 "hero" post: Production quality, high effort
- 2-3 "story" posts: Narrative, ongoing
- 1-2 "filler" posts: Low effort, real life
- 1 "ugly-cute" post: Vulnerable, honest

PATTERN_NOT_TO_FOLLOW:
- ❌ Perfect quality every single photo
- ❌ Same expression every photo
- ❌ Same distance every photo
- ❌ No transitional moments
- ❌ No filler/low-quality shots
```

---

## Continuity-Feed Architecture

### Principle

Feed should tell a story. Each photo relates to others. Continuity creates life narrative.

### Continuity Types

```
CONTINUITY_LIBRARY:

CON_01: OUTFIT_CONTINUITY
- Same outfit, different angles/activities
- Token: [OUTFIT_CONTINUITY]

CON_02: LOCATION_CONTINUITY
- Same location across days/weeks
- Token: [LOCATION_CONTINUITY]

CON_03: MOOD_CONTINUITY
- Same emotional state continuing
- Token: [MOOD_CONTINUITY]

CON_04: NARRATIVE_CONTINUITY
- Sequel to previous post's story
- Token: [NARRATIVE_CONTINUITY]

CON_05: PERSON_CONTINUITY
- Same friend/people appearing
- Token: [PERSON_CONTINUITY]

CON_06: TIME_CONTINUITY
- Before/after, morning/night, then/now
- Token: [TIME_CONTINUITY]
```

### Feed Example

```
IMAGE_01: [POST_WORKOUT] + [OUTFIT_CONTINUITY: same gym outfit from yesterday]
IMAGE_02: [SAME_PLACE_AGAIN] + [LOCATION_CONTINUITY: same gym]
IMAGE_03: [QUICK_SELFIE] + [FOOD_DOCUMENT] + [RANDOM_SNAPSHOT] = [PHOTODUMP_SESSION]
IMAGE_04: [RETURNING_AFTER_BREAK] + [SAME_FRIEND_AGAIN]
```

---

## Social-Upload Rhythm Grammar

### When Real Girls Post

```
UPLOAD_RHYTHM:

RHYTHM_A: MORNING_DOC (Morning person)
- Morning photo, wake-up face
- Coffee, morning light
- Token: [MORNING_POST]

RHYTHM_B: AFTERNOON_CANDID (Spontaneous afternoon)
- Random afternoon moment
- Nothing special happening
- Token: [AFTERNOON_RANDOM]

RHYTHM_C: EVENING_GLAM (Going out prep)
- Getting ready, outfit reveal
- Evening/event context
- Token: [EVENING_GLAM]

RHYTHM_D: LATE_NIGHT_REFLECTION (Night owl)
- Late night, reflective
- 11pm+ posts
- Token: [LATE_NIGHT_REFLECT]

RHYTHM_E: WEEKEND_VARIATION (Weekend vs weekday)
- Weekend: more casual, spontaneous
- Weekday: more curated
- Token: [WEEKEND_CASUAL]
```

---

## HK-Specific Feed Patterns

| Pattern | Description | Token |
|---------|-------------|-------|
| Tea restaurant repeat | Same tea restaurant, different dishes | [TEA_REST_FEED] |
| MTR same station | Same MTR station, different days | [MTR_STATION_FEED] |
| Friend group rotation | Same friends, different activities | [HK_FRIEND_FEED] |
| Night market documentation | Night market visit, food focus | [NIGHT_MARKET_FEED] |
| Beach day series | Beach trip, photodump style | [BEACH_DAY_FEED] |
| Staycation repetition | Same hotel, different occasions | [STAYCATION_FEED] |

---

## Feed-Level Anti-Repetition Rules

1. **Every 5 images: at least one "ugly-cute" or "filler" type**
2. **Every 7 images: at least one photodump session (3+ related shots)**
3. **Every 10 images: at least one transitional moment**
4. **Quality variation is key**: Mix high-quality + medium + low-quality shots. Not every photo should be hero quality.
5. **"Accidental bad" ≠ "consistently bad"**: 1-2 genuinely awkward/blurry shots per 10 images = authenticity. Every photo looking low-quality = low-skill generation.
6. **Anti-formula rule**: If the last 5 images all have similar silhouette (tight top + tight bottom), the next image MUST have loose/baggy silhouette.

---

*Research: AREA 07 — Feed-Level Realism System*
*Status: IN PROGRESS — Ready for DeepSeek verification + extension*