# R020 — Character Preservation Engine

**Mission:** Research why certain environments overpower character identity and how to preserve lil.troublr identity across scenes.

**Scope lens:** lil.troublr-specific identity preservation, with general virtual-influencer methods.

**Canon status:** BLOCKED until production testing. Research proceeds now; promotion to canon is blocked until production testing confirms improved retention, realism, recognisability, or attachment.

**Research sources considered:** Japanese gravure, Xiaohongshu, Instagram female influencers, lingerie campaigns, swimwear campaigns, editorial fashion, luxury gifting campaigns, sports/lifestyle/street photography, virtual influencer production, and visual attention research.

---

## Executive thesis

The successful image is not merely higher quality. It gives the viewer a controlled reason to keep looking after the first recognition pass. Beauty opens the door; a social, behavioural, or curiosity anchor keeps the viewer inside the frame. Production prompts must therefore specify **attention routing**, not just subject description.

---

## Findings

### Finding 1: Activities overpower identity when role nouns replace character nouns

**Finding**  
Activities overpower identity when role nouns replace character nouns

**Why It Works**  
Prompts like athlete, swimmer, businesswoman, model, idol, tourist, and luxury girl carry strong visual priors. The generator follows the role stereotype and discards the character signature.

**Visual Trigger**  
Uniformed body, generic sport pose, changed face ratio, changed personality expression.

**Prompt Translation**  
Write character first, role second: "lil.troublr remains herself first; the sport is something she is doing today, not a new identity."

**Expected Production Impact**  
Reduces generic-athlete drift in sports and action frames.

**Confidence**  
High

---

### Finding 2: Identity lock needs face, body, and behaviour simultaneously

**Finding**  
Identity lock needs face, body, and behaviour simultaneously

**Why It Works**  
Face lock alone is insufficient. If body language and expression change to match the environment stereotype, the character feels replaced. Stable identity requires repeated face geometry, body proportions, expression grammar, and behavioural habits.

**Visual Trigger**  
Same face landmarks, same softness/height/body rhythm, same teasing/local-girl response style.

**Prompt Translation**  
Use a four-part lock: "face identity preserved; body proportions preserved; expression signature preserved; behavioural signature preserved."

**Expected Production Impact**  
Improves recognisability across outfits, sports, nightlife, home, street, and editorial.

**Confidence**  
High

---

### Finding 3: Environment should frame her habits, not overwrite them

**Finding**  
Environment should frame her habits, not overwrite them

**Why It Works**  
A scene preserves character when the environment shows how she behaves there. A scene replaces character when it simply dresses her as the environment.

**Visual Trigger**  
Personal objects, small hesitation, local routine, familiar posture, not full costume transformation.

**Prompt Translation**  
Prompt: "environment supports her existing personality: she uses the gym/market/beach in her own slightly teasing, lived-in way."

**Expected Production Impact**  
Turns locations into character evidence instead of costume categories.

**Confidence**  
High

---

### Finding 4: Wardrobe and styling must contain a signature carry-over

**Finding**  
Wardrobe and styling must contain a signature carry-over

**Why It Works**  
High-variance outfits cause identity drift unless at least one styling signature persists: hair handling, makeup softness, jewelry scale, colour bias, accessory type, silhouette comfort zone.

**Visual Trigger**  
Recurring earrings, hair part, natural makeup, strap/neckline preference, phone case, small charm.

**Prompt Translation**  
Add: "one signature carry-over remains visible even in the new environment."

**Expected Production Impact**  
Maintains continuity without making every outfit identical.

**Confidence**  
Medium-High

---

### Finding 5: Action scenes need personality residue after the action

**Finding**  
Action scenes need personality residue after the action

**Why It Works**  
During intense movement, the body must serve the action. Identity can re-enter through pre-action or post-action residue: smile after missing, annoyed little laugh, hair-fixing, checking a friend, casual object use.

**Visual Trigger**  
After-effort expression, personal reaction, social trace, imperfect recovery.

**Prompt Translation**  
Use: "capture the recovery beat after the action; her personality returns through the reaction, not through posing during the action."

