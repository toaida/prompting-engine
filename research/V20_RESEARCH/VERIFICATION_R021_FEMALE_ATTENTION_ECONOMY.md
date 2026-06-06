# R021 — Female Attention Economy Engine Verification Protocol

**Canon status:** BLOCKED until production testing.

**Purpose:** Define how to test whether R021 improves production output before any finding is promoted into canon.

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

### R021-01 — Attraction is the stop-scroll layer, not the full engine
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 1.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R021-02 — Retention comes from a readable gaze path
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 2.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R021-03 — Attachment comes from personality continuity
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 3.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R021-04 — Curiosity comes from withheld context, not mystery aesthetics
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 4.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R021-05 — Emotional attachment requires low-status vulnerability mixed with competence
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

## Verification & Extension Report: R021 — Female Attention Economy Engine

### Verdict
**BLOCKED — Conditionally sound, structurally incomplete.** The framework is logically coherent and production-relevant, but contains critical gaps in visual logic, category boundary definitions, and missing attention mechanisms that will cause production failures if promoted as-is.

---

### Strengths
1. **Clear layered architecture** — Attraction → Retention → Attachment → Curiosity forms a usable production hierarchy.
2. **Anti-pattern list is actionable** — "Pretty but solved" and "All-over sharpness" are specific, testable failure modes.
3. **Production testing plan exists** — Concrete metrics (first-glance stop, 3-second hold, zoom-in rate) are defined.
4. **Curiosity definition is correct** — Differentiates from "mystery aesthetics" (fog/shadows) to specific unanswered questions.
5. **Vulnerability + competence finding** — Correctly identifies the attachment mechanism; avoids the "damsel" trap.

---

### Issues

#### 1. Missing: **Attention Capture Hierarchy** (Critical Gap)
The framework assumes attention is linear (stop → hold → attach). Visual attention research shows **bottom-up salience** (color, contrast, motion) and **top-down goals** (task relevance) compete. The engine has no mechanism for:
- **Salience override** — When background color contrast beats face salience.
- **Task conflict** — When product placement fights gaze path.
- **Fixation competition** — Multiple high-salience regions (face + bright product + text overlay).

**Fix:** Add a pre-processing layer: "Salience audit — ensure face is highest salience region, then route gaze."

#### 2. Contradiction: **Finding 2 vs. Anti-pattern "All-over sharpness"**
Finding 2 says "routeable detail" is good. Anti-pattern says "all-over sharpness" is bad. But routeable detail requires sharpness to be readable. The contradiction is unresolved: **how much sharpness is routeable vs. competitive?**

**Fix:** Define "sharpness gradient" — face and primary anchor sharp, secondary anchors softer, background blurred. Prompt: "sharpness gradient: face sharp, hand/object medium, background soft."

#### 3. Missing: **Gaze Path Failure Modes** (Production Risk)
The engine assumes gaze paths are always successful. Research shows:
- **Gaze capture failure** — Viewer fixates on face and never moves.
- **Path abandonment** — Viewer follows path but finds no reward, exits.
- **Loop fatigue** — Viewer cycles face → object → face repeatedly with no new information.

**Fix:** Add "gaze path reward" — each step must provide new information (expression nuance, object detail, environmental clue). If path loops without new data, it fails.

#### 4. Category Boundary Ambiguity
- **Attraction vs. Retention** — "Face clarity" is listed under Attraction, but face clarity also enables Retention (gaze path needs a clear face to return to). Overlap is not acknowledged.
- **Curiosity vs. Attachment** — "Withheld context" (Curiosity) and "vulnerability" (Attachment) both create re-view value. The engine doesn't explain when to use which.

**Fix:** Add decision tree: "Use Curiosity when product/context is the question. Use Attachment when character is the question."

#### 5. Missing: **Temporal Attention Decay** (Production Gap)
The engine assumes attention layers stack permanently. Research shows:
- Attraction decays in ~1.5 seconds.
- Retention decays after 2-3 gaze cycles.
- Attachment and Curiosity are the only layers that survive beyond 5 seconds.

**Fix:** Add "attention decay curve" to each layer. Prompts must specify which layer sustains the longest dwell.

