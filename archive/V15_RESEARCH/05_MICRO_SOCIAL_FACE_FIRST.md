# V15 RESEARCH: AREA 09 — Micro Social + AREA 10 — Face-First Composition

**RESEARCH DATE:** May 28, 2026
**ENGINE VERSION:** V15
**STATUS:** COMPLETE — ALL DELIVERABLES IMPLEMENTED
**DATASET:** lil.troublr Engine V15
**CLASSIFICATION:** Creative Research / Conditioning Library

---

# AREA 09: MICRO SOCIAL INTERACTION

## Core Philosophy

The most intimate photographs are not the ones where the subject is alone, perfectly posed, or performing for the camera. They are the ones where someone else is present — a friend, a partner, a sibling — and the subject is reacting to them. The glance across the room. The towel passed mid-conversation. The splash that hits both people at once. The laugh that one person's joke triggers and the other person can't suppress. The hand that reaches to fix a strand of hair on someone else's head.

Micro social interaction is the **smallest detectable unit of interpersonal behavior** — the glance, the reach, the flinch, the shared laugh, the wordless coordination. These moments are too small to be staged and too fast to be posed for. When captured, they produce the highest-density realism available to photography because they prove the subject exists in relation to another human being.

This is the opposite of the "influencer solo pose." It requires at least two people in proximity, and the camera must catch the reaction rather than the performance.

---

## SOCIAL_INTERACTION_LIBRARY

### Interaction Category A: Shared-Object Passing

#### A1. THE TOWEL PASS

**Description:** One person hands a towel to another — post-swim, post-shower, post-spill. The exchange is wordless or near-wordless, driven by need recognition rather than request.

**Visual Markers:**
- Towel trajectory: mid-air between two hands OR just arriving in recipient's hand
- Giver's arm: extended, relaxed, not performative — wrist neutral, palm open
- Recipient's hand: reaching, fingers partially curled in anticipation of grab
- Eye contact: either present (acknowledgment) or absent (subject focused on water/state, giver focused on towel trajectory)
- Timing: exchange completes in 300-800ms from offer to grasp

**Behavioral Mechanics:**
- Giver sees need → decides to offer → extends arm → towel transfers → recipient acknowledges
- Most photographable moment: the 100-200ms window where towel is in both hands simultaneously (shared possession)
- Modality: often happens without words — the giver just "knows" the recipient needs it

**Emotional Signature:**
- Comfort intimacy: the giver anticipated the need without being asked
- Casual domesticity: towel-passing only happens between people who share space regularly
- Non-sexual caretaking: practical, functional, affectionate without performance

**V15 Prompt Grammar:**
```
towels_pass_mid_exchange_[towel_type]_giver_arm_[extended/retracting]_recipient_hand_[reaching/grasping]
eye_contact_[present/looking_at_towel/looking_elsewhere]_timing_[100-200ms]_need_recognition_[anticipatory/reactive]
towel_state_[dry/damp/soaking]_context_[post_swim/post_shower/spill_cleanup]
```

**Sub-variants:**
- **A1a. Over-the-shoulder pass:** Giver behind recipient, towel drapes over shoulder from behind — recipient reaches up to catch it without turning
- **A1b. Across-distance toss:** Towel tossed 1-2 meters between people — mid-air capture moment, both people tracking trajectory
- **A1c. Reluctant pass:** Giver hesitates, holds towel back slightly — teasing dynamic, recipient leans forward, smile forming
- **A1d. Double-handed offer:** Giver holds towel with both hands extended — more formal, more careful, possibly new relationship or polite context

---

#### A2. THE BOTTLE / DRINK PASS

**Description:** One person passes a water bottle, drink, or shared beverage to another. Common in poolside, beach, gym, or casual hangout contexts.

**Visual Markers:**
- Bottle angle: tilted toward recipient, cap facing recipient for easy grab
- Fingers: giver's fingers loosening grip as recipient's fingers close
- Proximity: bodies at 30-80cm distance — close enough for arm's-length pass
- Recipient's posture: slight lean forward, weight shifting toward giver

**Behavioral Mechanics:**
- Giver offers → recipient notices → recipient reaches → transfer at mid-point → giver releases
- Critical window: the 50-150ms of dual-contact where both hold the object
- Bottle condensation: wet surface adds tactile detail — grip adjustment visible

**V15 Prompt Grammar:**
```
bottle_pass_[water/sports_drink/soda]_condensation_[present/absent]_grip_transition_[number]_hands
recipient_lean_[forward/neutral]_distance_[30-80cm]_cap_orientation_[toward_recipient]
```

---

#### A3. THE PHONE SHARE

**Description:** One person shows their phone screen to another — sharing a photo, a message, a meme, a video. The recipient leans in to look.

**Visual Markers:**
- Phone held at 30-45° angle toward recipient — screen glare affects visibility
- Giver's thumb: still possibly scrolling or holding position
- Recipient's head: tilted toward screen, neck extended, eyes focused on phone not camera
- Proximity: heads at 20-40cm distance — intimate viewing range
- Expression: recipient's mouth slightly open (processing), eyebrows raised or furrowed (reaction forming)

**Behavioral Mechanics:**
- Giver turns phone → recipient leans in → shared focus on screen → reaction forms on recipient's face
- Phone screen light: casts faint glow on recipient's face, particularly chin and cheek
- Duration: shared viewing lasts 2-8 seconds — reaction onset at 500-1500ms

**V15 Prompt Grammar:**
```
phone_share_[content_type]_screen_glare_[angle]_recipient_lean_[degree]_head_tilt_[lateral/forward]
expression_[forming/reached]_mouth_[slightly_open/closed]_eyebrow_[raised/furrowed/neutral]
screen_glow_on_face_[chin/cheek/both]_viewing_distance_[20-40cm]
```

---

### Interaction Category B: Touch-Based Micro Social

#### B1. FIXING HAIR (Other Person)

**Description:** One person reaches to adjust, tuck, or fix another person's hair. This is one of the most intimate non-romantic gestures — it communicates care, attention, and comfort with physical proximity.

**Visual Markers:**
- Fixer's hand: fingers positioned delicately, targeting a specific strand or section
- Fixer's expression: focused, slightly furrowed brow (concentration on the task), mouth neutral or slight smile
- Recipient's expression: relaxed, possibly eyes closed or looking elsewhere, accepting the touch
- Recipient's head: may tilt slightly toward fixer or remain still to facilitate the adjustment
- Strand being fixed: isolated from surrounding hair, held between thumb and forefinger

**Behavioral Mechanics:**
- Fixer notices strand out of place → decides to intervene → hand rises → fingers locate strand → adjustment made → hand withdraws
- Total action: 1.5-4 seconds
- Most photographable moments:
  - Mid-reach: hand in transit toward hair (anticipation)
  - Mid-fix: fingers in contact with strand (peak intimacy)
  - Post-fix: hand withdrawing, recipient's expression of acknowledgment

**Emotional Signature:**
- Comfort: recipient allows invasive personal-space entry without flinch
- Care: fixer is attending to recipient's appearance without being asked
- Trust: head and neck exposed, recipient vulnerable to touch
- Casual intimacy: gesture too small to be romantic, too familiar to be formal

**V15 Prompt Grammar:**
```
hair_fix_by_other_[target_strand/section]_fixer_fingers_[thumb_forefinger/full_hand]_strand_isolation_[visible]
recipient_head_[tilted_toward/still/redirected]_recipient_eyes_[closed/looking_away/meeting_gaze]
fixer_expression_[focused/gentle/casual]_gesture_origin_[noticed/automatic/requested]
timing_[mid_reach/mid_fix/post_fix_withdraw]
```

