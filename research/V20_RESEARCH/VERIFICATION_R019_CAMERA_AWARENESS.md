# R019 — Camera Awareness Engine Verification Protocol

**Canon status:** BLOCKED until production testing.

**Purpose:** Define how to test whether R019 improves production output before any finding is promoted into canon.

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

### R019-01 — Direct eye contact improves retention when the scene can plausibly pause
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 1.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R019-02 — No eye contact is required during high-effort action
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 2.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R019-03 — Accidental awareness is the bridge between realism and retention
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 3.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R019-04 — Indirect eye contact works when intimacy would be too strong
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 4.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R019-05 — Intentional camera awareness needs a reason
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

## Verification & Extension Report — R019 Camera Awareness Engine

---

### Verdict

**PARTIALLY VALID — BLOCKED STATUS CORRECT.** The research is structurally sound and the core thesis is strong. However, it contains significant gaps in visual logic, production applicability, and internal contradictions that must be resolved before promotion to canon. The executive thesis is excellent; the execution of findings is incomplete.

---

### Strengths

1. **Executive thesis is production-grade.** "Attention routing, not subject description" is a clear, actionable principle that directly addresses the "pretty but solved" anti-pattern.
2. **Matrix is useful as a quick reference.** Scene type → eye contact mode → reason is the right structure for production prompts.
3. **Anti-patterns are well-identified.** "Unjustified eye contact" and "product catalogue logic" are real failure modes that this engine can prevent.
4. **Production testing plan is correct in structure.** A/B comparison with clear metrics is the right approach.
5. **Accidental awareness (Finding 3) is the strongest finding.** It bridges realism and retention correctly and is the most likely to survive production testing.

---

### Issues

#### 1. Contradiction: Finding 1 vs. Finding 5

- Finding 1 says direct eye contact works "when the scene can plausibly pause."
- Finding 5 says intentional camera awareness "needs a reason" and without reason "it becomes modelling."
- **Problem:** Finding 1's "plausible pause" is not a reason; it's a condition. A pause alone does not justify camera awareness. The viewer will still ask "why is she looking at me?" unless the scene provides a diegetic camera.
- **Fix:** Merge Finding 1 into Finding 5. Direct eye contact is always intentional; the only question is whether the intention is justified by the scene. Remove Finding 1 as a standalone finding.

#### 2. Missing: The "No Camera" Mode

- The research assumes a camera is always present in the scene. It does not address scenes where the camera is **hidden** or **observational** (e.g., paparazzi, security cam, documentary, hidden lens).
- **Gap:** What happens when the character should *not* know the camera exists? This is a distinct mode from "no eye contact during action." A character at rest can still ignore the camera if she doesn't know it's there.
- **Fix:** Add Finding 6: "No camera awareness is required when the camera is not part of the scene's reality." Visual trigger: character absorbed in private moment, no acknowledgment of observer. Prompt translation: "camera is hidden; she is unaware of being watched."

#### 3. Missing: The "Broken Fourth Wall" Mode

- The research treats camera awareness as a binary (aware vs. unaware) with a hybrid (accidental). It does not address **deliberate fourth-wall breaking** (e.g., wink, smirk, direct address to viewer).
- **Gap:** This is common in lingerie, swimwear, and luxury gifting campaigns. It is not "modelling" if the genre permits it.
- **Fix:** Add Finding 7: "Deliberate fourth-wall break is allowed when the genre or character persona permits direct viewer address." Visual trigger: smirk, wink, eyebrow raise, direct stare with no diegetic camera. Prompt translation: "she knows the viewer is watching and acknowledges it directly."

#### 4. Weak: Finding 4 (Indirect eye contact)

- "Looking near the camera, at the photographer, into a mirror, or at an off-frame friend" are four different behaviours with different visual outcomes. They are lumped together.
- **Problem:** "At the photographer" implies a diegetic photographer exists. "Into a mirror" implies a mirror. "Off-frame friend" implies a social scene. These are not interchangeable.
- **Fix:** Split Finding 4 into three sub-findings:
    - 4a: Gaze to diegetic photographer (camera is held by someone she knows).
    - 4b: Mirror gaze (camera is not the target; her own reflection is).
    - 4c: Off-frame social gaze (she is looking at someone the viewer cannot see).

#### 5. Missing: Temporal Dynamics

