# LIL_TROUBLR V20 MASTER DRAFT
## Runtime-Ready Integration Layer for Attention, Camera Relationship, Body Language, Objects, Night, and HK Locality

---

## Executive Summary

V20 adds a runtime decision layer on top of V14-V19. It does not replace older engines. It decides **which existing and new systems should activate in a given image** so that prompt generation feels socially photographed, locally Hong Kong, physically plausible, and attention-aware.

V20 includes six active modules:

1. `ENGINE_V20_ATTENTION_ROUTING_SYSTEM`
2. `ENGINE_V20_CAMERA_RELATIONSHIP_SYSTEM`
3. `ENGINE_V20_BODY_LANGUAGE_ATTRACTION_SYSTEM`
4. `ENGINE_V20_OBJECT_LOGIC_V2_SYSTEM`
5. `ENGINE_V20_NIGHT_REALISM_SYSTEM`
6. `ENGINE_V20_HONG_KONG_LOCAL_GIRL_SYSTEM`

---

## V20 Runtime Stack

Use this stack after character identity and safety rules, before final prompt rendering:

```
PHOTO EXISTENCE REASON
→ CAMERA RELATIONSHIP
→ ATTENTION ROUTING PATH
→ HK LOCALITY / ENVIRONMENT
→ BODY LANGUAGE ACTION JUSTIFICATION
→ OBJECT LOGIC / STAGED AUTHENTICITY
→ LIGHTING / NIGHT REALISM
→ FILM / FORMAT / CAROUSEL SYSTEMS
→ ANTI-AI SELF-CHECK
```

---

## Quick Activation Matrix

| Scene Need | Activate |
|---|---|
| viewer should stop scrolling | Attention Routing |
| subject sees / ignores camera | Camera Relationship |
| pose feels too staged | Body Language Attraction |
| objects look like props | Object Logic V2 |
| night looks flat / AI | Night Realism |
| image reads generic Asian | HK Local Girl |
| carousel / photobook | V19 Carousel + V20 continuity checks |

---

## Minimal V20 Prompt Skeleton

```
[Character identity + safety]
[Photo existence reason]
[Camera relationship: who is taking this photo and how she reacts]
[Attention path: first anchor → transition → emotional destination]
[HK/local environment details if relevant]
[Body language justified by action]
[Objects with owner/timing/wear/lighting]
[Lighting/camera physics, especially night]
[Anti-AI constraints]
```

---

## Example: HK Cafe Friend-Shot

```
adult 24-year-old Hong Kong woman, lil.troublr canon intact,
photo exists because her friend caught her waiting for food at a cramped cha chaan teng,
CAMERA_REACTIVE warm recognition: eyes just found the phone camera, smile not fully landed,
attention path starts at iced milk tea condensation, travels through her hand and phone on the formica table,
then to her face; LOCAL_HK details: tissue packet, receipt, Traditional Chinese menu blur, friend's second drink cropped at frame edge;
body language: seated table lean, one shoulder slightly forward, phone hand relaxed;
objects share warm fluorescent cafe lighting and contact shadows, not prop-styled;
not model gaze, not perfect studio composition, not generic Asian cafe
```

---

## Example: HK Night Street

```
adult 24-year-old Hong Kong woman, friend-shot after late dinner,
photo exists because her friend called her name while she was checking taxi route;
attention path begins at wet pavement reflecting red taxi lights, rises through white sneakers mid-step and crossbody bag,
then to her face as she turns; CAMERA_REACTIVE playful recognition, expression between annoyed and laughing;
NIGHT_REALISM: convenience store white spill from right, red taxi tail-light reflections, phone screen glow under chin,
ISO grain in shadows, 1 stop underexposed, shallow DOF; HK_LOCAL: Traditional Chinese LED signs, folded umbrella, humidity flyaways;
no flat AI night, no static neon model pose
```

---

## V20 Self-Check

Before finalizing any prompt, ask:

1. Would someone actually take this photo? Why?
2. Who is holding the camera?
3. What does the viewer notice first?
4. What keeps attention after the first glance?
5. Does her body position have an action reason?
6. Do objects have owner, timing, wear, lighting, and shadow logic?
7. If HK, would a Hongkonger recognize the behavior/place/object stack?
8. If night, are light sources visible and physically consistent?
9. Is this improving prompt generation or just adding words?

---

## Source Modules

See `modules/V20/` for full runtime modules. See `research/V20_RESEARCH/` for original research + DeepSeek verification.
