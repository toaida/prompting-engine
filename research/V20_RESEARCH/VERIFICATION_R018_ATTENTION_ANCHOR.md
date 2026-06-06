# R018 — Attention Anchor Engine Verification Protocol

**Canon status:** BLOCKED until production testing.

**Purpose:** Define how to test whether R018 improves production output before any finding is promoted into canon.

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

### R018-01 — Face + contradiction beats pure beauty
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 1.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R018-02 — Anchor hierarchy beats environment storytelling
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 2.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R018-03 — Curiosity requires one incomplete pattern, not many
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 3.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R018-04 — Zoom-in behaviour is created by legible micro-information
- **Compliance evidence:** image shows the described trigger without competing anchors.
- **Red flags:** trigger absent, too staged, or overwhelmed by background/role stereotype.
- **Test prompt:** apply the Prompt Translation from Finding 4.
- **Pass threshold:** 80% of 20 test frames show the rule without realism loss.

### R018-05 — Anchor conflict kills retention
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

# Verification & Extension Report — R018 Attention Anchor Engine

## Verdict
**PASS WITH EXTENSIONS REQUIRED.** The core thesis is sound and production-relevant. However, the research has significant gaps in visual logic, production specificity, and consolidation that must be addressed before canon promotion.

---

## Strengths
- **Clear hierarchy model** (face > behaviour > curiosity > identity > environment) is well-supported by attention research and practical observation.
- **Anti-patterns** are concrete and actionable; "pretty but solved" is a useful diagnostic.
- **Curiosity anchor constraint** (one incomplete pattern only) is a strong, testable rule.
- **Production testing plan** is minimal but correct in structure.
- **Anchor conflict** finding correctly identifies a common failure mode in generated imagery.

---

## Issues

### 1. Missing Temporal Logic
The research treats attention as static. In feed-scrolling, the first 200ms determine stop-or-skip. The hierarchy must be expressed as a **temporal sequence**:
- **0–200ms:** Face saliency + contradiction trigger (stop)
- **200–800ms:** Curiosity anchor resolves partially (hold)
- **800ms–3s:** Micro-detail reward (zoom/dwell)
- **3s+:** Identity/environment integration (re-look/save)

**Action:** Add temporal layer to all findings. "Face + contradiction" is a first-glance trigger; "curiosity anchor" is a second-glance mechanism.

### 2. Contradiction Definition is Vague
"Direct-but-not-posed gaze" and "luxury item in ordinary place" are examples, not definitions. What makes a contradiction *effective* vs. *confusing*?

**Missing criteria:**
- Contradiction must be **resolvable** (viewer believes answer exists)
- Contradiction must be **social** (implies human behaviour, not abstract incongruity)
- Contradiction must **not violate physics** (fantasy contradictions break realism)

**Action:** Define "resolvable social contradiction" as the only valid type for this engine.

### 3. No Gaze Direction Logic
The research mentions "direct-but-not-posed gaze" but doesn't specify:
- **Gaze direction relative to frame:** Looking at camera vs. looking at object vs. looking off-frame
- **Gaze + hand coordination:** Where eyes go, hands follow; mismatch breaks realism
- **Gaze as curiosity anchor:** Looking at something off-frame creates stronger curiosity than looking at visible object

**Action:** Add gaze direction rules: (a) gaze at camera = engagement anchor, (b) gaze at object = behaviour anchor, (c) gaze off-frame = strongest curiosity anchor but requires visible reason.

### 4. Missing "Why This Face" Logic
The research assumes any face works. Production data shows:
- **Familiar faces** (IP-adapted characters) have higher retention than novel faces
- **Faces with micro-expressions** (suppressed smile, half-blink, lip-bite) outperform neutral expressions
- **Faces with visible skin texture** (not smooth) increase realism and trust

**Action:** Add "face quality" as a prerequisite anchor condition, not just presence.

### 5. No Production-Specific Constraints
The research is generic but claims production-mappability to lil.troublr. Missing:
- **Character prompt integration:** How does anchor hierarchy interact with character identity?
- **Style constraints:** Does this work in anime? Painterly? Photorealistic?
- **Resolution limits:** Micro-detail is useless at 512x512; requires minimum 1024x1024
- **Generation failure modes:** What happens when the model can't produce the anchor hierarchy?

**Action:** Add production-specific section with resolution, style, and character constraints.

### 6. Contradiction with Finding 4
Finding 4 says "zoom-in behaviour is created by legible micro-information" but Finding 3 says "one incomplete pattern only." These are not contradictory per se, but the research doesn't explain:
- Micro-detail can be *complete* (e.g., visible stitching) and still reward zoom-in
- Curiosity anchor must be *incomplete* (e.g., half-hidden text)
- Both can coexist if the incomplete pattern is the *primary* curiosity driver and micro-detail is *secondary* reward

