# R018 — Attention Anchor Engine

**Mission:** Research why some images instantly stop scrolling while others are ignored despite good image quality.

**Scope lens:** generic visual system; production-mappable to lil.troublr when a character prompt is present.

**Canon status:** BLOCKED until production testing. Research proceeds now; promotion to canon is blocked until production testing confirms improved retention, realism, recognisability, or attachment.

**Research sources considered:** Japanese gravure, Xiaohongshu, Instagram female influencers, lingerie campaigns, swimwear campaigns, editorial fashion, luxury gifting campaigns, sports/lifestyle/street photography, virtual influencer production, and visual attention research.

---

## Executive thesis

The successful image is not merely higher quality. It gives the viewer a controlled reason to keep looking after the first recognition pass. Beauty opens the door; a social, behavioural, or curiosity anchor keeps the viewer inside the frame. Production prompts must therefore specify **attention routing**, not just subject description.

---

## Findings

### Finding 1: Face + contradiction beats pure beauty

**Finding**  
Face + contradiction beats pure beauty

**Why It Works**  
A technically good image is often parsed as a solved category: pretty portrait, flower market, beach shot. The image stops scrolling only when a primary human anchor is paired with an unresolved contradiction: direct-but-not-posed gaze, luxury item in an ordinary place, private expression in public space, or an object whose purpose is not fully explained.

**Visual Trigger**  
Face-first saliency, asymmetric expression, foreground object, partially hidden narrative clue.

**Prompt Translation**  
Start prompt with one dominant human anchor, then add one unresolved clue: "her face is the sharpest and brightest anchor; one hand half-hides a small gift envelope; her eyes know the camera noticed before the scene explains why."

**Expected Production Impact**  
Raises first-glance retention and second-glance behaviour by giving the viewer a task after the beauty is registered.

**Confidence**  
High

---

### Finding 2: Anchor hierarchy beats environment storytelling

**Finding**  
Anchor hierarchy beats environment storytelling

**Why It Works**  
Environment-based storytelling fails when the background carries information but no human question. The viewer sees a nice location and leaves. Human anchors outperform because faces, eyes, and hands are processed faster than scenery and create social meaning.

**Visual Trigger**  
Eyes > mouth > hands > personal object > text/brand detail > environment.

**Prompt Translation**  
Use hierarchy language: "primary anchor: eyes; secondary anchor: mouth in suppressed smile; tertiary anchor: hand holding object; background only supports context."

**Expected Production Impact**  
Reduces flower-market failure mode where the environment is pretty but not behaviourally sticky.

**Confidence**  
High

---

### Finding 3: Curiosity requires one incomplete pattern, not many

**Finding**  
Curiosity requires one incomplete pattern, not many

**Why It Works**  
Curiosity appears when the frame withholds exactly one important answer. Too many unresolved details become clutter; no unresolved detail becomes decorative.

**Visual Trigger**  
A cropped hand, half-visible message, opened box, strap being adjusted, one chair empty, gift tag turned away.

**Prompt Translation**  
Add: "one incomplete pattern only: the card is visible but not readable; everything else is coherent."

**Expected Production Impact**  
Improves zoom-in and dwell time because the viewer searches for the withheld answer.

**Confidence**  
High

---

### Finding 4: Zoom-in behaviour is created by legible micro-information

**Finding**  
Zoom-in behaviour is created by legible micro-information

**Why It Works**  
Zoom-in happens when the viewer believes there is more information to decode. Tiny marks must be specific enough to reward inspection but not so dominant that they steal the first glance.

**Visual Trigger**  
Small text, charm, stitching, product tag, handwriting, reflected face, second cup, lipstick mark.

**Prompt Translation**  
Prompt micro-details as "legible at close inspection, secondary to face, not centered, not brighter than eyes."

**Expected Production Impact**  
Increases saves and re-views because the image contains a second layer after the feed preview.

**Confidence**  
Medium-High

---

### Finding 5: Anchor conflict kills retention

**Finding**  
Anchor conflict kills retention

**Why It Works**  
If face, body, background, product, and lighting all compete equally, the viewer has no route through the frame. The image feels busy, not deep.

**Visual Trigger**  
Equal sharpness, equal brightness, all-over HDR, saturated flowers, multiple readable signs.

**Prompt Translation**  
Add negative contract: "no all-over sharpness, no background brighter than face, no competing large text, no second face as bright as subject."

**Expected Production Impact**  
Improves production stability by turning attention into a path, not a pile of details.

**Confidence**  
High


---

## Anchor hierarchy

1. **Living face anchor** — eyes, catchlight, periorbital engagement, mouth-state.
2. **Behaviour anchor** — hand doing something, body mid-transition, object interaction.
3. **Curiosity anchor** — one clue that is visible but unresolved.
4. **Identity anchor** — personal detail that belongs to her rather than the set.
5. **Environment anchor** — location detail that frames the action but never competes.

Environment-only concepts, including flower-market frames, fail when they skip levels 1–3 and rely on colour/beauty alone.

## Production rules

- The face is the first anchor unless the image is explicitly faceless/editorial.
- Every frame needs one and only one curiosity anchor.
- Use three focal planes: foreground behaviour, face/subject, background context.
- Background saliency must be lower than face saliency.
- Micro-detail must reward zoom-in but remain secondary in feed view.


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

---

# PART 11: LUCY CONSOLIDATION AFTER DEEPSEEK

## Accepted fixes

### Temporal attention layer
- **0–200ms:** face saliency, contrast, clean silhouette, and one human contradiction create the stop.
- **200ms–1s:** viewer resolves whether the contradiction is socially meaningful.
- **1–3s:** hand/object/detail route creates the second glance.
- **3s+:** micro-information and return-to-face trigger create zoom-in and re-look.

