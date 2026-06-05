# ENGINE_V20_OBJECT_MOTIVATION_SYSTEM

**Engine ID:** V20-ENG-013
**Engine name:** Object Motivation Engine (R013)
**Canon status:** BLOCKED — awaiting production testing per VERIFICATION_R013
**Version:** 0.1.0
**Last updated:** 2026-06-05
**Owner:** V20 production track
**Research file:** `research/V20_RESEARCH/R013_OBJECT_MOTIVATION_ENGINE.md`
**Verification file:** `verification/V20_RESEARCH/VERIFICATION_R013_OBJECT_MOTIVATION.md`
**Companion engines:** R012 (Conversation Illusion), R014 (Viewer Gaze)

---

## 1. Mission

Give every visible object in a V20 frame a **motivation record**: a deterministic plan for why the object is there, who it belongs to, what it was used for, and why the camera is seeing it. The engine exists to convert *set-dressed* environments (objects placed for the camera) into *lived-in* environments (objects placed for the user).

The engine does NOT decide:
- Who the persona is (R015 / Persona Visual Anchor)
- What the persona is wearing (R016 / Outfit Card)
- Where the persona is (R017 / Environment Engine)
- What the persona is doing (R011 / Scene Composition)
- What expression she has (R012 / Conversation Illusion)
- Where the viewer's eye goes (R014 / Viewer Gaze)

The engine DOES decide, given the above inputs:
- What objects are visible in the frame.
- The five mandated attributes for each visible object.
- The active cluster, the baseline, and the in-progress residue.
- The use-signature, the visibility reason, and the entropy level.

---

## 2. Inputs

| Input | Type | Source | Required? |
|---|---|---|---|
| `persona_id` | string | R015 | required |
| `persona_object_signature` | object (dominant_hand, sleep_side, morning_routine, evening_routine, known_objects) | R015 | required |
| `scene_id` | string | R011 | required |
| `scene_location_type` | enum { kitchen, bathroom, bedroom, hotel_room, fitting_room, study, balcony, cafe, street, transport, generic } | R011 | required |
| `scene_time_of_day` | enum { early_morning, morning, midday, afternoon, evening, late_night, ambiguous } | R011 | required |
| `scene_event_proximity_hours` | float (hours since last event, default = 24+) | R011 | required |
| `lighting_brief` | object (key_direction, intensity, source_type) | R017 | required |
| `camera_angle` | enum { eye_level, high_angle, low_angle, dutch, side } | R017 | required |
| `subject_action` | string (e.g., "drinking coffee", "reading", "putting on shoes") | R011 | required |
| `subject_position` | object (x, y, z in scene coordinates) | R011 | required |
| `platform_target` | enum { instagram, xiaohongshu, twitter, douyin, generic } | R018 | required |

---

## 3. Output contract — the object list

The engine emits a JSON object describing every visible object in the frame, with the five mandated attributes.

```json
{
  "objects": [
    {
      "id": "obj_001",
      "type": "coffee_cup",
      "attributes": {
        "owner": "her",
        "purpose": "drinking morning coffee",
        "last_interaction": {
          "timestamp_relative": "5 minutes ago",
          "actor": "her",
          "action": "took a sip, set the cup down"
        },
        "current_state": {
          "position": "on the nightstand",
          "orientation": "handle to her right (right-handed)",
          "physical_state": "warm, half-full, condensation ring on the nightstand",
          "state_indicators": ["waterline visible", "warmth implied", "handle position"]
        },
        "visibility_reason": "in the foreground depth, near her hand, in the camera's eye-line"
      },
      "use_signature": "warm half-full morning coffee, handle to dominant hand, condensation ring",
      "entropy_level": "low (active cluster)",
      "contradictions": []
    }
  ],
  "active_cluster": {
    "object_ids": ["obj_001", "obj_002", "obj_003"],
    "cluster_type": "wake_up_morning",
    "in_progress_activity": "drinking coffee, looking at phone"
  },
  "baseline_objects": ["obj_004", "obj_005"],
  "in_progress_residue": [
    {"id": "obj_006", "type": "phone", "state": "face-up, screen lit, recent text visible"}
  ],
  "second_person_traces": [
    {"id": "obj_007", "type": "second_coffee_cup", "state": "across the table, half-drunk, partner's cup"}
  ],
  "closed_storage": [
    {"id": "obj_008", "type": "cabinet", "state": "closed"},
    {"id": "obj_009", "type": "drawer", "state": "closed"}
  ],
  "open_storage": [
    {"id": "obj_010", "type": "drawer", "state": "open", "justification": "she is looking for her keys"}
  ],
  "time_of_day_coherence": {
    "lighting": "morning window light",
    "objects": "morning-consistent",
    "residue": "morning-consistent",
    "coherent": true
  },
  "realism_score": {
    "object_audit_completeness": 0.0..1.0,
    "active_cluster_clarity": 0.0..1.0,
    "use_signature_strength": 0.0..1.0,
    "time_coherence": 0.0..1.0,
    "any_FP_match": true | false,
    "overall": 0.0..1.0
  }
}
```