- The research treats each frame as static. It does not address **sequence logic** (e.g., she looks away, then back; she notices the camera, then ignores it).
- **Gap:** In video or multi-frame production, camera awareness must be consistent across frames. A character cannot be accidentally aware in frame 1 and intentionally aware in frame 2 without a narrative reason.
- **Fix:** Add a note: "For multi-frame sequences, camera awareness mode must remain consistent unless a narrative beat (e.g., she notices the camera mid-action) justifies the change."

#### 6. Weak: Production Rules are Too Vague

- "If the body can plausibly pause, direct awareness is allowed." This is not a rule; it's a guideline. What counts as a "plausible pause"? A runner at a traffic light? A dancer holding a pose? A model mid-stride?
- **Fix:** Replace with: "Direct awareness is allowed only when the character's primary action (task, movement, interaction) can be interrupted without breaking realism. If the action requires continuous attention, awareness is forbidden."

#### 7. Missing: Character-Specific Logic

- The scope lens says "apply to lil.troublr only when the scene asks for character-specific behaviour." But the research does not define what character-specific behaviour means for lil.troublr.
- **Gap:** What is lil.troublr's default camera awareness mode? Is she shy? Confident? Playful? Aloof? The research must specify a baseline for her.
- **Fix:** Add a character note: "lil.troublr's default mode is accidental awareness (Finding 3). She is aware of the camera but does not perform for it. Direct intentional gaze is reserved for selfie/mirror scenes or moments of deliberate confidence."

---

### Extensions

#### Extension 1: Attention Routing Hierarchy

The executive thesis mentions "attention routing" but does not define it. Propose:

1. **First glance:** Face/eyes (automatic, hardwired).
2. **Second glance:** Object/action she is interacting with (curiosity anchor).
3. **Third glance:** Environment/context (scene comprehension).
4. **Fourth glance:** Return to face/eyes (re-evaluation, emotional read).

**Production rule:** The prompt must ensure that the second glance (object/action) is not blocked by the first glance (face). If the face is too dominant (e.g., extreme close-up, high contrast, direct stare), the viewer never reaches the curiosity anchor.

#### Extension 2: The "Gaze Arc" Concept

For single-frame images, the viewer's eye path is determined by gaze direction. If the character looks left, the viewer looks left. If she looks at the camera, the viewer stays on her face.

**Production rule:** Use gaze direction to control viewer attention flow. If the curiosity anchor is to her right, she should be looking right or at the object, not at the camera.

#### Extension 3: Cultural Variation Note

The research sources include Japanese gravure, Xiaohongshu, and Korean editorial. These have different norms for camera awareness:

- **Japanese gravure:** Direct eye contact is standard; it is a performance of availability.
- **Korean editorial:** Indirect or averted gaze is common; direct gaze is reserved for high-fashion or confrontational concepts.
- **Western influencer:** Direct gaze is default; accidental gaze is a stylistic choice.

**Production rule:** When generating for a specific cultural market, override the default matrix with market-specific norms.

---

### Production Risks

| Risk | Severity | Mitigation |
|---|---|---|
| **Unjustified direct gaze** (Finding 1 without Finding 5) | High | Merge findings; require diegetic camera or genre permission |
| **Accidental awareness misinterpreted as "caught off guard"** | Medium | Clarify: accidental awareness is a brief, non-performative look, not a startled reaction |
| **Indirect gaze confusion** (Finding 4 lumped) | Medium | Split into sub-findings; specify which one in prompt |
| **No camera mode ignored** | High | Add Finding 6; test against paparazzi/hidden-camera scenes |
| **Character baseline missing** | High | Add lil.troublr default mode; test against her existing canon |
| **Temporal inconsistency in sequences** | Medium | Add sequence logic note; test with 2+ frame prompts |

---

### Consolidation Notes

1. **Merge Finding 1 into Finding 5.** Direct eye contact is always intentional; remove "plausible pause" as a standalone justification.
2. **Split Finding 4 into three sub-findings** (diegetic photographer, mirror gaze, off-frame social gaze).
3. **Add Finding 6 (no camera mode)** and **Finding 7 (deliberate fourth-wall break)**.
4. **Add character baseline for lil.troublr:** default = accidental awareness; direct gaze = selfie/mirror/confidence moment.
5. **Replace vague production rules** with the corrected versions above.
6. **Add attention routing hierarchy** and **gaze arc concept** as production tools.
7. **Add cultural variation note** for market-specific override.
8. **Keep anti-patterns** as-is; they are correct and useful.
9. **Keep production testing plan** as-is; it is correct.
10. **Promotion to canon remains BLOCKED** until production testing confirms at least 3 of the 5 metrics improve (first-glance stop, 3-second hold, zoom-in rate, re-look rate, realism failure count).