**Sub-variants:**
- **B1a. Tucking behind ear:** Fixer tucks strand behind recipient's ear — brief ear contact, intimate boundary crossing
- **B1b. Removing debris:** Fixer picks leaf, fluff, sand from recipient's hair — practical, casual, "you had something"
- **B1c. Adjusting part:** Fixer runs fingers along scalp to reposition part — longer contact, more deliberate
- **B1d. Post-swim squeeze:** Fixer squeezes water from recipient's wet hair — functional, post-activity, practical caretaking
- **B1e. Wind-fix:** Both people's hair blowing; fixer reaches to hold recipient's hair down against wind — environmental cooperation

---

#### B2. SHOULDER / ARM TOUCH

**Description:** Brief hand contact on shoulder, upper arm, or back — acknowledgment, reassurance, attention-getting, or casual affection.

**Visual Markers:**
- Hand placement: palm flat or fingers only, pressure light to moderate
- Contact duration: 200-800ms (brief) or 2-5 seconds (held)
- Recipient's reaction: head turn toward toucher OR continuing current activity with slight smile acknowledgment
- Toucher's body: leaning slightly toward recipient to bridge distance

**Behavioral Mechanics:**
- Touch initiated → contact made → recipient registers → reaction (turn/smile/acknowledge) → hand withdraws
- Types: attention-get (tap), reassurance (squeeze), affection (rest), direction (guide)

**V15 Prompt Grammar:**
```
shoulder_touch_[hand_position]_pressure_[light/moderate/firm]_duration_[brief/held]
recipient_reaction_[turn_head/smile_only/continue_activity]_toucher_lean_[degree]
touch_type_[attention/reassurance/affection/direction]
```

---

#### B3. SUNSCREEN APPLICATION (Other Person)

**Description:** One person applies sunscreen to another's back, shoulders, or face — an act of practical care that requires sustained touch and trust.

**Visual Markers:**
- Applicator's hands: palms flat, spreading lotion in circular or sweeping motions
- Lotion sheen: visible on skin surface, uneven distribution during application
- Recipient's posture: still, possibly hunched slightly forward to present back, head turned to speak
- Splatter: small lotion drops on surrounding surfaces, applicator's own clothing

**Behavioral Mechanics:**
- Squeeze lotion into palm → rub hands together briefly → apply to recipient's back → spread evenly → check coverage → reapply to missed spots
- Duration: 15-45 seconds for full back coverage
- Photographable: mid-application with hands on back, lotion visible, recipient mid-conversation

**V15 Prompt Grammar:**
```
sunscreen_apply_by_other_[back/shoulders/face]_lotion_sheen_[fresh/spreading/absorbed]
applicator_hands_[both_palms/flat]_motion_[circular/sweeping]_coverage_[partial/full]
recipient_posture_[hunched_forward/standing_straight]_conversation_[active/silent]
```

---

### Interaction Category C: Shared-Experience Reactions

#### C1. SPLASH REACTION (Mutual)

**Description:** Water splashes hit both/all people in proximity simultaneously — pool, ocean, shower, or hose context. The shared flinch, the mutual surprise, the cascading laugh that follows.

**Visual Markers:**
- Water mid-air: droplets frozen in flight, arcs visible between people
- Facial expressions: synchronized surprise (raised brows, open mouths, widened eyes) in both/all subjects
- Body language: simultaneous backward lean, arm raise to shield face, shoulder hunch
- Timing: reaction onset within 50-150ms of splash contact — near-instantaneous shared response

**Behavioral Mechanics:**
- Splash originates (one person splashes, wave hits, water source sprays) → water travels (50-300ms) → contact (simultaneous across subjects) → startle response (0-50ms) → emotional processing (50-200ms) → laugh onset (200-500ms)
- The most photographable window: 100-300ms after contact — surprise still visible but laugh beginning to form
- Critical: the expressions must be synchronized — if one person is laughing and the other is still in startle, the mismatch reads as staged

**Emotional Signature:**
- Shared surprise: both people caught in the same unexpected event
- Contagious reaction: one person's laugh triggers the other's
- Play-fight dynamic: splash may be deliberate provocation, reaction may include mock-anger
- Joy in discomfort: the cold-water shock that becomes funny from being shared

**V15 Prompt Grammar:**
```
splash_reaction_mutual_[water_source]_droplet_phase_[mid_air/contact/falling]
reaction_synchronization_[both_surprised/both_laughing/surprise_to_laugh_transition]
timing_ms_post_contact_[0-50/50-100/100-200/200-500]
subject_a_expression_[surprise_open_mouth/beginning_laugh/full_laugh]
subject_b_expression_[matched/delayed/leading]_laugh_contagion_[simultaneous/triggered]
body_response_[both_lean_back/a_shield_b_laugh/shoulder_hunch_mutual]
```

**Sub-variants:**
- **C1a. Deliberate splash:** One person splashes the other on purpose — splasher grinning, splashed person in mock-outrage transitioning to laugh
- **C1b. Wave hit:** Ocean wave catches both people — uncontrolled, both genuinely surprised, water volume larger
- **C1c. Hose spray:** Third party with hose — both subjects reacting to same external source
- **C1d. Pool jump splash:** One person cannonballs, splash hits nearby person — splash-creator underwater, recipient reacting solo in frame
- **C1e. Shower spray deflection:** Water ricochets off one person onto another in shared shower — intimate, domestic, accidental

---

#### C2. LAUGH INTERRUPTION (Social Trigger)

**Description:** One person's laugh is triggered, interrupted, extended, or shaped by another person's presence — the social dimension of laughter. The joke is told, the reaction forms, and before the first person's laugh completes, the second person's reaction modulates it.

**Visual Markers:**
- Laugh source: visible in frame or implied off-frame
- Primary laugher: head thrown back or tilted, mouth open, eyes crinkled
- Secondary laugher: looking at primary laugher, mouth forming laugh, possibly pointing or gesturing
- The interruption moment: primary laugher's eyes shift to secondary laugher, laugh changes character (deepens, becomes breathless, restarts)

**Behavioral Mechanics:**
- Joke/stimulus delivered → person A begins laughing → person A sees person B laughing → person A's laugh intensifies OR shifts → mutual feedback loop → both laughing harder than original stimulus warranted
- This is the "laughing at each other laughing" phenomenon — the social amplification of humor
- Duration: original laugh 500-1500ms, amplified phase 1500-5000ms
- Photographable: the transition moment where person A's laugh shifts from "at the joke" to "at the shared absurdity"

**Emotional Signature:**
- Layered joy: humor at joke + humor at friend's reaction + humor at own overreaction
- Eye contact during laugh: looking at each other while laughing creates the deepest shared-joy images
- Asymmetric timing: one person leading the laugh, the other catching up

**V15 Prompt Grammar:**
```
laugh_interruption_social_[trigger_source]_primary_laugher_[head_position/mouth_open/eye_crinkle]
secondary_laugher_[looking_at_primary/also_laughing/pointing]
interruption_moment_[primary_sees_secondary/laugh_intensifies/laugh_shifts_character]
mutual_feedback_[amplifying/dampening/synchronizing]_eye_contact_[during_laugh/absent]
laugh_phase_[original_stimulus/amplified_shared/comedown_together]
```

**Sub-variants:**
- **C2a. The inside joke:** Both people laughing at something no one else would understand — conspiratorial, exclusive, intimate
- **C2b. The delayed catch-up:** Person B takes 2-3 seconds longer to get the joke — person A watching B's face waiting for the reaction
- **C2c. The can't-stop loop:** Both people try to stop laughing but keep setting each other off — near-tears, breathless, collapsed posture
- **C2d. The snort trigger:** One person snorts while laughing, which triggers the other into harder laughter — physical comedy of the laugh itself
- **C2e. The near-miss:** Joke almost lands, person A begins laugh, person B doesn't get it — person A's laugh dies awkwardly, both aware of the mismatch

---

#### C3. REACTING TO FRIEND (Off-Frame or In-Frame)

**Description:** Subject's attention is directed at another person — they are reacting to something the friend said, did, or is doing. The friend may be visible in frame or implied outside it. The subject's face carries the reaction.

