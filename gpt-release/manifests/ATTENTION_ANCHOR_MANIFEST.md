# ATTENTION_ANCHOR_ENGINE_MANIFEST

**Manifest ID:** MANIFEST-R018-V01
**Engine:** R018 Attention Anchor Engine
**Version:** 0.1.0
**Canon status:** BLOCKED until production testing
**Last updated:** 2026-06-06

---

## 1. Purpose

Declare the release surface for the R018 research-to-engine package. This manifest tells GPT, Lucy, and downstream production tooling what the module is allowed to do and what remains blocked.

---

## 2. Artifacts

- `research/V20_RESEARCH/R018_ATTENTION_ANCHOR_ENGINE.md`
- `research/V20_RESEARCH/VERIFICATION_R018_ATTENTION_ANCHOR.md`
- `modules/V20/ENGINE_V20_ATTENTION_ANCHOR_ENGINE`
- `gpt-release/manifests/ATTENTION_ANCHOR_ENGINE_MANIFEST.md`

---

## 3. Public contract

```yaml
module: R018
name: "Attention Anchor Engine"
canon_status: "blocked_until_production_testing"
research_scope: "generic visual system; production-mappable to lil.troublr when a character prompt is present"
requires_deepseek_verification: true
requires_production_testing: true
allowed_use: "prompt experimentation, GPT review, production A/B tests"
forbidden_use: "canon promotion without test evidence"
```

---

## 4. Success metrics

- Better first-glance stop for attention/attraction modules
- Better second-glance / zoom-in for curiosity modules
- Better realism for camera-awareness/action modules
- Better recognisability for character-preservation modules
- Better repeat-viewing / save logic for attachment modules

---

## 5. Release note

This manifest is release documentation only. The engine remains blocked from canon until production testing validates the rule set.
