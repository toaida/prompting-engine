---
name: ENGINE_V15_PHOTODUMP_RHYTHM_SYSTEM
description: Photodump Rhythm System for authentic social media documentation
areas: AREA 07
version: V15
status: READY FOR INTEGRATION
---

# ENGINE_V15_PHOTODUMP_RHYTHM_SYSTEM

## Core Philosophy

**Photodump** = posting multiple low-stakes photos in sequence, treating the camera as a documentation device rather than a performance tool. The subject doesn't know they're being photographed. The photographer isn't directing. The result feels like "found footage" of a real moment.

Key distinction from posed content: **no aesthetic optimization**. The point is not to look good — it's to document that you were there.

---

## PHOTODUMP_RHYTHM_LIBRARY

### Rhythm Types

| Type | Description | Visual Markers | Prompt Token |
|------|-------------|----------------|--------------|
| RAPID_FIRE | 3-5 shots within seconds | Identical lighting, similar pose, slight blur | [RAPID_FIRE] |
| BURST_MODE | 8-15 shots over 1-2 minutes | Mixed expressions, outfit changes, movement | [BURST_MODE] |
| SPREAD_DOC | 1 shot per hour over day | Different locations, consistent subject | [SPREAD_DOC] |
| ACCIDENTAL | 1-2 shots total, unplanned | Awkward angle, blur, background dominate | [ACCIDENTAL_SHOT] |
| EVIDENCE | Documenting specific object/moment | Subject secondary or absent | [EVIDENCE_SHOT] |

### Modulation Profiles

```
PROFILE_A: LOW_EFFORT_AUTHENTIC
- Shooting frequency: Random, spontaneous
- Framing: Auto-composition (device defaults)
- Subject awareness: Unaware or forgetful
- Failure tolerance: HIGH (failures are authentic)
- Token: [LOW_EFFORT_AUTHENTIC]

PROFILE_B: DOCUMENTARY_CAPTURE
- Shooting frequency: Consistent, pattern-based
- Framing: Environmental context prioritized
- Subject awareness: Forgotten camera
- Failure tolerance: MEDIUM (some intentional blur)
- Token: [DOCUMENTARY_CAPTURE]

PROFILE_C: FRIEND_COLLECTION
- Shooting frequency: Medium, conversational
- Framing: 2+ subjects, group dynamics
- Subject awareness: Semi-aware (cooperating friend)
- Failure tolerance: HIGH (imperfect chemistry)
- Token: [FRIEND_COLLECTION]

PROFILE_D: TRAVEL_LOG
- Shooting frequency: High volume, location-driven
- Framing: Landmark + subject (landmark primary)
- Subject awareness: Photo-taking is part of experience
- Failure tolerance: LOW (travel photos are curated)
- Token: [TRAVEL_LOG]
```

---

## Prompt Grammar

```
[rhythm_type]_photodump_
[modulation_profile]_
[documenting_moment]:_[what_is_documented]_
[subject_state]:_[awareness_level]_
[device_type]:_[capture_mode]
```

**Examples:**
```
[BURST_MODE]_photodump_[LOW_EFFORT_AUTHENTIC]
documenting_moment:beach_afternoon_sunset
subject_state:swimming_in_fully_aware_could_be_photographed
device_type:iphone_14_pro_auto_mode

[EVIDENCE_SHOT]_photodump_[DOCUMENTARY_CAPTURE]
documenting_moment:late_night_market_street_food
subject_state:ordering_from_stall_half_turned_away
device_type:android_auto_night_mode
```

---

## HK-Specific Content

- **MTR Journey Photodump**: Transit documentation, platform arrivals, crowd moments
- **Tea Restaurant Photodump**: Ordering process, food arrival, incomplete dishes
- **Night Market Photodump**: Street food discovery, walking documentation
- **Ferry Crossing Photodump**: Harbour moments, outdoor deck sequences

**HK Tokens:** [MTR_DOC] [TEA_RESTAURANT_DOC] [NIGHT_MARKET_DOC] [FERRY_DOC]

---

## Moderation Profile

**PRESERVES:**
- Casual settings (no professional staging)
- Natural subject expressions (unaware)
- Environmental authenticity (documentary context)

**REMOVES:**
- Aesthetic optimization signals
- Professional lighting setups
- Directed poses or expressions

**WARNINGS:**
- Avoid evidence shots that capture strangers without awareness
- Travel log profile should not approach professional photography aesthetics

---

## Cross-References

- Complements BAD_PHOTO_REALISM (accidental failures are photodump-native)
- Complements ENVIRONMENTAL_AIR (environmental context is photodump priority)
- HK-specific profiles integrate with SOCIAL_CAMERA operators (OP_13-OP_22)

---

*Module: ENGINE_V15_PHOTODUMP_RHYTHM_SYSTEM.md*
*Source: AREA 07 — V15 Research*
*Status: READY FOR INTEGRATION*
