# Locus Placement Guide

How to assign verse phrases to objects in Bible memory images.

---

## The Path Schema

The eye travels through the image in a specific order. Phrases are assigned to objects along this path:

```
┌─────────────────────────────────────────┐
│                                         │
│   (6)            (5)            (4)     │   ← TOP HALF
│  left third    middle third   right third
│                                         │
├─────────────────────────────────────────┤
│                                         │
│   (1)            (2)            (3)     │   ← BOTTOM HALF
│  left third    middle third   right third
│                                         │
└─────────────────────────────────────────┘
```

**Order:**
1. Phrase 1 → Left third, bottom half
2. Phrase 2 → Middle third, bottom half
3. Phrase 3 → Right third, bottom half
4. Phrase 4 → Right third, top half
5. Phrase 5 → Middle third, top half
6. Phrase 6 → Left third, top half

The path moves left-to-right across the bottom, then right-to-left across the top.

---

## Breaking Passages into Phrasal Units

Each locus holds **one natural phrasal unit** — a tight, memorable chunk. Break at natural speech pauses, not at sentence or clause boundaries.

### Principles

1. **Small units** — 3–6 words per phrase is typical
2. **Natural speech rhythm** — Where would you pause if speaking aloud?
3. **Parallel structures get their own loci** — Each item in a list is separate
4. **Verbs often start new units** — "to bring," "to set," "against" can each begin a phrase
5. **Count units first, then calculate images** — 6 loci per image

### Example: Matthew 10:34-36

**Passage:**
> "Do not think that I have come to bring peace to the earth. I have not come to bring peace, but a sword. For I have come to set a man against his father, and a daughter against her mother, and a daughter-in-law against her mother-in-law. And a person's enemies will be those of his own household."

**Phrasal breakdown (11 units → 2 images):**

| # | Phrasal Unit | Image |
|---|--------------|-------|
| 1 | Do not think that I have come | 1 |
| 2 | to bring peace to the earth | 1 |
| 3 | For I have come | 1 |
| 4 | to set a man | 1 |
| 5 | against his father | 1 |
| 6 | and a daughter | 1 |
| 7 | against her mother | 2 |
| 8 | and a daughter-in-law | 2 |
| 9 | against her mother-in-law | 2 |
| 10 | and a person's enemies | 2 |
| 11 | will be those of his own household | 2 |

Note: Image 2 has 5 units, leaving one locus unused.

### Calculating Images Needed

```
images_needed = ceil(phrasal_units / 6)
```

A passage with 11 units needs 2 images. A passage with 25 units needs 5 images.

---

## Handling Imperfect Images

### No object in the expected zone

Find the object **closest** to the correct zone. The path order matters more than exact positioning.

### Object is in the right zone but repeats a recent object

Skip it and find the **next closest** distinct object. Check `object_registry` in `BIBLE_MAPPINGS.json` for recent usage.

### Objects are clumped together

Prefer objects that are spatially separated from each other. A well-spaced path is easier to walk mentally.

---

## Object Selection Principles

1. **Follow the path** — The zone order (1→2→3→4→5→6) is primary
2. **Spatial separation** — Objects should not be adjacent; prefer spread across the image
3. **Distinctness** — Each object should be visually unique
4. **One object per locus** — Never combine two objects into one locus (e.g., "inkwell with wax seals" is wrong—choose either "inkwell" OR "wax seals", not both)
5. **Tight visual anchors** — The locus must be a specific point the eye can land on, not a whole scene or action. "The Boss" is a whole person—use "maze-braided red hair" or "the Boss's raised arm."
6. **No recent repeats** — Avoid objects used within the last week (~7 images)
7. **Long-term uniqueness** — Ideally, objects are unique across the entire project (this becomes harder over time)

---

## Example: Romans 8:28 (Yeller Quarry scene)

Verse: "And we know that for those who love God all things work together for good, for those who are called according to his purpose."

Image contains: open specimen bag (left foreground), crude trap (center foreground), iron skillet on stones (right foreground), the Boss at cave entrance (right background), White Yeller's braid (center background), toothpick on log (left background).

**Breaking the verse:**
1. "And we know that" → open specimen bag
2. "for those who love God" → crude trap
3. "all things work together" → iron skillet
4. "for good," → the Boss at cave entrance
5. "for those who are called" → White Yeller's braid
6. "according to his purpose." → toothpick on log

---

## Quick Checklist

Before finalizing locus assignments:

- [ ] Does each phrase follow the path order (bottom L→M→R, then top R→M→L)?
- [ ] Are objects spatially separated (not clumped)?
- [ ] Is each object visually distinct from the others in this image?
- [ ] Have I checked `object_registry` for recent repeats?
- [ ] Does the verse break into phrases that preserve meaning?
- [ ] If fewer than 6 natural units, is there a clear strategy (split or rest marker)?

---

*Last updated: 2025-12-27*