**Expected Production Impact**  
Preserves realism while keeping lil.troublr recognisable.

**Confidence**  
High


---

## Identity preservation stack

1. **Face lock** — facial geometry, eye shape, nose-mouth relation, face softness.
2. **Body lock** — proportions, posture tendency, shoulder/neck rhythm, movement scale.
3. **Personality lock** — teasing softness, local-girl casualness, slightly mischievous response.
4. **Behaviour lock** — how she touches objects, reacts to being seen, recovers from action.
5. **Styling carry-over** — one consistent hair/makeup/accessory/silhouette signature.

## Production rules

- Character name and identity contract must come before scene role.
- Avoid strong stereotype nouns as the dominant subject label.
- In action scenes, preserve personality through recovery beat rather than impossible eye contact during peak action.
- Environment supports identity by showing her habits inside it.


---

## Anti-patterns

- **Pretty but solved:** the image can be understood in under one second.
- **Environment-first:** location colour and decoration dominate the human question.
- **All-over sharpness:** every detail competes; no route exists.
- **Role replacement:** the scene noun replaces character identity.
- **Unjustified eye contact:** lens gaze appears where task gaze is physically required.
- **Too many clues:** curiosity collapses into clutter.
- **Product catalogue logic:** product is displayed but not used, touched, hidden, gifted, or reacted to.

---

## Production testing plan

1. Generate 20 frames using current baseline prompts.
2. Generate 20 frames using this engine's prompt contract.
3. Compare: first-glance stop, 3-second hold, zoom-in rate, re-look rate, identity recognisability, realism failure count.
4. Promote only rules with clear production win; keep unclear rules as experimental.

---


## Sources and further reading

1. Itti, L., & Koch, C. (2000). A saliency-based search mechanism for overt and covert shifts of visual attention. *Vision Research*. https://doi.org/10.1016/S0042-6989(99)00163-7
2. Yarbus, A. L. (1967). *Eye Movements and Vision*. Springer. https://link.springer.com/book/10.1007/978-1-4899-5379-7
3. Henderson, J. M. (2003). Human gaze control during real-world scene perception. *Trends in Cognitive Sciences*. https://doi.org/10.1016/S1364-6613(03)00148-1
4. Cerf, M., Frady, E. P., & Koch, C. (2009). Faces and text attract gaze independent of the task. *Journal of Vision*. https://doi.org/10.1167/9.12.10
5. Bakhshi, S., Shamma, D. A., & Gilbert, E. (2014). Faces engage us: Photos with faces attract more likes and comments on Instagram. CHI. https://doi.org/10.1145/2556288.2557403
6. Kampe, K. K. W., Frith, C. D., Dolan, R. J., & Frith, U. (2001). Reward value of attractiveness and gaze. *Nature*. https://doi.org/10.1038/35098149
7. Horton, D., & Wohl, R. R. (1956). Mass communication and para-social interaction. *Psychiatry*. https://doi.org/10.1080/00332747.1956.11023049
8. Loewenstein, G. (1994). The psychology of curiosity: A review and reinterpretation. *Psychological Bulletin*. https://doi.org/10.1037/0033-2909.116.1.75
9. Berlyne, D. E. (1960). *Conflict, Arousal, and Curiosity*. McGraw-Hill. https://archive.org/details/conflictarousalc0000berl
10. Ruiz, N., Li, Y., Jampani, V., Pritch, Y., Rubinstein, M., & Aberman, K. (2023). DreamBooth: Fine Tuning Text-to-Image Diffusion Models for Subject-Driven Generation. CVPR. https://arxiv.org/abs/2208.12242
11. Ye, H., Zhang, J., Liu, S., Han, X., & Yang, W. (2023). IP-Adapter: Text Compatible Image Prompt Adapter for Text-to-Image Diffusion Models. https://arxiv.org/abs/2308.06721
12. Wang, Q., Bai, X., Wang, H., Qin, Z., & Chen, A. (2024). InstantID: Zero-shot Identity-Preserving Generation in Seconds. https://arxiv.org/abs/2401.07519


---

# PART 10: DEEPSEEK V4 PRO VERIFICATION & EXTENSION