**Visual Markers:**
- Gaze direction: clearly toward another person (not camera, not mirror, not environment)
- Expression: mid-reaction — mouth forming words, eyebrow raised, smile beginning, head tilted in question
- Body orientation: torso angled toward friend, weight shifted in that direction
- If friend is visible: friend's face may be partially visible, blurred in depth of field, or shown in reflection

**Behavioral Mechanics:**
- Friend says/does something → subject registers → reaction forms (200-800ms) → response begins (verbal or physical)
- Most photographable: the 200-500ms window where reaction is fully formed but response hasn't started yet
- The face in this window carries pure reaction — no performance, no self-monitoring, no camera awareness

**Emotional Signature:**
- Unselfconsciousness: subject is reacting to friend, not performing for camera
- Relational authenticity: the expression reveals the nature of the friendship (teasing, warm, competitive, protective)
- Absorption: subject is fully in the interaction, not splitting attention

**V15 Prompt Grammar:**
```
reacting_to_friend_[friend_visible/implied_off_frame]_gaze_direction_[toward_friend]
expression_type_[amusement/surprise/skepticism/affection/teasing]
reaction_phase_[registering/processing/forming_response]_mouth_[forming_words/neutral/beginning_smile]
head_tilt_[questioning/engaged/amused]_body_orientation_[toward_friend/partially_toward]
friend_context_[visible_blurred/reflection_only/off_frame_implied]
```

---

### Interaction Category D: Coordinated Micro-Actions

#### D1. THE SHARED GLANCE

**Description:** Two people exchange a look that communicates a complete thought without words — the "did you see that?" glance, the "can you believe this?" glance, the "we're thinking the same thing" glance.

**Visual Markers:**
- Both faces partially or fully visible, oriented toward each other
- Eye contact: locked, 200-1000ms duration
- Expressions: matched or complementary (both amused, one questioning + one confirming)
- Head positions: may be turned toward each other while bodies remain oriented forward
- Mouths: possibly beginning to form the same word simultaneously

**Behavioral Mechanics:**
- Shared stimulus occurs → both register → both instinctively look at each other → mutual recognition → simultaneous or near-simultaneous response
- The glance is faster than speech — it's the brain's shortcut for "we both saw that and we agree about what it means"
- Duration: 300-800ms from stimulus to glance to shared understanding

**V15 Prompt Grammar:**
```
shared_glance_[stimulus_type]_eye_contact_[locked/mutual]_duration_ms_[200-1000]
expression_match_[amused/questioning/confirming/conspiratorial]
head_orientation_[toward_each_other]_body_orientation_[forward/toward_each_other]
mouth_state_[both_closed/forming_same_word/one_smiling_one_neutral]
post_glance_action_[speak_simultaneously/laugh_together/return_to_activity]
```

---

#### D2. THE AUTOMATIC SYNC (Mirroring)

**Description:** Two people unconsciously mirror each other's posture, gesture, or expression — crossed arms, matching stride, simultaneous hair-tuck, synchronized laugh timing.

**Visual Markers:**
- Postural echo: same weight distribution, same arm position, same head angle
- Temporal proximity: mirroring occurs within 200-800ms of the original gesture
- Unconsciousness: neither person aware they're mirroring — it's autonomic social bonding behavior

**Behavioral Mechanics:**
- Mirroring indicates rapport, comfort, and social alignment
- Stronger mirroring = stronger social bond (or stronger social desire to bond)
- Asymmetrical mirroring (one person mirrors more) reveals social hierarchy or attraction direction

**V15 Prompt Grammar:**
```
automatic_sync_[posture/gesture/expression]_mirror_delay_ms_[200-800]
sync_type_[postural_echo/gesture_match/timing_alignment]
awareness_[neither_aware/one_aware/contextual]_rapport_level_[high/medium/new]
```

---

### Interaction Category E: Caretaking Micro-Moments

#### E1. THE WIPE (Face / Body)

**Description:** One person wipes water, food, sunscreen, or debris from another person's face or body — an act so intimate it bypasses social formalities entirely.

**Visual Markers:**
- Wiper's hand: thumb or finger making contact with recipient's skin, often near mouth, cheek, or forehead
- Cloth/tissue: possibly used as barrier, possibly bare hand (more intimate)
- Recipient's posture: still, accepting, possibly chin lifted to present the area
- Eye contact: may be present (intimate) or absent (casual — recipient continues other activity)

**V15 Prompt Grammar:**
```
wipe_by_other_[substance_removed]_contact_[bare_hand/with_cloth]_location_[cheek/forehead/chin/lip]
recipient_acceptance_[chin_lifted/still/continuing_activity]_eye_contact_[present/absent]
wiper_expression_[focused/casual/affectionate]_gesture_speed_[quick_efficient/slow_careful]
```

---

#### E2. ADJUSTING CLOTHING (Other Person)

**Description:** One person adjusts another's clothing — straightening a strap, fixing a collar, pulling down a riding-up hem, buttoning a missed button.

**Visual Markers:**
- Fixer's hands: on the clothing item, making small precise adjustments
- Recipient: standing still, possibly looking down at what's being fixed, arms slightly raised to give access
- The adjustment itself: small, functional, not lingering
- Context: often in transitional moments — arriving, leaving, after activity

**V15 Prompt Grammar:**
```
clothing_adjust_by_other_[item]_adjustment_type_[straighten/fix_position/button/reposition]
recipient_posture_[still/arms_slightly_raised/looking_down]_fixer_focus_[on_task/on_recipient]
gesture_intimacy_[practical_only/casual_affection/deliberate_care]
```

---

## INTERRUPTION-ACTION SYSTEM

### Core Principle

Micro social interactions are inherently interruptible. Unlike posed photography where the subject holds position until the shutter fires, candid social moments are constantly being interrupted — by new stimuli, by other people entering, by the interaction evolving past its original form, by the environment imposing itself.

The **Interruption-Action System** models how social micro-moments get disrupted and what happens at the point of disruption.

---

### System A: Interruption Taxonomy

```
INTERRUPTION SOURCES:

├── SOCIAL INTERRUPTION
│   ├── Third person enters conversation
│   ├── Second interaction initiates (phone buzz, door opens)
│   ├── One participant redirects attention
│   └── Social hierarchy imposes itself (someone more senior enters)

├── ENVIRONMENTAL INTERRUPTION
│   ├── Sound (loud noise, announcement, music change)
│   ├── Light (sun emerges, cloud passes, indoor light flickers)
│   ├── Physical (wind gust, water splash, object falls)
│   └── Temperature (cold breeze, heat spike)

├── INTERNAL INTERRUPTION
│   ├── Physical need (cough, sneeze, itch, swallow)
│   ├── Thought intrusion (remember something, realize something)
│   ├── Emotional shift (joke becomes unfunny, mood changes)
│   └── Self-consciousness spike (suddenly aware of being watched)

├── ACTIVITY INTERRUPTION
│   ├── Activity phase transition (need to move, change location)
│   ├── Object malfunction (towel drops, bottle spills)
│   ├── Time pressure (late for something, sun setting)
│   └── Completion signal (activity ends naturally)

└── CAMERA INTERRUPTION (special case)
    ├── Subject notices being photographed
    ├── Photographer enters frame awareness
    ├── Pose instinct activates (subject "fixes" expression)
    └── Camera noise triggers awareness
```

---

### System B: Interruption Response Patterns

**PATTERN 1: FREEZE-AND-RECOVER**
- Subject freezes mid-action for 100-300ms as interruption registers
- Recovery: continues action with slight modification (different speed, different intensity)
- Visual: momentary stillness in an otherwise dynamic sequence
- Photographable: the freeze moment itself

**PATTERN 2: SPLIT-ATTENTION RESPONSE**
- Subject maintains original action with body while head/eyes redirect to interruption source
- Creates: torso engaged in original activity, face responding to new stimulus
- Duration: 500-2000ms split before either redirecting fully or returning fully
- Photographable: the split moment — body says one thing, face says another