**Action:** Clarify that micro-detail and curiosity anchor serve different temporal functions and can coexist if hierarchy is maintained.

---

## Extensions

### Extension 1: Add "Behavioural Consistency" Rule
**Observation:** Generated images often show hands in anatomically impossible positions or objects held without functional purpose. This breaks the behaviour anchor.

**Rule:** Every hand-object interaction must have a clear physical purpose (holding, adjusting, gifting, hiding, writing, etc.). "Hand resting on surface" is not a behaviour anchor.

### Extension 2: Add "Lighting Hierarchy" Rule
**Observation:** Attention follows brightness. If background is brighter than face, the viewer's eye goes to background first, then has to re-find the face.

**Rule:** Face luminance must be 1.5–2x background luminance. Curiosity anchor can be slightly brighter than face only if it's small (<5% of frame).

### Extension 3: Add "Frame Composition" Rules
**Observation:** The research doesn't specify where anchors should be placed in the frame.

**Rules:**
- Face in upper-left or upper-center (Western reading pattern)
- Curiosity anchor in lower-right (natural scanpath end)
- Behaviour anchor in mid-frame, aligned with gaze direction
- Micro-detail in lower-left or near hand

### Extension 4: Add "Negative Space" Requirement
**Observation:** Cluttered frames fail even with correct hierarchy. The viewer needs visual breathing room.

**Rule:** At least 30% of frame must be negative space (plain background, out-of-focus area, or empty surface). This increases anchor saliency.

### Extension 5: Add "Temporal Unfolding" Prompt Structure
**Current prompt translation is flat.** Replace with temporal structure:

```
[First glance trigger] Her face is the sharpest and brightest anchor; direct gaze with suppressed smile.
[Second glance hook] One hand half-hides a small gift envelope; the card is visible but not readable.
[Zoom reward] The envelope has a wax seal with a partial monogram; her nail polish is slightly chipped.
[Context] Background is a minimalist cafe; nothing competes with face or hand.
```

---

## Production Risks

| Risk | Severity | Mitigation |
|------|----------|------------|
| Model cannot produce specified anchor hierarchy | High | Use ControlNet depth/pose + IP-Adapter face; test with simple scenes first |
| Curiosity anchor becomes main anchor (steals from face) | Medium | Enforce face saliency via brightness/contrast/sharpness rules |
| Micro-detail is not legible at generation resolution | High | Minimum 1024x1024; avoid text smaller than 8px at output resolution |
| Behaviour anchor looks unnatural (hand/object physics) | High | Use reference poses; avoid complex hand-object interactions in first tests |
| Contradiction is not resolvable (viewer gives up) | Medium | Test contradictions with human raters; remove any that don't produce "aha" response |
| Style mismatch (anchor hierarchy works in photo but not illustration) | Medium | Test separately for photorealistic vs. stylized; may need different rules |

---

## Consolidation Notes

### What to Keep
- **Anchor hierarchy** (face > behaviour > curiosity > identity > environment) — core model
- **One curiosity anchor only** — critical constraint
- **Anchor conflict kills retention** — important negative rule
- **Anti-patterns** — useful diagnostics

### What to Add
- **Temporal sequence** (0–200ms, 200–800ms, 800ms–3s, 3s+)
- **Gaze direction rules** (camera/object/off-frame)
- **Behavioural consistency** (hand-object physics)
- **Lighting hierarchy** (face 1.5–2x background)
- **Frame composition** (face upper-left, curiosity lower-right)
- **Negative space** (30% minimum)
- **Face quality prerequisites** (micro-expression, skin texture)

### What to Merge
- **Finding 1 + Finding 2** → "Face + hierarchy + contradiction" as unified first-glance rule
- **Finding 3 + Finding 4** → "Curiosity anchor for hold, micro-detail for zoom" as temporal pair
- **Finding 5** → Standalone as "anchor conflict" anti-pattern

### What to Remove or Downgrade
- **"Environment anchor"** as level 5 — it's not an anchor; it's context. Rename to "environmental context."
- **"Identity anchor"** as level 4 — this is a character consistency issue, not an attention anchor. Move to character prompt rules.

### Revised Hierarchy (Consolidated)
1. **Face anchor** (saliency, expression, gaze direction, skin quality)
2. **Behaviour anchor** (hand-object interaction, body mid-transition, functional purpose)
3. **Curiosity anchor** (one resolvable social contradiction, incomplete pattern)
4. **Micro-detail reward** (legible at zoom, secondary to face, not curiosity)
5. **Environmental context** (supports action, lower saliency than face)

---

## Final Recommendation

**Promote to canon only after:**
1. Temporal sequence is added to all findings
2. Gaze direction rules are specified
3. Production constraints (resolution, style, character) are documented
4. Lighting and composition rules are added
5. Testing plan includes temporal metrics (not just aggregate retention)

**Current status:** BLOCKED (correct) — but research should continue with these extensions before production testing begins.