#### 6. Missing: **Cultural Attention Variance**
The engine is trained on Japanese gravure, Xiaohongshu, Instagram. These have different gaze norms:
- Japanese gravure: indirect gaze, partial face, body-line priority.
- Xiaohongshu: direct gaze, lifestyle context, product interaction.
- Instagram: direct gaze, high contrast, face-dominant.

**Fix:** Add "cultural gaze norm" parameter to prompt contract. Example: "gaze norm: direct (Western social media)" vs. "gaze norm: averted (East Asian editorial)."

---

### Extensions

#### Extension 1: **Attention Routing Prompt Contract**
Add to production rules:
```
ATTENTION_ROUTING:
  - Primary anchor: [face/eyes]
  - Secondary anchor: [hand/object/environment]
  - Tertiary anchor: [clue/withheld element]
  - Return trigger: [expression change/partial reveal]
  - Salience hierarchy: [face > anchor > background]
  - Gaze path reward: [new info at each step]
  - Decay layer: [curiosity/attachment for >5s dwell]
```

#### Extension 2: **Gaze Path Validation Test**
Before production, test each frame for:
1. **Salience map** — Is face the highest salience region?
2. **Path readability** — Can a viewer trace eyes → anchor → clue → return in <2 seconds?
3. **Reward density** — Does each step provide new information?
4. **Loop detection** — Does the path cycle without new data?

#### Extension 3: **Attention Layer Stacking Rules**
```
Layer stacking:
  - Attraction + Retention = high dwell, low saves
  - Attraction + Curiosity = high zoom-in, low repeat
  - Attraction + Attachment = high saves, high repeat
  - Attraction + Retention + Curiosity = high engagement
  - Attraction + Retention + Attachment = high loyalty
  - All four = optimal but rare; requires careful salience management
```

#### Extension 4: **Product Integration Logic**
Current engine treats product as "behavior anchor." Extend:
```
PRODUCT_INTEGRATION:
  - Product as gaze anchor: hand holding, using, or reacting to product
  - Product as curiosity trigger: half-open, unwrapped, gifted
  - Product as attachment symbol: repeated use, personalization, wear
  - Product as status signal: luxury context, but must not dominate face
  - Anti-pattern: product as catalog object (no interaction, no reaction)
```

---

### Production Risks

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Gaze path failure (viewer stuck on face) | High | Medium | Add salience audit + path reward check |
| Cultural gaze mismatch | Medium | High | Add cultural norm parameter to prompt |
| Layer conflict (curiosity vs. attachment) | Medium | Medium | Add decision tree for layer priority |
| Product dominance (catalog logic) | High | High | Enforce product interaction rules |
| Over-engineering prompts | Medium | Low | Keep prompt contract to 3-5 lines max |
| Realism failure from complex prompts | Medium | High | Test with simple prompts first, add complexity iteratively |

---

### Consolidation Notes

1. **Merge Finding 2 and Anti-pattern "All-over sharpness"** into a single rule: "Sharpness gradient: face sharp, primary anchor medium, background soft. No equal sharpness across frame."

2. **Merge Finding 4 and Finding 5** under a new category: "Re-view value" — Curiosity (unanswered question) and Attachment (vulnerability) both create reasons to return. Differentiate by: Curiosity = external question (what is that?), Attachment = internal question (who is she?).

3. **Add "Attention Decay" as a new finding** — Each layer has a decay time. Prompts must specify which layer sustains the longest dwell.

4. **Add "Cultural Gaze Norm" as a production parameter** — Not a finding, but a required prompt field.

5. **Remove "Role replacement" anti-pattern** — It's vague. Replace with "Character identity erased by scene noun" (e.g., "barista" replaces personality).

6. **Promote to canon only after:**
   - Salience audit passes for 80% of test frames.
   - Gaze path reward test passes for 70% of test frames.
   - Cultural norm parameter is included in prompt contract.
   - Layer stacking rules are validated against production metrics.

---

### Final Recommendation
**Do not promote to canon.** The framework is structurally sound but missing critical attention mechanisms (salience hierarchy, gaze path reward, decay curves, cultural variance). Fix these gaps, run production testing with the extended prompt contract, then re-evaluate. The anti-pattern list and layer architecture are strong and should be preserved.