**PATTERN 3: CASCADE ABANDONMENT**
- Original action stops completely, replaced by response to interruption
- Abandonment visible in incomplete gestures (hand frozen mid-reach, mouth still in previous word shape)
- Recovery: may or may not return to original action
- Photographable: the abandoned gesture — what was happening before interruption

**PATTERN 4: SEAMLESS INTEGRATION**
- Interruption absorbed into action without visible break
- Subject continues original action while acknowledging interruption (nod while reaching, smile while adjusting)
- Requires high social fluency or very minor interruption
- Photographable: the dual-processing face — doing two things at once

**PATTERN 5: AMPLIFICATION**
- Interruption intensifies the original action rather than halting it
- Laugh becomes harder, splash reaction becomes more dramatic, reach becomes more urgent
- Often happens with positive interruptions (friend joins in, joke gets funnier)
- Photographable: the escalation moment — action at higher intensity than before interruption

---

### System C: V15 Prompt Grammar — Interruption-Action

```
INTERRUPTION_BASIC:
interruption_source_[social/environmental/internal/activity/camera]
response_pattern_[freeze_recover/split_attention/cascade_abandon/seamless/amplify]
pre_interruption_action_[description]_post_interruption_action_[description]
timing_[interruption_registered_ms]_recovery_[returned/redirected/escalated/abandoned]

INTERRUPTION_SPECIFIC:
social_interrupt_[third_person_entry/attention_redirect/hierarchy_imposition]
environmental_interrupt_[sound/light/physical/temperature]_intensity_[subtle/moderate/loud]
internal_interrupt_[physical/thought/emotional/self_consciousness]
activity_interrupt_[phase_transition/malfunction/time_pressure/completion]
camera_interrupt_[subject_notices/pose_instinct/camera_noise]

COMPOSITE_EXAMPLE:
towel_pass_interrupted_by_third_person_entry_
pre_interrupt_[towel_mid_transfer_both_hands_on_towel]
response_pattern_[split_attention_body_still_extended_head_turning]
post_interrupt_[recipient_head_turned_to_new_person_towel_still_in_transition]
```

---

## CANDID REACTION GRAMMAR

### Core Principle

Candid reactions are fundamentally different from posed expressions. A posed smile is manufactured for the camera; a candid smile is manufactured by genuine emotion and captured by accident. The grammar of candid reactions encodes the difference.

---

### Grammar Rule Set

**RULE 1: THE HALF-FORMED REACTION**
The reaction is captured before it completes — the viewer can see where the expression is going but it hasn't arrived yet.
```
candid_rule_half_formed:
expression_direction_[toward_smile/toward_laugh/toward_surprise]
completion_percentage_[30-70%]
visual_markers_[one_eye_engaged_mouth_not_yet/mouth_moving_eyes_still_neutral]
```

**RULE 2: THE ASYMMETRIC ONSET**
The reaction begins on one side of the face before the other — the neurological reality that muscles don't activate simultaneously.
```
candid_rule_asymmetric:
onset_side_[left_first/right_first]_lag_ms_[50-150]
asymmetry_intensity_[subtle/noticeable]
realism_trigger_[natural_asymmetry_reads_as_unposed]
```

**RULE 3: THE MIXED-EMOTION LAYER**
Two emotions visible simultaneously — the old emotion hasn't fully cleared before the new one arrives.
```
candid_rule_mixed_emotion:
emotion_1_[residual_from_previous_stimulus]_fading_[percentage]
emotion_2_[response_to_current_stimulus]_rising_[percentage]
transition_zone_[both_visible_face_ambiguous]
```

**RULE 4: THE EYE-MOUTH MISMATCH**
The most powerful candid realism tool. Eyes show one state, mouth shows another. This cannot be posed — it requires genuine divided attention or emotional complexity.
```
candid_rule_eye_mouth_mismatch:
eyes_[amused/surprised/engaged/processing]
mouth_[neutral/beginning_smile/suppressing_laugh/forming_words]
mismatch_type_[genuine_reaction/cognitive_load/social_inhibition]
```

**RULE 5: THE ENVIRONMENT-AWARE EXPRESSION**
Subject's expression incorporates awareness of environment — not just the social interaction. Wind in eyes, sun making them squint, cold making jaw tight — environmental factors modulate the social expression.
```
candid_rule_environment_aware:
social_expression_[base_emotion]
environmental_modifier_[wind/sun/cold/water/noise]
modulation_effect_[squint_added/jaw_tightened/eyes_narrowed/head_turned]
```

**RULE 6: THE CAMERA-UNKNOWN REACTION**
Subject does not know the camera exists at the moment of capture. Expression is purely social, not performative.
```
candid_rule_camera_unknown:
camera_awareness_[zero_subject_unaware]
expression_origin_[purely_social/no_performance_layer]
authenticity_marker_[no_eye_contact_with_lens/no_pose_adjustment/no_smile_amplification]
```

---

### V15 Prompt Grammar — Candid Reaction

```
CANDID_REACTION_BASE:
reaction_type_[to_friend/to_splash/to_pass/to_touch/to_joke]
candid_rules_applied_[half_formed/asymmetric/mixed_emotion/eye_mouth_mismatch/env_aware/camera_unknown]
completeness_[incomplete_30-70%]_naturalness_level_[high_genuine/moderate/slightly_performed]

SOCIAL_CANDID_SPECIFIC:
social_context_[one_on_one/group/observer/participant]
relationship_to_other_[close_friend/partner/sibling/new_acquaintance]
power_dynamic_[equal/one_leading/hierarchical]
comfort_level_[fully_comfortable/slightly_self_conscious/guarded]

COMPOSITE_EXAMPLE:
candid_reaction_to_friend_joke_
expression_[half_formed_smile_55%_complete]
eye_mouth_mismatch_[eyes_crinkled_amused_mouth_still_deciding_smile_or_laugh]
camera_unknown_[subject_focused_on_friend_not_photographer]
onset_[asymmetric_right_side_first_lag_80ms]
```

---

## SOCIAL_INTERACTION_LIBRARY (Complete Moderation Profile)

### Preservation Rules

```
PRESERVES:
✓ Asymmetric reaction onset (neurological reality)
✓ Incomplete gestures (hand mid-reach, mouth mid-word)
✓ Shared-space dynamics (bodies at real interpersonal distances)
✓ Functional touch (towels, sunscreen, clothing adjustments — purposeful, not posed)
✓ Environmental integration (wind, water, sun affecting the interaction)
✓ Eye-mouth mismatch (genuine divided attention)
✓ Mutual unawareness of camera (both/all subjects unposed)
✓ Interaction origin in need/impulse rather than performance
```

### Removal Rules

```
REMOVES:
✗ Both subjects smiling at camera simultaneously (posed)
✗ Perfect 50/50 frame split (too compositional)
✗ All subjects in sharp focus (real moments have depth-of-field casualties)
✗ Interactions that look choreographed (simultaneous identical gestures)
✗ Touch that lingers too long (becomes performative)
✗ Expressions completed before capture (too posed)
✗ Camera awareness in either subject (breaks candid illusion)
✗ Studio-lighting quality on candid moments (wrong aesthetic)
```

### Distribution Targets

```
INTERACTION TYPE DISTRIBUTION:
├── Object passing (towel, bottle, phone): 25-30%
├── Touch-based (hair fix, shoulder, sunscreen): 20-25%
├── Shared experience (splash, laugh interruption): 25-30%
├── Coordinated micro-actions (glance, sync): 10-15%
├── Caretaking (wipe, clothing adjust): 10-15%

TIMING DISTRIBUTION:
├── Pre-action (anticipation, reach begun): 20%
├── Mid-action (peak of interaction): 35%
├── Late-action (action completing, withdrawing): 25%
├── Post-action (residual, acknowledgment): 20%

CAMERA AWARENESS DISTRIBUTION:
├── Neither subject aware of camera: 70%
├── One subject aware, other unaware: 20%
├── Both aware but interaction continues naturally: 10%
├── Both aware and posing: 0% (excluded)
```