Each object must have all five attributes. Objects with any missing attribute are removed from the visible-object list and become "background" (not subject to the mandate).

---

## 4. State

The engine maintains a per-character, per-location state:

- `persona_object_signature`: the character's consistent object signature (dominant hand, sleep side, etc.).
- `known_objects_in_location`: a list of objects the character owns in this location, with their typical positions and states.
- `last_interaction_timeline`: a per-object log of recent interactions in this session.
- `active_cluster_history`: which cluster was active in recent frames, to prevent repetition.

The state persists across frames within a session. The state is reset when a new location or a new arc starts.

---

## 5. Core rules (from research file §13)

The engine enforces the 15 R013 rules plus the 5 mandated attributes. Each rule is a *hard* constraint.

| Rule ID | Rule | Pass criteria |
|---|---|---|
| R013-01 | Object list audit | Every visible object has all 5 attributes |
| R013-02 | Last-interaction timestamp | Timestamp plausible for lighting and state |
| R013-03 | Default closed | Storage closed unless an in-progress activity is specified |
| R013-04 | Active cluster mandate | Exactly one active cluster; rest at baseline |
| R013-05 | Use-signature props | Every prop has a use-signature |
| R013-06 | Owner signature | All objects share consistent owner habits |
| R013-07 | Path of motion | Objects in motion are mid-motion; at-rest at rest |
| R013-08 | Visibility justification | Every visible object has a visibility reason |
| R013-09 | Time-of-day coherence | All objects consistent with the lighting's time-of-day |
| R013-10 | Casual entropy default | Default entropy is "no event in 24+ hours" |
| R013-11 | No real-estate angles | No open-cabinet reveals, no curated interiors |
| R013-12 | No catalogue composition | ≥ 1 slightly-worn object in the active cluster |
| R013-13 | No bilaterally symmetric arrangement | No mirror-symmetric placements |
| R013-14 | Hotel-room/bathroom state markers | Hotel: ≥ 1 guest trace. Bathroom: ≥ 1 post-shower marker |
| R013-15 | Shopping bag lean rule | Bags lean, sit, or are held; not standing free |

---

## 6. Forbidden patterns (from research file §14)

The engine rejects any frame matching one of these patterns.

| FP ID | Pattern |
|---|---|
| FP-01 | Feature-object syndrome (one of each, well-composed) |
| FP-02 | Real-estate open storage (open cabinet, curated interior) |
| FP-03 | Catalogue composition (all "best of", no wear) |
| FP-04 | Bilateral symmetry (two-of-each, equally weighted) |
| FP-05 | Mood-prop pile-up (candle + flower + journal, soft light) |
| FP-06 | Time-of-day incoherence (lighting and objects from different times) |
| FP-07 | Uniform clutter (every surface equally cluttered) |
| FP-08 | Empty personal space (no photos, no magnets, no personal items) |
| FP-09 | Upright shopping bag (standing free in centre) |
| FP-10 | Hanger-ready clothes (wardrobe/fitting room, perfectly arranged) |
| FP-11 | Stock fitting room (empty, single hook, no residue) |
| FP-12 | OOTD fitting room (full outfit, mirror angled, no "no" pile) |
| FP-13 | Hotel-room stock (made bed, symmetric lamps, no traces) |
| FP-14 | Beauty counter bathroom (all products visible, mirror clean) |
| FP-15 | Event entropy without event (post-party look with no event specified) |

---

## 7. Interaction with sibling engines

### R012 (Conversation Illusion) — the engine reads from R012

R012's `second_person_trace` and `in_progress_residue` are R013's most-trusted inputs. R012 has the *narrative* context (what the conversation beat is) and R013 must produce the objects that *support* that narrative.

