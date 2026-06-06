# R020 — Character Preservation Engine Verification Protocol

**Canon status:** BLOCKED until production testing.

**Purpose:** Define how to test whether R020 improves production output before any finding is promoted into canon.

---

## 0. Required metrics

- First-glance stop probability
- 3-second dwell/hold proxy
- Second-glance behaviour
- Zoom-in / close inspection likelihood
- Realism failure count
- Character preservation score where applicable
- Prompt bloat / overconstraint score

---

## 1. Per-finding verification

### R020-01 — Activities overpower identity when role nouns replace character nouns
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 1.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R020-02 — Identity lock needs face, body, and behaviour simultaneously
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 2.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R020-03 — Environment should frame her habits, not overwrite them
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 3.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R020-04 — Wardrobe and styling must contain a signature carry-over
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 4.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R020-05 — Action scenes need personality residue after the action
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 5.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

---

## 2. Production hold rule

This module remains **blocked until production testing**. A rule can be promoted only when it improves the target metric without creating a stronger failure in realism, identity preservation, or prompt controllability.

---

## 3. DeepSeek verification status

Pending DeepSeek V4 Pro verify + extend pass. Lucy will append consolidation notes after DeepSeek feedback is evaluated.

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