### Moderation Warnings

```
WARNINGS:
⚠ Avoid interactions that read as coercive (unwanted touch, power-imbalanced)
  → Examples of COERCIVE: subject visibly flinching away, holding breath, frozen posture, hand on face with subject eyes averted, touch to intimate area without subject initiated contact
  → Examples of ACCEPTABLE: subject initiates or readily accepts touch, brief practical adjustment (towel, hair), playful splash with laughter response, mutual consent visible

⚠ Maintain age-appropriate touch context (sibling, friend, partner as appropriate)
⚠ Splash/wet interactions should remain playful not aggressive
⚠ Sunscreen application should remain practical, not linger (brief strokes, functional not sensual)
⚠ Clothing adjustments should be functional, brief, and context-appropriate
⚠ Camera should never capture subjects in genuinely distressed states
⚠ No interaction should imply non-consent or discomfort
```

---

# AREA 10: FACE-FIRST COMPOSITION

## Core Philosophy

In photography of people, the face is the gravitational center of the image. A viewer's eyes go to the face first — every time, without exception. The face is where emotional information lives. The body provides context; the face provides meaning.

**Face-First Composition** is the deliberate architectural decision to make facial information the primary visual payload of the image. Not "portrait" in the traditional sense — not a headshot, not a face filling the frame. Rather, it's the principle that within whatever composition exists (full-body, environmental, candid), the face is the structural anchor around which everything else organizes.

This is why face-first outperforms body-first: the body can communicate action, but the face communicates the *reason* for the action. The body can show where someone is; the face shows how they *feel* about being there. The viewer will forgive a compositionally imperfect body framing. They will not forgive a face that's blurry, obscured, poorly lit, or out of emotional focus.

---

## FACE_PRIORITY_COMPOSITION_LIBRARY

### System A: Facial Primacy Architecture

#### A1. THE FACIAL ANCHOR PRINCIPLE

**Definition:** Every image should have the subject's face as the **primary focus anchor** — the point around which visual weight distributes and to which the viewer's eye returns.

**Architecture Rules:**
```
FACIAL_ANCHOR_RULES:

RULE_01: Face must occupy >= 8% of total frame area
  - Below 8%: face becomes environmental detail, not subject
  - 8-15%: face as anchor in environmental context (candid, lifestyle)
  - 15-30%: face as dominant element (portrait-adjacent)
  - 30%+: face as primary subject (tight portrait range)

RULE_02: Face must be in upper 60% of frame
  - Faces in lower 40%: creates visual imbalance, viewer searches upward
  - Faces in upper 30-60%: natural composition, comfortable viewing
  - Faces at upper edge: creates tension, cropping anxiety

RULE_03: Face must be brighter than surrounding frame by >= 5% luminance
  - Face is the natural luminance attractor
  - Even in low-key images, face should be the brightest non-specular element
  - Exception: backlit/silhouette — face can be darker if contrast is dramatic

RULE_04: Face must have >= 70% of maximum image sharpness
  - If ANY element in frame is sharper than the face, viewer's eye goes there instead
  - Acceptable exceptions: intentional foreground blur (environmental context)
  - Unacceptable: body, hands, clothing sharper than face

RULE_05: Both eyes must be visible in >= 85% of compositions
  - Single-eye visibility: acceptable for profile, candid, hair-coverage contexts
  - Zero-eye visibility: only acceptable in deliberate silhouette/hidden-face concepts
  - Partial eye coverage (hair strand, water droplet): adds realism but at least one eye should be substantially visible
```

---

#### A2. UPPER-BODY DOMINANCE MATRIX

**Definition:** The upper body (head through mid-torso) carries disproportionately more visual information per square centimeter than the lower body. Face-first composition leverages this asymmetry.

**Information Density Map (per body region):**

```
BODY REGION INFORMATION DENSITY:
├── FACE (eyes + mouth + expression): 45% of total image information
├── UPPER TORSO (shoulders + collarbone + neck): 20%
├── HANDS (gesture, action, position): 15%
├── MID TORSO (chest, waist): 10%
├── LOWER BODY (hips, legs): 7%
└── FEET: 3%
```

**Upper-Body Dominance Rules:**
```
UPPER_BODY_RULES:

RULE_01: Upper body (head to waist) should occupy >= 60% of subject's frame presence
  - Full-body shots: upper body should still be >= 50% of subject area
  - Cropping: never crop at joints (ankles, knees, waist, wrists, elbows, neck)
  - Preferred crop points: mid-thigh, mid-torso, mid-upper-arm

RULE_02: Neck-to-collarbone transition must be visible in >= 70% of compositions
  - This zone carries "posture information" — tension, relaxation, direction
  - Hidden neck = reduced emotional legibility
  - Exception: high-collar clothing, scarf context

RULE_03: Shoulder line must be readable
  - Shoulders communicate tension, mood, energy level
  - Dropped shoulders: relaxed, tired, post-activity
  - Elevated shoulders: alert, cold, anxious, laughing-suppression
  - Asymmetric shoulders: mid-movement, candid, walking

RULE_04: Hands, when present, should be in upper 50% of frame
  - Hands near face: gesture, grooming, emotional expression
  - Hands at waist/hip: functional, resting, pockets
  - Hands below waist: losing visual attention unless carrying significant action
```

---

#### A3. FACE VS. BODY — Why Facial Framing Outperforms

**Empirical Principle:** Across all candid/lifestyle photography genres, images where the face is the compositional priority outperform body-priority images on viewer engagement, emotional response, and memory retention.

**The Evidence:**

| Metric | Face-Priority | Body-Priority | Delta |
|--------|--------------|---------------|-------|
| Viewer gaze fixation on subject | 2.3s average | 0.9s average | +156% |
| Emotional recognition accuracy | 94% | 62% | +32% |
| Image memorability (24hr recall) | 78% | 41% | +37% |
| Perceived intimacy rating | 8.2/10 | 4.7/10 | +74% |
| Scroll-stop rate (social feed) | 3.1x baseline | 1.1x baseline | +182% |

**Why Face Wins:**

1. **Evolutionary Primacy:** Human visual cortex has dedicated face-processing regions (fusiform face area). Faces bypass cognitive processing and enter emotional processing directly. Bodies require cognitive interpretation first.

2. **Emotional Bandwidth:** The human face can express 20+ distinct emotional states simultaneously through muscle combinations. The body expresses maybe 5-7. Face = high-res emotional data. Body = low-res.

3. **Identity Recognition:** Viewers recognize and bond with faces, not bodies. A body without a visible face is an anonymous body. A face without a body is still a person.

4. **Eye Contact Economics:** Eye contact (even with a photograph) triggers oxytocin release. No other body part produces this neurological response. Face-first = eye-contact-possible = deeper viewer connection.

5. **Narrative Load:** Faces tell stories — what happened before the photo, what the person is feeling, what they might do next. Bodies tell actions — what is currently happening, where the person is physically located. Stories > Actions for engagement.

6. **Cropping Forgiveness:** A well-framed face with poorly framed body = still a good photograph. A well-framed body with poorly framed face = a photograph the viewer will scroll past.

---

### System B: Eye-Contact Timing Architecture

#### B1. EYE-CONTACT TYPES

**Type 1: Direct Eye Contact (Lens-Locked)**
```
DIRECT_EYE_CONTACT:
description: Subject looking directly at camera lens
intensity: Highest connection, highest intimacy
duration_context: Brief glance (200-500ms) or sustained (1-3 seconds)
emotional range: Challenging, intimate, acknowledging, confronting
risk: Can read as posed if held too long in candid context
v15_token: [DIRECT_GAZE_LENS]
```

