**Verdict:** **PASS** (with clear scope boundaries)

**Remaining research blockers:** **None.** The micro-detail examples (1–6) are concrete, frame-specific, and technically feasible for a single-frame prompt. The scope clarification correctly identifies that post-generation validation (e.g., "is the tag corner actually hidden under the thumb?") is a production-test concern, not a research deliverable blocker.

**OK to production-test:** **YES** — *provided* the production pipeline accepts that:
- Only one micro-detail per frame is used (no stacking).
- The "not verified on generated image" items are explicitly tracked as **production validation tasks**, not research failures.
- The production test includes a human review step to confirm the chosen micro-detail is present and legible as specified.