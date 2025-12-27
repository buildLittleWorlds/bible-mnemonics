# Bible Mnemonics — Planning

## What This Project Is

Memorizing Bible verses using Densworld images as memory palaces. Each verse maps to objects in scenes from an imaginary world — arbitrary pairings that create unexpected resonance.

**Core principle:** The mapping between Bible text and Densworld is arbitrary. Do NOT match themes. Choose regions/ore randomly. Meaningful connections emerge through stochastic resonance, not design.

---

## Current Method (Established 2025-12-27)

### Session Workflow

1. I provide a verse reference (e.g., "Matthew 10:34-36")
2. Claude randomly selects from `ORE_SOURCES.json`
3. Claude reads the ore fragment and identifies a vivid, imageable moment
4. Claude writes an image prompt following `VISUAL_STYLE_GUIDE.md`
5. I generate the image in Nano Banana Pro
6. I review and may request adjustments or regeneration
7. Once images are final, Claude assigns verse phrases to object loci
8. Update `BIBLE_MAPPINGS.json`, session HTML, and index

### Phrasal Units (Critical)

Break verses into **small phrasal units** (3–6 words), not sentences or clauses. Each locus holds one tight, memorable chunk. See `LOCUS_PLACEMENT_GUIDE.md` for the complete method.

**Example:** Matthew 10:34-36 (3 verses) became 11 phrasal units requiring 2 images.

### Image Types

Four types, documented in `VISUAL_STYLE_GUIDE.md`:

1. **Landscape View** — Wide exterior, objects across terrain
2. **Narrative Scene** — Frozen moment from ore fragment with characters
3. **Object Interior** — Close view of large object (e.g., Oneride), parts as loci
4. **Architectural Interior** — Inside a building, furnishings as loci

### Visual Style

Use Densworld's own visual vocabulary (NOT real art history):
- Cartographic Guild illustration style
- Color palette from Densworld materials (Quarry Ochre, Iron Gall Black, etc.)
- Clean lines, unified lighting from top-left, deep focus
- Six distinct objects clearly separated by negative space

### Object Selection

- Track used objects in `object_registry` within `BIBLE_MAPPINGS.json`
- Avoid repetition (no open books/ledgers/journals appearing too often)
- Prefer objects specific to the ore fragment's narrative
- Consider using parts of larger objects when variety is needed

---

## File Structure

```
_bible-mnemonics/
├── index.html                 # Home page with session list
├── PLANNING.md                # This file
├── VISUAL_STYLE_GUIDE.md      # Image generation guide
├── LOCUS_PLACEMENT_GUIDE.md   # How to break verses and assign to loci
├── BIBLE_MAPPINGS.json        # Verse→image→locus lookup + object registry
├── ORE_SOURCES.json           # Curated W1 sources for random selection
├── sessions/
│   └── YYYY-MM-DD.html        # One HTML file per session
└── images/
    └── YYYY-MM-DD/            # Images organized by session date
        ├── bible-001.png
        ├── bible-002.png
        └── ...
```

### Image Naming

Images are named sequentially: `bible-001`, `bible-002`, etc. The image name does NOT reference the Bible passage — that connection lives in `BIBLE_MAPPINGS.json`.

---

## Data Structures

### BIBLE_MAPPINGS.json

```json
{
  "verse_index": {
    "Matthew": {
      "10": {
        "34": [
          { "image": "bible-001", "locus": 1, "text": "Do not think that I have come" },
          { "image": "bible-001", "locus": 2, "text": "to bring peace to the earth" }
        ]
      }
    }
  },
  "images": {
    "bible-001": {
      "image_file": "images/2025-12-27/bible-001.png",
      "region": "Capital",
      "ore_source_id": "capital-003",
      "loci": {
        "1": { "object": "worn leather seat", "placement": "bottom-left" },
        ...
      }
    }
  },
  "object_registry": ["worn leather seat", "brass control lever", ...]
}
```

This structure enables efficient verse lookup: `Matthew → 10 → 34 → [image, locus, text]`

---

## Source Refinement

The curated list in `ORE_SOURCES.json` is refined over time. When random selection produces an unsuitable source:

1. **Stop** — Do not select another random source
2. **Remove** — Delete from `ORE_SOURCES.json`
3. **Note why** — W2 material? Too short? No visual moments?
4. **Replace** — Find a suitable replacement from the same region
5. **Use** — Use the replacement for the current image

### W1 vs W2 Material

- **W1** = True Densworld (imaginary world with its own physics, geography, characters)
- **W2** = Real-world references (Godfrey Illinois, historical figures in Earth settings)

Only W1 material is suitable. If an ore fragment references real Earth locations or people in non-Densworld contexts, remove it from the source list.

---

## Deployment

GitHub Pages: https://buildlittleworlds.github.io/bible-mnemonics/

Repository: https://github.com/buildLittleWorlds/bible-mnemonics

After each session, commit and push to deploy updates.

---

## Open Questions

1. **Cross-project object registry** — Share with Commedia or keep separate? (Current: separate)

2. **Tracking "used moments"** — Currently using `images_extracted` in ore sources. Need to actually update this when moments are used.

3. **Long verses** — What if a verse needs 10+ images? No examples yet.

---

*Last updated: 2025-12-27*