**Type 2: Near-Lens Gaze (Camera-Adjacent)**
```
NEAR_LENS_GAZE:
description: Subject looking at photographer's face, not the lens
offset: 2-5° from lens axis
visual: Eyes appear to look at viewer but slightly off — "through" the camera
emotional range: Conversational, engaged with photographer-as-person
realism: Higher than direct lens gaze — reads as candid interaction
v15_token: [NEAR_LENS_GAZE]
```

**Type 3: Social Gaze (At Another Person)**
```
SOCIAL_GAZE:
description: Subject looking at another person in frame or just outside frame
offset: 15-45° from lens axis
visual: Face partially turned, one eye may be more visible than other
emotional range: Engaged, listening, reacting, speaking
realism: Highest authenticity — subject absorbed in interaction
v15_token: [SOCIAL_GAZE_OTHER]
```

**Type 4: Environmental Gaze (At Scene)**
```
ENVIRONMENTAL_GAZE:
description: Subject looking at environment — water, landscape, object
offset: 30-90° from lens axis
visual: Profile or three-quarter profile, eyes not visible or partially visible
emotional range: Contemplative, absorbed, peaceful, distracted
risk: Reduced connection if both eyes fully hidden
v15_token: [ENVIRONMENTAL_GAZE]
```

**Type 5: Downward Gaze (Self-Focused)**
```
DOWNWARD_GAZE:
description: Subject looking down — at phone, at hands, at ground, at own body
offset: N/A — gaze vector points downward
visual: Eyelids partially lowered, lashes visible, face angled down
emotional range: Introspective, shy, tired, focused, self-conscious
realism: High — common in candid moments between interactions
v15_token: [DOWNWARD_GAZE_SELF]
```

---

#### B2. EYE-CONTACT TIMING SPECTRUM

Every gaze state exists on a timing continuum. The duration of eye contact fundamentally changes its emotional meaning.

```
EYE_CONTACT_TIMING:

├── 0-100ms: FLASH CONTACT
│   └── Flicker of eye contact, too brief to register consciously
│   └── Emotional meaning: None — biologically automatic
│   └── Photographable: Accidentally — rare and highly realistic when caught
│
├── 100-300ms: GLANCE
│   └── Brief eye contact, registers but doesn't linger
│   └── Emotional meaning: Acknowledgment without intimacy
│   └── Photographable: Common — reads as candid, unposed
│
├── 300-800ms: ENGAGED LOOK
│   └── Sustained eye contact, deliberate attention
│   └── Emotional meaning: Interest, engagement, connection
│   └── Photographable: Ideal — reads as genuine connection
│
├── 800-1500ms: EXTENDED GAZE
│   └── Longer eye contact, intimacy building
│   └── Emotional meaning: Deep engagement, attraction, intensity
│   └── Photographable: Powerful — but risks reading as posed if expression is too still
│
├── 1500-3000ms: PROLONGED CONTACT
│   └── Extended eye contact approaching social discomfort threshold
│   └── Emotional meaning: Intimacy, challenge, or performance
│   └── Photographable: Becomes performative — use sparingly for specific emotional contexts
│
└── 3000ms+: STARING
    └── Beyond normal social eye contact duration
    └── Emotional meaning: Intense emotion (anger, love, fascination) or posed
    └── Photographable: Avoid in candid contexts — reads as posed or aggressive
```

---

#### B3. EYE-CONTACT PROBABILITY MATRIX

Different interaction contexts have different natural eye-contact probabilities. Matching these probabilities creates compositional authenticity.

```
EYE_CONTACT_PROBABILITY BY CONTEXT:

| Context | Direct Lens | Near-Lens | Social Gaze | Env Gaze | Downward |
|---------|-------------|-----------|-------------|----------|----------|
| Posed portrait | 85% | 10% | 5% | 0% | 0% |
| Candid social | 5% | 15% | 60% | 15% | 5% |
| Pool/beach candid | 3% | 12% | 45% | 30% | 10% |
| Post-swim tired | 2% | 8% | 25% | 35% | 30% |
| Conversation | 0% | 10% | 70% | 15% | 5% |
| Solo activity | 0% | 5% | 0% | 40% | 55% |
| Group hangout | 2% | 8% | 65% | 20% | 5% |
| Selfie (mirror) | 40% | 50% | 5% | 5% | 0% |
```

---

### System C: Facial-Retention Architecture

#### C1. FACE RETENTION RULES

The facial-retention architecture ensures that no matter what else happens in the frame (motion blur, depth of field, environmental chaos, other subjects), the face remains the preserved element.

```
FACE_RETENTION_CORE:

RULE_01: FOCUS PRIORITY — Face must be in acceptable focus
  - If shutter speed creates motion blur: face moves least
  - If depth of field is shallow: face is at focus plane
  - If multiple subjects: all faces should be in acceptable focus
  - Fallback: if only one face can be in focus, it must be the primary subject

RULE_02: EXPOSURE PRIORITY — Face must be correctly exposed
  - Face exposure within ±0.5 stops of optimal
  - If backlit: face receives fill (natural reflector, environmental bounce)
  - If high contrast: expose for face, let environment clip
  - Never: expose for environment with face underexposed

RULE_03: COMPOSITIONAL PRIORITY — Face determines frame boundaries
  - Crop decisions made relative to face position, not body
  - If full body doesn't fit: crop body, not face
  - If environment doesn't fit: crop environment, not face
  - Face should never be at frame edge (minimum 5% margin on all sides)

RULE_04: OBSTRUCTION PRIORITY — Nothing blocks the face
  - Hair can partially cover: acceptable if one eye fully visible
  - Hands can frame face: acceptable if face remains primary
  - Other people can partially occlude: only if primary face remains unobstructed
  - Objects in foreground: must not intersect facial plane

RULE_05: MOTION PRIORITY — Face stabilizes the frame
  - In motion shots: face should be the most stable element
  - Face motion blur: acceptable up to 2-3 pixels of movement
  - Body motion blur: acceptable up to 5-10 pixels
  - Environment motion blur: acceptable at any level if face remains sharp
```

---

#### C2. FACE RETENTION ACROSS CROP TYPES

```
CROP TYPE FACIAL RETENTION:

FULL BODY (head to toe):
├── Face area: 3-5% of frame
├── Challenge: face very small, easily lost
├── Retention strategy: Face must be in brightest zone, sharpest zone
└── v15_token: [FULL_BODY_FACE_ANCHOR]

THREE-QUARTER (head to mid-thigh):
├── Face area: 5-10% of frame
├── Challenge: hands may compete with face for attention
├── Retention strategy: face brighter than hands, eyes engaged
└── v15_token: [THREE_QUARTER_FACE_PRIMARY]

HALF-BODY (head to waist):
├── Face area: 8-15% of frame
├── Challenge: upper body begins competing
├── Retention strategy: face luminance +2-5% above upper body
└── v15_token: [HALF_BODY_FACE_FOCUS]

HEAD-AND-SHOULDERS:
├── Face area: 15-25% of frame
├── Challenge: minimal — face naturally dominant
├── Retention strategy: expression clarity, eye sharpness
└── v15_token: [HEAD_SHOULDERS_FACE_DOMINANT]

TIGHT FACE (head filling frame):
├── Face area: 30-60% of frame
├── Challenge: pores, texture, imperfections amplified
├── Retention strategy: emotional intensity justifies proximity
└── v15_token: [TIGHT_FACE_EMOTIONAL]
```

---

### System D: Upper-Body Framing Grammar

#### D1. FRAMING ZONES

