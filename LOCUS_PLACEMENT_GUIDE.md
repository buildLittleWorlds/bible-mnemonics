# Locus Placement Guide

How to assign verse phrases to objects in Bible memory images.

---

## Flexible Arrangements

Images are generated with creative freedom — the model arranges objects naturally rather than to a rigid grid. After generation, identify which arrangement the image follows, then assign loci accordingly.

### Arrangement A: 3 Foreground + 3 Background

The classic zigzag. Three objects in foreground, three in background.

```
┌─────────────────────────────────────────┐
│                                         │
│   (6)            (5)            (4)     │   ← BACKGROUND
│   left         center         right     │
│                                         │
├ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─┤
│                                         │
│   (1)            (2)            (3)     │   ← FOREGROUND
│   left         center         right     │
│                                         │
└─────────────────────────────────────────┘
```

**Path:** Foreground L→C→R, then Background R→C→L

1. Phrase 1 → Foreground left
2. Phrase 2 → Foreground center
3. Phrase 3 → Foreground right
4. Phrase 4 → Background right
5. Phrase 5 → Background center
6. Phrase 6 → Background left

---

### Arrangement B: 4 Foreground + 2 Background

Common when the scene has a dominant foreground action. Four objects up front, two in the distance.

```
┌─────────────────────────────────────────┐
│                                         │
│        (6)                  (5)         │   ← BACKGROUND
│        left                right        │
│                                         │
├ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─┤
│                                         │
│   (1)       (2)       (3)       (4)     │   ← FOREGROUND
│   left    center-L  center-R   right    │
│                                         │
└─────────────────────────────────────────┘
```

**Path:** Foreground L→CL→CR→R, then Background R→L

1. Phrase 1 → Foreground left
2. Phrase 2 → Foreground center-left
3. Phrase 3 → Foreground center-right
4. Phrase 4 → Foreground right
5. Phrase 5 → Background right
6. Phrase 6 → Background left

---

### Arrangement C: 2 Foreground + 4 Background

Less common. Two objects close to viewer, four spread across the background (often figures or scene elements).

```
┌─────────────────────────────────────────┐
│                                         │
│   (6)       (5)       (4)       (3)     │   ← BACKGROUND
│   left    center-L  center-R   right    │
│                                         │
├ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─┤
│                                         │
│        (1)                  (2)         │   ← FOREGROUND
│        left                right        │
│                                         │
└─────────────────────────────────────────┘
```

**Path:** Foreground L→R, then Background R→CR→CL→L

1. Phrase 1 → Foreground left
2. Phrase 2 → Foreground right
3. Phrase 3 → Background right
4. Phrase 4 → Background center-right
5. Phrase 5 → Background center-left
6. Phrase 6 → Background left

---

## Identifying the Arrangement

After generating an image:

1. **Count foreground objects** — How many distinct objects are in the lower half / closer to viewer?
2. **Count background objects** — How many are in the upper half / farther away?
3. **Match to arrangement:**
   - A (3+3) — balanced foreground and background
   - B (4+2) — foreground-heavy
   - C (2+4) — background-heavy
4. **Assign loci** — Follow the path for that arrangement

If the image doesn't fit any pattern cleanly, adapt: the principle is always **foreground left-to-right, then background right-to-left**.

---

## Locus Specificity: One Thing Only

**Each locus is ONE visual element — not a cluster, not a person-with-accessories, not a machine-with-screen.**

The eye needs a single anchor point. When you look at that spot in the image, you should land on ONE thing.

### Wrong (too many elements)
- "Redbox machine with alien movie on screen" — that's a machine + a screen + an image
- "Boy in tie-dye shirt, finger on RENT button" — that's a person + clothing + hand + button
- "Girl bouncing, bandaged arm visible" — that's a person + pose + medical detail
- "Woman with beanie and shopping cart" — that's a person + hat + cart

### Right (single visual anchor)
- "Alien face on screen"
- "Tie-dye spiral pattern"
- "Bandaged arm"
- "Shopping cart handle"

### The Test

Can you point to it with one finger? If describing it requires "with" or "and," you've included too much.

**Person → pick ONE detail** (their hat, their hand position, their distinctive clothing feature)
**Machine → pick ONE part** (the screen, a button, a slot)
**Scene element → pick the tightest visual anchor**

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

**Arrangement identified:** A (3+3)

**Locus assignment (note single-element specificity):**
1. "And we know that" → specimen bag opening (foreground left)
2. "for those who love God" → trap's jaw mechanism (foreground center)
3. "all things work together" → skillet handle (foreground right)
4. "for good," → cave entrance darkness (background right)
5. "for those who are called" → white braid (background center)
6. "according to his purpose." → toothpick (background left)

---

## Quick Checklist

Before finalizing locus assignments:

- [ ] Have I identified the arrangement (A: 3+3 or B: 4+2)?
- [ ] Does each phrase follow the path order (foreground L→R, then background R→L)?
- [ ] Are objects spatially separated (not clumped)?
- [ ] Is each object visually distinct from the others in this image?
- [ ] Have I checked `object_registry` for recent repeats?
- [ ] Does the verse break into phrases that preserve meaning?
- [ ] If fewer than 6 natural units, is there a clear strategy (split or rest marker)?

---

*Last updated: 2025-12-28*