**Verification date:** 2026-06-06
**Model:** deepseek-chat
**Scope:** content verify + extend

## Verification & Extension Report: R020 — Character Preservation Engine

**Verdict:** **PARTIALLY VALID — Production-ready logic with critical gaps in attention mechanics, identity decay modeling, and testing methodology.**

---

### Strengths

1. **Attention routing thesis is correct.** The shift from "higher quality" to "controlled reason to keep looking" aligns with Yarbus (1967) and Henderson (2003) — gaze is task-driven, not saliency-driven. This is underutilized in current production.

2. **Five-layer identity stack** (face, body, personality, behaviour, styling) is structurally sound. It mirrors real-world character design pipelines (e.g., Pixar's "character bible" approach) and is directly actionable.

3. **Anti-pattern list** is practical and testable. "Pretty but solved" and "product catalogue logic" are common failure modes that this engine explicitly addresses.

4. **Recovery beat concept** (Finding 5) is novel and production-useful. It solves the "action erases identity" problem without requiring impossible eye contact during peak movement.

---

### Issues

1. **Contradiction: Finding 1 vs. Finding 4.** Finding 1 says "role nouns replace character nouns" — but Finding 4 says "wardrobe must contain signature carry-over." If role nouns are dangerous, how does a swimsuit campaign (role: swimwear model) avoid triggering the same stereotype? The engine doesn't distinguish between *occupational roles* (athlete, businesswoman) and *situational roles* (swimsuit wearer, gym user). This needs a **role hierarchy**:
   - **High-risk roles:** career, identity, lifestyle labels (athlete, idol, tourist)
   - **Low-risk roles:** temporary, situational labels (person wearing swimsuit, person at gym)

2. **Missing: Attention decay modeling.** The engine assumes attention is binary (look/don't look). It doesn't model:
   - **First glance (0-500ms):** face detection, saliency, contrast
   - **Second glance (500ms-2s):** identity verification, social cue processing
   - **Sustained attention (2s+):** curiosity, narrative inference, emotional response
   
   Production prompts need to specify which attention phase they're targeting. Current rules collapse all phases into one.

3. **Missing: Identity decay rate.** The engine assumes identity is either preserved or lost. In practice, identity degrades gradually across frames due to:
   - **Accumulated variance:** each generation introduces small drift
   - **Contextual override:** strong environments (e.g., neon nightclub, snowy mountain) dominate visual processing
   - **Temporal inconsistency:** across a sequence, small changes compound
   
   Need a **decay threshold** — at what point does drift become noticeable? At what point does it break recognisability?

4. **Missing: Gaze direction rules.** The engine mentions "unjustified eye contact" but doesn't specify when gaze should be direct vs. averted. Research (Kampe et al., 2001; Cerf et al., 2009) shows:
   - **Direct gaze:** increases arousal, triggers social processing, but can feel confrontational
   - **Averted gaze:** reduces threat, allows environment exploration, signals disinterest
   - **Task-appropriate gaze:** looking at object being used, person being addressed, direction of movement
   
   Production needs a **gaze contract** per scene type.

5. **Missing: Environment-to-character ratio.** The engine says "environment should frame her habits" but doesn't specify the visual weight distribution. A beach scene with 80% background and 20% character will still feel environment-first regardless of habits. Need a **ratio rule**:
   - **Character-dominant scenes (70/30):** close-ups, portraits, intimate moments
   - **Balanced scenes (50/50):** street, cafe, casual activities
   - **Environment-dominant scenes (30/70):** landscapes, action, context-establishing shots
   
   The identity lock must be stronger in environment-dominant scenes.

---

### Extensions

1. **Add: Attention phase targeting.** For each scene type, specify which attention phase is primary:
   - **First glance:** high contrast, face prominence, clear silhouette
   - **Second glance:** social cues, expression nuance, object interaction
   - **Sustained attention:** narrative hooks, incomplete actions, curiosity triggers

2. **Add: Identity decay countermeasures.** For multi-frame sequences:
   - **Anchor frame:** every 3-5 frames, one frame with maximum identity lock (face + body + behaviour)
   - **Drift correction:** compare consecutive frames; if face landmarks shift >5%, regenerate
   - **Contextual buffer:** strong environments require stronger identity signals (e.g., signature accessory in foreground)

3. **Add: Gaze contract per scene type:**
   - **Social scenes (cafe, party, street):** direct gaze or gaze at another person
   - **Action scenes (sports, dance):** task-appropriate gaze (ball, target, direction)
   - **Intimate scenes (home, bedroom):** averted gaze or soft direct gaze
   - **Editorial scenes (fashion, beauty):** direct gaze with slight asymmetry (head tilt, eye contact with one eye)

4. **Add: Role hierarchy for prompt construction:**
   - **Safe roles:** person wearing [item], person at [location], person doing [action]
   - **Conditional roles:** [character] as [role] — only if role is temporary and character traits are explicitly preserved
   - **Unsafe roles:** [role] alone — never use without character prefix

5. **Add: Visual weight calculation.** For each scene, estimate:
   - Character area as % of frame
   - Background complexity (low/medium/high)
   - Number of competing objects
   - If character area <30% and background complexity is high, identity lock must be reinforced with:
     - Signature colour pop
     - Face in upper third
     - Clear silhouette separation

---

### Production Risks

1. **Testing plan is insufficient.** Comparing 20 baseline vs. 20 engine frames is too small for statistical significance. Need:
   - Minimum 100 frames per condition
   - Blind rating by 3+ evaluators
   - Metrics: recognition accuracy, time-to-recognise, preference score
   - Control for: lighting, pose variety, environment complexity

2. **Recovery beat may feel staged.** If every action scene ends with a "cute recovery," it becomes predictable. Need variety:
   - **Genuine recovery:** tired, relieved, amused
   - **Social recovery:** checking phone, talking to someone, fixing hair
   - **Environmental recovery:** looking at surroundings, adjusting equipment

3. **Styling carry-over may conflict with scene authenticity.** A signature earring in a swimsuit scene is fine; a signature earring in a boxing scene is dangerous. Need **carry-over compatibility rules:**
   - **High compatibility:** hair, makeup, skin tone, body language
   - **Medium compatibility:** jewelry, accessories, silhouette preference
   - **Low compatibility:** specific clothing items, props, footwear

4. **Over-specification risk.** The engine has 5 identity layers + 5 findings + anti-patterns + production rules. If prompts become too long, the generator may ignore key constraints. Need **priority ordering:**
   - **Tier 1 (always):** face lock, body lock
   - **Tier 2 (often):** personality lock, behaviour lock
   - **Tier 3 (when relevant):** styling carry-over, recovery beat, attention routing

---

### Consolidation Notes

1. **Merge Finding 1 and Finding 4** into a single "Role vs. Identity" rule with the role hierarchy extension.

2. **Merge Finding 2 and Finding 3** — both address environment-character balance. Finding 2 specifies *what* to preserve; Finding 3 specifies *how* to frame it. Combine into: "Identity lock must be proportional to environment dominance."

3. **Move anti-patterns into production rules.** "Pretty but solved" is a symptom, not a cause. The cause is lack of attention routing — make that explicit.

4. **Add a new section: "Attention Phase Rules"** with the three-phase model and per-phase prompt adjustments.

5. **Add a new section: "Identity Decay Management"** with anchor frames, drift correction, and contextual buffer rules.

6. **Revise testing plan:**
   - Increase sample size to 100+ per condition
   - Add blind rating protocol
   - Add attention phase metrics (first glance hold, second glance engagement, sustained attention)
   - Add decay tracking across sequences

---

**Final recommendation:** Promote to production testing with the extensions above. The core logic is sound; the gaps are in specificity and testing rigor. Block canon status until:
1. Testing confirms >80% recognition accuracy across 5+ environment types
2. Decay rate is measured and countermeasures are validated
3. Attention phase targeting shows measurable improvement in 3-second hold rate

---

# PART 11: LUCY CONSOLIDATION AFTER DEEPSEEK

## Accepted fixes

### Role-risk classification
- **High-risk role nouns:** athlete, idol, tourist, model, businesswoman, luxury girl, influencer. These can replace identity.
- **Low-risk situational descriptors:** wearing swimwear, at the gym, after tennis practice, holding a gift, walking through market. These describe context without becoming identity.

### Identity decay management
Identity is not binary; it decays by layer:
1. Face geometry drift
2. Body proportion drift
3. Styling-signature drift
4. Expression grammar drift
5. Behaviour/personality drift

Every production prompt should preserve the top three first, then add behavioural/personality preservation if token budget allows.

### Environment-to-character ratio
Recommended visual weight:
- Face + upper body / subject: 55–70% of viewer priority
- Behaviour/object anchor: 15–25%
- Environment support: 10–20%
- Background spectacle: never above subject priority

### Action-scene preservation
For high-effort action, identity returns through **pre-action setup** or **post-action recovery**, not through impossible direct camera gaze during peak motion.

### Priority order for prompt budget
1. Face identity
2. Body/proportion identity
3. Expression/personality signature
4. Behavioural habit
5. Styling carry-over
6. Environment support

---

# PART 12: FINAL BLOCKER FIXES AFTER DEEPSEEK REQUERY

## Attention phase targeting for identity preservation
- **0–500ms first glance:** preserve face geometry, hairstyle silhouette, and subject priority. Viewer must recognise the same person before reading the scene.
- **500ms–2s second glance:** preserve body proportion, posture tendency, expression grammar, and styling carry-over.
- **2s+ sustained look:** preserve behavioural identity: how she reacts, touches objects, recovers from action, and shows personality inside the environment.

## Testing methodology
- Minimum sample: 30 generated frames per high-risk environment category; 20 is acceptable only for exploratory pretest.
- Blind rating: raters compare each frame against a known identity reference without seeing the prompt.
- Metrics: face recognisability, body recognisability, personality recognisability, environment dominance, role-stereotype drift, and realism failure count.
- Pass threshold: ≥80% recognisability, ≤20% role drift, no major Character Bible conflict, no repeated face/body drift pattern.

## Production test categories
1. Sports/action high-risk role
2. Swimwear/lingerie styling high-risk body prior
3. Luxury/editorial high-risk fashion prior
4. Local lifestyle low-risk routine
5. Street/candid social scene

---

# PART 13: OPERATIONAL FIXES AFTER FINAL DEEPSEEK REQUERY

## Enforcement method by pipeline level

### Prompt-level enforcement
```text
Identity lock before scene:
[character name/reference] remains the same person: same face geometry, same eye shape, same nose-mouth relation, same body proportions, same soft teasing/local-girl expression grammar.
Scene role is temporary: she is [doing activity / wearing outfit], not becoming [role stereotype].
Preserve signature carry-over: [hair/makeup/accessory/posture habit].
```

### Reference-level enforcement
- Use the same identity reference image or approved face reference set for high-risk environments.
- If available, use identity-preserving adapters/reference guidance before relying on text alone.
- Do not change face age, ethnicity, face width, eye spacing, body proportions, or core styling baseline unless a separate Character Bible proposal approves it.

### Post-generation enforcement
- Compare generated frame against reference set using human blind rating first; automated face similarity can support but not replace human review.
- If identity drift appears in 2 consecutive frames for the same environment class, rollback that environment prompt pattern and lower role noun strength.

## Concrete rating scale
Each rater scores 1–5:
1. Not the same person
2. Weak resemblance only
3. Same face but personality/body drift
4. Recognisable same character with minor scene adaptation
5. Clearly same character and same personality in new scene

Pass criteria:
- Average face/body identity ≥4.0
- Personality identity ≥3.8
- No more than 20% frames scored 1–2
- No repeated drift pattern across 2+ frames

## Integration trigger and rollback
- Apply R020 checks to every high-risk role scene: sports, swimwear, lingerie, luxury editorial, professional role, tourist/location-heavy prompt.
- Rollback trigger: two consecutive outputs where role stereotype beats character identity.
- Correction: replace high-risk role noun with situational descriptor, increase identity lock priority, reduce environment spectacle, and move personality to recovery beat.