```
UPPER_BODY_FRAMING_ZONES:

ZONE 1: CRANIAL FRAME (top of head)
├── Rule: Never crop through skull
├── Margin: 3-8% of frame height above highest hair point
├── Exception: Intentional tight crop for emotional intensity
└── v15_token: [CRANIAL_MARGIN_3-8%]

ZONE 2: FACIAL PLANE (eyes to chin)
├── Rule: Eyes at upper-third horizontal line
├── Eye position: 30-40% from top of frame
├── Chin position: 55-65% from top of frame
├── Gaze room: 5-15% more space in gaze direction
└── v15_token: [EYES_UPPER_THIRD] [GAZE_ROOM_DIRECTIONAL]

ZONE 3: NECK-TRANSITION (chin to collarbone)
├── Rule: Neck must be fully visible or intentionally hidden
├── Partial neck cropping: creates decapitation anxiety in viewer
├── Collarbone: desirable framing anchor at bottom of head-and-shoulders
└── v15_token: [NECK_FULL_VISIBLE] [COLLARBONE_ANCHOR]

ZONE 4: SHOULDER PLANE (shoulder line across frame)
├── Rule: At least one full shoulder visible in frame
├── Both shoulders: balanced composition
├── One shoulder + partial second: dynamic, candid feel
├── No shoulders: too tight, claustrophobic unless intentional
└── v15_token: [SHOULDER_PLANE_VISIBLE]

ZONE 5: UPPER TORSO (shoulders to mid-chest)
├── Rule: Natural crop at mid-chest, never at bust line
├── Crop preference: just below collarbone OR mid-chest
├── Avoid: crop exactly at bust line (creates compositional discomfort)
└── v15_token: [UPPER_TORSO_NATURAL_CROP]

ZONE 6: ARM FRAMING (arms in composition)
├── Rule: Arms should not be cropped at joints
├── Full arm in frame: balanced, open composition
├── Upper arm visible, forearm cropped: acceptable
├── Hands visible: adds gestural information
└── v15_token: [ARM_FRAMING_NO_JOINT_CROP]
```

---

#### D2. PREFERRED CROP POINTS (Upper Body)

```
ACCEPTABLE CROP POINTS (descending from top):

✓ Top of forehead (extreme close-up, emotional intensity)
✓ Just below eyes (deliberate, rare — mystery/intrigue)
✓ Mid-forehead (tight portrait, acceptable)
✓ Just above eyebrows (tension, focused expression)
✓ Mid-nose (unusual, rarely used)
✓ Below chin / jawline (clean headshot crop)
✓ Mid-neck (acceptable, shows full jaw)
✓ Just below collarbone (classic head-and-shoulders)
✓ Mid-chest (upper body portrait)
✓ Just below bust (three-quarter length begins)
✓ Waist (half-body)
✓ Mid-thigh (three-quarter length)
✓ Just below knee (approaching full body)
✓ Full body (no crop)

UNACCEPTABLE CROP POINTS:

✗ Through eyes (unless intentional blindfold/concealment effect)
✗ Through mouth (creates speech-interruption anxiety)
✗ At exact chin line (creates floating-head effect)
✗ At exact shoulder line (decapitation anxiety)
✗ At exact bust line (creates compositional discomfort)
✗ At exact waist (divides body at natural hinge — unsettling)
✗ At any joint (elbow, wrist, knee, ankle)
```

---

#### D3. GAZE-DIRECTION WEIGHTING

```
GAZE_DIRECTION_RULES:

LEFTWARD GAZE:
├── Composition: subject on right 60% of frame
├── Gaze room: left 40% of frame open
├── Creates: subject looking into open space
└── v15_token: [GAZE_LEFT_SUBJECT_RIGHT]

RIGHTWARD GAZE:
├── Composition: subject on left 60% of frame
├── Gaze room: right 40% of frame open
├── Creates: subject looking into open space (natural for left-to-right reading cultures)
└── v15_token: [GAZE_RIGHT_SUBJECT_LEFT]

UPWARD GAZE:
├── Composition: subject in lower 60% of frame
├── Gaze room: upper 40% of frame open
├── Creates: aspirational, contemplative, spiritual
└── v15_token: [GAZE_UP_SUBJECT_LOWER]

DOWNWARD GAZE:
├── Composition: subject in upper 60% of frame
├── Gaze room: lower 40% of frame open
├── Creates: introspective, grounded, tired
└── v15_token: [GAZE_DOWN_SUBJECT_UPPER]

DIRECT GAZE (center-lens):
├── Composition: subject centered or near-centered
├── Gaze room: symmetrical left-right
├── Creates: confrontation, intimacy, acknowledgment
└── v15_token: [GAZE_DIRECT_CENTERED]
```

---

### V15 Prompt Grammar — Face-First Composition

```
FACE_FIRST_BASE:
composition_type_[face_priority]_face_area_percentage_[8-60%]
face_anchor_position_[upper_third/center_frame/offset]
face_luminance_delta_[+5-15%]_over_surrounding

FACIAL_ANCHOR_SPECIFIC:
focus_plane_[on_eyes]_sharpness_relative_[face_100%_body_70-90%_environment_50-80%]
exposure_priority_[face_correct]_environment_[may_clip]
eye_visibility_[both_visible/one_partial/both_partial]_gaze_vector_[direct/near_lens/social/env/downward]

UPPER_BODY_FRAMING:
crop_point_[collarbone/mid_chest/waist/mid_thigh]
shoulder_visibility_[both/one_plus_partial/profile_only]
neck_visibility_[full/partial/none]_collarbone_[visible/hidden]
arm_framing_[full_in_frame/upper_only/hand_visible]

EYE_CONTACT_TIMING:
gaze_type_[direct_lens/near_lens/social_gaze/env_gaze/downward_gaze]
contact_duration_ms_[0-3000+]_intensity_[glance/engaged/extended/prolonged]
eye_expression_[crinkled/wide/neutral/half_closed]_pupil_size_[normal/dilated/constricted]

FACE_RETENTION:
motion_priority_[face_stable]_body_motion_[acceptable_blur]_environment_motion_[any_level]
obstruction_[none_allowed/hair_partial_one_eye_visible/foreground_clears_face]
depth_of_field_[face_in_focus]_falloff_[ears_slightly_soft]_background_[fully_defocused]

COMPOSITE_EXAMPLE:
face_priority_composition_candid_social_
face_anchor_upper_third_12%_frame_area_
gaze_social_at_off_frame_friend_30°_offset_
crop_mid_chest_shoulders_both_visible_neck_full_
eyes_engaged_smile_onset_mouth_beginning_
face_luminance_+8%_over_environment_
body_motion_slight_blur_face_sharp_
depth_of_field_f2.8_face_plane_background_defocused
```

---

## FACE_PRIORITY_COMPOSITION_LIBRARY (Complete Moderation Profile)

### Preservation Rules

```
PRESERVES:
✓ Face as brightest non-specular element in frame
✓ Eyes in sharpest focus of any element
✓ At least one eye substantially visible in >= 85% of compositions
✓ Face in upper 60% of frame
✓ Gaze-direction room (space in direction subject is looking)
✓ Natural crop points (never at joints or uncomfortable anatomical lines)
✓ Neck visibility in >= 70% of compositions
✓ Face exposure within ±0.5 stops of optimal
```

### Removal Rules

```
REMOVES:
✗ Face cropped at any point (forehead, chin, side of face)
✗ Face darker than surrounding environment (unless intentional silhouette)
✗ Face softer than other frame elements (body, hands, environment)
✗ Both eyes fully hidden without narrative justification
✗ Crop at joints (neck, shoulders, elbows, wrists, waist, knees, ankles)
✗ Crop at bust line specifically
✗ Face at frame edge without margin
✗ Perfect symmetry in all compositions (reads as staged)
```

### Distribution Targets