R013 can also *request* traces from R012: if R012 needs a "you_caught_me" trace, R013 can supply a "half-unpacked bag" or "tag still on" object to support that beat.

### R014 (Viewer Gaze) — the engine writes to and reads from R014

R013 reads R014's `attention_anchors` (foreground, mid-ground, background) to determine which objects should be visible at which depth. Objects that R014 wants as foreground anchors must be placed accordingly.

R013 writes the `object_audit_completeness` to R014 so R014 can factor it into the gaze itinerary.

### R015 (Persona Visual Anchor) — the engine reads from R015

R013 reads the persona's `object_signature` (dominant hand, sleep side, morning/evening routine) and uses it to ensure owner consistency across the frame.

### R011 (Scene Composition) — the engine reads from R011

R013 reads the scene's `location_type`, `time_of_day`, and `event_proximity_hours` to drive the object selection and state assignment.

---

## 8. Object-selection algorithm (summary)

For a given scene, the engine:

1. **Reads the persona's known objects** for the location (e.g., a study has her notebook, pen, coffee cup, phone, lamp; her laptop; her books; her chair).
2. **Filters by visibility** — which of these objects are visible from the camera angle? (Spatial check: is the object in the camera's frustum and at a visible depth?)
3. **Assigns the five attributes** to each visible object:
   - Owner: from the persona's signature (her, partner, child, pet).
   - Purpose: from the object's known purpose (drinking, writing, drying, etc.).
   - Last interaction: from the timeline, derived from the scene's time-of-day and the subject's current action.
   - Current state: derived from the last interaction and the object's known behaviour (e.g., a coffee cup 5 min after use is warm, half-full, with a condensation ring).
   - Visibility reason: spatial (where it is) and narrative (why it's in this beat).
4. **Identifies the active cluster** — the cluster of objects that the subject is currently interacting with or that is in the immediate vicinity of her current action.
5. **Identifies the baseline** — the rest of the visible objects, at rest, with no in-progress state.
6. **Identifies the in-progress residue** — objects that show the residue of recent activity (e.g., a half-eaten meal, an open book).
7. **Identifies the second-person traces** — objects that imply another person (a second cup, a pulled-out chair, a half-written note).
8. **Identifies closed and open storage** — default closed, with explicit justification for any open storage.
9. **Checks time-of-day coherence** — every object must be consistent with the lighting's implied time-of-day.
10. **Checks forbidden patterns** — rejects any frame matching FP-01…FP-15.
11. **Computes the realism_score** — see §9.

---

## 9. Realism scoring

```
overall = 0.25 * object_audit_completeness
        + 0.20 * active_cluster_clarity
        + 0.20 * use_signature_strength
        + 0.15 * time_coherence
        + 0.10 * (1 - any_FP_match)
        + 0.10 * second_person_trace_naturalness
```

Each sub-score is 0–1:
- `object_audit_completeness`: 1.0 if all visible objects have all 5 attributes, 0.0 if any are missing.
- `active_cluster_clarity`: 1.0 if exactly one cluster is active, 0.5 if multiple or none.
- `use_signature_strength`: 1.0 if all props have strong use-signatures, 0.5 if some are weak, 0.0 if any are missing.
- `time_coherence`: 1.0 if all objects match the lighting, 0.0 if any mismatch.
- `any_FP_match`: 1.0 if no forbidden pattern matches, 0.0 if any matches.
- `second_person_trace_naturalness`: 1.0 if a trace is present and in a natural position, 0.5 if present but staged, 0.0 if absent.

A frame with `overall < 0.6` is rejected. `0.6 ≤ overall < 0.8` is passed but flagged. `overall ≥ 0.8` is passed without flag.

---

## 10. Version and changelog

**v0.1.0** (2026-06-05) — Initial engine module. Canon status: BLOCKED.

**Planned for v0.2.0 (post-production-test):**
- Per-character tuning of the `object_signature`.
- Per-location-type tuning of the `known_objects_in_location` defaults.
- Per-time-of-day tuning of the `last_interaction` defaults.
- A learning loop that updates the realism_score based on human-rater feedback.

---

**End R013 engine spec.** Companion: R013_OBJECT_MOTIVATION_ENGINE.md (research), VERIFICATION_R013_OBJECT_MOTIVATION.md (verification).