### Resolvable social contradiction definition
A valid attention contradiction must be:
1. **Resolvable** — the viewer believes an answer exists inside or just outside the frame.
2. **Social/behavioural** — the question concerns intent, reaction, relation, gift, message, or interruption.
3. **Physically plausible** — no surreal object logic, impossible pose, or fantasy mismatch.
4. **Subordinate to the face** — contradiction extends attention; it does not replace the subject.

### Anchor hierarchy revision
Final hierarchy for R018:
1. Living face anchor
2. Behaviour anchor
3. Curiosity anchor
4. Micro-information anchor
5. Environment support anchor

Identity anchor is moved out of R018's core hierarchy and treated as an optional cross-reference to R020.

### Finding 4 clarification
Micro-information creates zoom-in only when it is **legible but secondary**: sharp enough to reward inspection, not bright/central enough to become the first anchor.

---

# PART 12: FINAL BLOCKER FIXES AFTER DEEPSEEK REQUERY

## Gaze direction rules
- **Camera gaze:** allowed when the face is the primary social anchor; must be paired with a response-state mouth, not dead stare.
- **Object gaze:** allowed when the curiosity anchor is being used, opened, adjusted, gifted, or hidden; the object must be visible and functional.
- **Off-frame gaze:** allowed only when a visible reason exists: second cup, message, shadow, hand entering frame, friend trace, or sound reaction.
- **Gaze-hand coordination:** if eyes attend to object, hands must be functionally related to that object; if eyes attend camera, hands may continue the previous action.

## Face quality prerequisites
- Micro-expression must be legible: suppressed smile, neutral-plus mouth, returned gaze, or slight surprise.
- Eyes need catchlight and periorbital engagement; no blank mannequin gaze.
- Skin texture should remain photographic and familiar, not plastic or over-smoothed.

## Production-specific constraints
- Character prompts: place identity before scene and anchor; generic prompts: place subject category before anchor.
- Style compatibility: photo-real prompts use lens/light/focus rules; anime/painterly prompts translate anchors into composition, expression, prop, and negative-space rules.
- Minimum output: face must remain readable at feed size; micro-detail must remain readable only at zoom size.
- Failure modes: surreal clues, floating objects, unreadable text, duplicate hands, and over-bright props invalidate the anchor.

## Lighting and composition hierarchy
- Face luminance target: visibly brighter than background, approximately 1.5–2x perceived priority.
- Curiosity anchor brightness: below face brightness; never the brightest object.
- Placement: face in upper third; behaviour/object anchor lower or side third; curiosity clue off-centre; environment recedes.
- Negative space: keep at least 25–35% low-information area so the anchor path can breathe.

## Behavioural consistency
Every object anchor requires owner, purpose, last interaction, and current physical state. Hands must touch, hold, open, adjust, hide, or release objects with believable physics.

---

# PART 13: OPERATIONAL FIXES AFTER FINAL DEEPSEEK REQUERY

## Owner/Purpose/Interaction/State prompt template
Use this exact pattern when an object becomes an attention anchor:

```text
Attention anchor object: [object].
Owner: [her / off-frame friend / gift sender].
Purpose: [why the object is here now].
Last interaction: [what just happened to it].
Current state: [where it rests, how it is held, what is open/closed/creased/wet/used].
Visibility reason: [why the viewer can see it without it being staged].
Anchor priority: secondary to face, readable on second glance, not centered, not brightest.
```

## Failure-mode correction rules
- If object floats / has no contact: regenerate with "object physically supported by hand/table/fabric; contact shadow visible".
- If text is unreadable but meant to be decoded: replace with fewer larger characters or remove the text goal.
- If curiosity anchor becomes brightest: lower its brightness and move it off-centre.
- If duplicate hands appear: reduce hand-object complexity to one visible active hand.
- If surreal clue appears: replace contradiction with social contradiction: message, gift, off-frame hand, second cup, interrupted action.

## Micro-detail construction rule
Micro-detail must be specified as:
1. **Feed-invisible but zoom-rewarding** — not required for first-glance comprehension.
2. **Physically placed** — on tag, card, phone screen, receipt, charm, stitching, mirror reflection.
3. **Optional to parse** — image still works if unreadable at feed size.
4. **Secondary priority** — never brighter, larger, or sharper than the eyes.

## Post-generation validation checklist
- Face is sharpest and brightest anchor.
- One object anchor has owner/purpose/last interaction/current state.
- One curiosity clue only.
- Curiosity clue has physical support/contact.
- Micro-detail rewards zoom but is not needed to understand the image.
- Background does not contain a brighter competing sign/object/face.

---

# PART 14: R018 CONCRETE MICRO-DETAIL EXAMPLES + SCOPE CLARIFICATION

## Concrete micro-detail examples

Use one per frame only:

1. **Gift tag clue:** small cream tag tied to a ribbon; readable fragment: "for later"; tag corner partially hidden under her thumb.
2. **Phone-screen clue:** lock-screen notification preview from an unnamed friend; only first 3–5 words visible; phone lies face-up beside her hand.
3. **Receipt clue:** café receipt with circled item and time visible; receipt is creased and partly under a cup.
4. **Jewelry/charm clue:** tiny initial charm on bracelet; visible only where wrist catches light; not centered.
5. **Mirror/reflection clue:** blurred second cup or hand reflected in compact mirror; reflection supports off-frame presence.
6. **Fabric/stitching clue:** lingerie/swimwear tag, embroidered initial, or stitching detail visible near strap/edge; only readable on zoom.

## Production-test scope clarification
No generated image is expected inside the research deliverable. The post-generation checklist is a future validation protocol for production testing. Therefore any "not verified on generated image" item remains **UNCLEAR / blocked until production testing**, not a research blocker.