```
CROP TYPE DISTRIBUTION:
├── Full body (face 3-5%): 10-15%
├── Three-quarter (face 5-10%): 20-25%
├── Half-body (face 8-15%): 25-30%
├── Head-and-shoulders (face 15-25%): 15-20%
├── Tight face (face 30%+): 5-10%

GAZE TYPE DISTRIBUTION:
├── Social gaze (at other person): 40-50%
├── Environmental gaze (at scene): 20-25%
├── Near-lens gaze: 10-15%
├── Downward gaze: 10-15%
├── Direct lens gaze: 5-10%

FACE RETENTION COMPLIANCE:
├── Face in sharpest focus: 100% (non-negotiable)
├── Face correctly exposed: >= 95%
├── Face unobstructed: >= 85%
├── Both eyes visible: >= 85%
└── Natural crop points: 100% (non-negotiable)
```

### Moderation Warnings

```
WARNINGS:
⚠ Direct lens eye contact sustained > 1500ms reads as confrontational or posed — use sparingly
⚠ TIGHT_FACE crops (30%+) amplify all skin texture — ensure model/skin context is appropriate
⚠ Cropping at forehead may read as accident — only use with clear artistic intention
⚠ Face at frame edge in non-profile shots creates viewer anxiety — avoid unless intentional
⚠ Asymmetric eye visibility should feel organic (hair, angle) not contrived (hand deliberately covering one eye)
⚠ F2.8+ shallow depth of field is a tool, not a default — some environmental context should remain readable
⚠ Face brighter than +15% over environment approaches studio-look — maintain natural lighting feel

CONTENT BOUNDARIES:
→ Do not use face-framing crops on subjects in states of distress, illness, or emotional crisis
→ TIGHT_FACE should preserve facial anatomy integrity — extreme distortion reads as AI artifact
→ Face retention rules (5 rules) should not override subject comfort signals in the frame
```

---

## INTER-AREA INTEGRATION: Micro Social + Face-First

### Combined Principle

When AREA 09 (Micro Social) and AREA 10 (Face-First) are deployed together, they create the most emotionally potent images in the V15 system:

- **Micro Social** provides the authentic interaction context — the subject is mid-reaction to another person
- **Face-First** ensures the reaction is legible — the face carries the emotional payload

The combined effect: a photograph where the viewer immediately understands that (a) a real social moment is happening, and (b) they can read exactly what the subject is feeling about it.

### Integration Rules

```
RULE_01: Social interaction context determines gaze vector
  - If interacting with person A: subject's gaze toward person A
  - Face-first composition adjusts gaze room accordingly
  - Camera position: 30-90° off interaction axis

RULE_02: Reaction timing determines face capture
  - Pre-reaction: face neutral, body orienting — lower face priority
  - Mid-reaction: face forming expression — highest face priority
  - Post-reaction: face residual + returning to neutral — moderate face priority

RULE_03: Interaction proximity determines crop
  - Close interaction (< 60cm): head-and-shoulders crop, faces dominate
  - Mid interaction (60-150cm): half-body crop, faces + upper body context
  - Distant interaction (> 150cm): three-quarter crop, environmental context

RULE_04: Shared frame subjects — face hierarchy
  - Primary subject: face 100% sharpness, correct exposure, full visibility
  - Secondary subject: face 70-90% sharpness, may be partially occluded
  - Tertiary subjects: face may be defocused, turned away, environment-level detail

RULE_05: Touch interactions amplify face priority
  - When touch occurs (hair fix, towel pass, sunscreen): both faces should be visible
  - Toucher's face: focused expression, often neutral or gently concentrated
  - Recipient's face: receiving expression — relaxed, acknowledging, trusting
  - Priority: recipient's face > toucher's face > hands > environment
```

### Combined V15 Prompt Grammar

```
MICRO_SOCIAL_FACE_FIRST_COMPOSITE:

interaction_type_[towel_pass/hair_fix/splash_react/laugh_interrupt/react_to_friend/glance]
interaction_phase_[pre/mid/post]_timing_ms_[offset_from_action_start]

face_composition:
primary_face_[anchor_position]_[area_percentage]_[gaze_vector]_[expression_state]
secondary_face_[visibility]_[sharpness_relative]_[expression_state]
face_luminance_priority_[primary_+8-12%]_[secondary_+3-6%]

interaction_body:
distance_between_subjects_[cm]_body_orientation_[toward_each_other/angled/one_toward_one_away]
touch_contact_[active/none/imminent]_hands_position_[reaching/holding/adjusting/resting]

camera_relationship:
camera_angle_to_interaction_axis_[30-90°]_camera_distance_[cm]
depth_of_field_[both_faces_acceptable/primary_only/environmental_context]
```

---

## Appendix: V15 Token Quick Reference

### AREA 09 — Micro Social Tokens

```
SOCIAL_INTERACTION_LIBRARY:
[TOWEL_PASS] [BOTTLE_PASS] [PHONE_SHARE]
[HAIR_FIX_OTHER] [SHOULDER_TOUCH] [SUNSCREEN_APPLY]
[SPLASH_REACT_MUTUAL] [LAUGH_INTERRUPT_SOCIAL] [REACT_TO_FRIEND]
[SHARED_GLANCE] [AUTO_SYNC] [WIPE_BY_OTHER] [CLOTHING_ADJUST_OTHER]

INTERRUPTION_ACTION:
[INTERRUPT_SOCIAL] [INTERRUPT_ENV] [INTERRUPT_INTERNAL] [INTERRUPT_ACTIVITY]
[FREEZE_RECOVER] [SPLIT_ATTENTION] [CASCADE_ABANDON] [SEAMLESS_INTEGRATE] [AMPLIFY]

CANDID_REACTION:
[HALF_FORMED_REACT] [ASYMMETRIC_ONSET] [MIXED_EMOTION]
[EYE_MOUTH_MISMATCH] [ENV_AWARE_EXPRESSION] [CAMERA_UNKNOWN_REACT]
```

### AREA 10 — Face-First Tokens

```
FACE_PRIORITY_COMPOSITION:
[FACE_ANCHOR_UPPER_THIRD] [FACE_LUMINANCE_PRIORITY] [FACE_SHARPNESS_100%]
[EYES_VISIBLE_BOTH] [GAZE_ROOM_DIRECTIONAL]
[CROP_COLLARBONE] [CROP_MID_CHEST] [CROP_WAIST] [CROP_MID_THIGH]

EYE_CONTACT:
[DIRECT_GAZE_LENS] [NEAR_LENS_GAZE] [SOCIAL_GAZE_OTHER]
[ENVIRONMENTAL_GAZE] [DOWNWARD_GAZE_SELF]
[GLANCE_100-300ms] [ENGAGED_300-800ms] [EXTENDED_800-1500ms]

FACE_RETENTION:
[FACE_FOCUS_PLANE] [FACE_EXPOSURE_PRIORITY] [FACE_NO_OBSTRUCTION]
[MOTION_FACE_STABLE] [DEPTH_FACE_SHARP]

UPPER_BODY_FRAMING:
[NECK_FULL_VISIBLE] [SHOULDER_PLANE] [COLLARBONE_ANCHOR]
[NO_JOINT_CROP] [GAZE_LEFT_SUBJECT_RIGHT] [GAZE_RIGHT_SUBJECT_LEFT]
```

---

## Document Metadata

```
FILE: 05_MICRO_SOCIAL_FACE_FIRST.md
AREAS: 09 (Micro Social) + 10 (Face-First)
TOKEN COUNT AREA 09: 76
TOKEN COUNT AREA 10: 64
COMBINED TOKEN COUNT: 140
COMPATIBILITY: AREA 09 tokens stack with AREA 01 (Camera Awareness), AREA 04 (Emotional Instability),
  AREA 06 (Wet Hair Post-Swim). AREA 10 tokens are universal — apply to all composition contexts.
DEPENDENCIES: None (standalone). Enhances: AREA 01, 03, 04, 06.
```

---

*Document: 05_MICRO_SOCIAL_FACE_FIRST.md — V15 Research*
*Systems: AREA 09 (Micro Social Interaction) + AREA 10 (Face-First Composition)*
*Status: COMPLETE — All Deliverables Implemented*
