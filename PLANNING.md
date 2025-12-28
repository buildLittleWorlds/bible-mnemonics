# Bible Mnemonics — Planning

## What This Project Is

Memorizing Bible verses using Densworld images as memory palaces. Each verse maps to objects in scenes from an imaginary world — arbitrary pairings that create unexpected resonance.

**Core principle:** The mapping between Bible text and source material is arbitrary. Do NOT match themes. Do NOT look for a "better" source. Meaningful connections emerge through stochastic resonance, not design.

**The stochastic commitment:** When random selection lands on a source, USE IT. Don't evaluate whether it "fits" the passage — there is no fitting. Extract whatever visual moment you can from that source and make it work. The arbitrariness is the point.

---

## Stochastic Source Selection (Established 2025-12-28)

The goal is **uniqueness through randomness**. A multi-pass process surfaces surprising combinations that wouldn't emerge from deliberate matching.

### Source Inventory

| Source Type | Count (Rating 3+) | Typical Content |
|-------------|-------------------|-----------------|
| curated-fragments | 806 | Vivid prose, scenes, texture |
| datasets | 129 | Names, relationships, measurements, taxonomy |
| generated-fragments | 72 | Narrative moments, character actions |
| living-ledger | 14 | Events, actors, locations, dates |
| other | 13 | World notes, misc |
| **Total** | **1,034** | |

### Phase 1: Automated Stochastic Search

Claude runs 2-3 random passes without knowing what they're looking for:

**Pass 1 — Random Seed:**
- Filter `SOURCE_AUDIT_LOG.json` to rating 3+ files
- Randomly select ONE file
- Read it, extract entities (names, creatures, places, objects)

**Pass 2 — Cross-Reference:**
- Pick a random entity from Pass 1
- Pick a random source TYPE different from Pass 1:
  - ore fragment → dataset
  - dataset → ore fragment
  - either → living-ledger
- Search that source type for the entity
- If found, read the match

**Pass 3 — Third Hop (50% chance):**
- If Pass 2 found something, extract new entities
- Pick one, search a THIRD source type
- Or: search for a region match in living-ledger

**Output:** A source bundle with 2-3 documents that intersect on some entity but come from different source types.

### Phase 2: Conversational Refinement

Claude presents:
1. The seed and what narrative moment it offers
2. The cross-references and what details they add
3. Possible "zoom directions" (e.g., "creatures.csv has more on Grimslew")

User chooses which threads to pull. Iterate until prompt has enough richness.

### Phase 3: Record

Update `BIBLE_MAPPINGS.json` with:
- `ore_source_path` (primary source)
- `cross_references: [...]` (enrichment sources used)

Track usage over time. If repetition becomes noticeable, check which paths are appearing frequently.

### Why This Works

Different source types provide different kinds of richness:

| Source Type | Provides |
|-------------|----------|
| Ore texts (curated) | Vivid scenes, atmosphere, prose texture |
| Ore fragments (generated) | Specific moments, character actions, objects in context |
| Datasets | Names, relationships, creature taxonomy, measurements |
| Living Ledger events | Causal chains, dates, actors, locations |

The stochastic process creates combinations that are:
- **Unique** — unlikely to repeat for a long time
- **Surprising** — entities connected across source types
- **Rich** — multiple layers of detail from different angles

---

## Session Workflow

1. I provide a verse reference (e.g., "Matthew 10:34-36")
2. Claude runs stochastic source selection (Phase 1)
3. Claude presents source bundle for refinement (Phase 2)
4. We iterate until we have enough detail for the prompt
5. Claude writes an image prompt following `PRODUCTION_TEMPLATE.md`
6. I generate the image in ChatGPT (DALL-E) or Gemini
7. I review and may request adjustments or regeneration
8. Once images are final, Claude assigns verse phrases to object loci
9. Update `BIBLE_MAPPINGS.json`, session HTML, and index

### Phrasal Units (Critical)

Break verses into **small phrasal units** (3–6 words), not sentences or clauses. Each locus holds one tight, memorable chunk. See `LOCUS_PLACEMENT_GUIDE.md` for the complete method.

**Example:** Matthew 10:34-36 (3 verses) became 11 phrasal units requiring 2 images.

### Visual Style

See `PRODUCTION_TEMPLATE.md` for the complete prompt formula. Key principles:
- Densworld field sketch style (watercolor wash + ink line work)
- Atmospheric color dominance by region
- Six findable objects as mnemonic loci
- The watching element always present

### Object Selection

**⚠️ CRITICAL: Objects must come from the source text, not from habit.**

Claude has a tendency to default to "expedition gear" vocabulary (lantern, rope, surveying equipment, compass, journal) regardless of what the source material actually contains. This defeats the purpose of stochastic selection.

**Before listing objects, ask:**
1. What objects are *actually mentioned* in the ore fragment?
2. What body parts, clothing, or environmental features are described?
3. What is the character doing, wearing, touching?

**If the source has no objects:** Use body parts (hands, boots, hair), clothing details (skirt hem, sleeve, collar), environmental features (stones, wall texture, shadow shapes), or the figure itself broken into parts.

**Do NOT default to:**
- Lanterns (unless explicitly in the scene)
- Rope (unless explicitly in the scene)
- Surveying equipment (unless explicitly in the scene)
- Journals/notebooks (unless explicitly in the scene)
- Compasses (unless explicitly in the scene)

**Do:**
- Track used objects in `object_registry` within `BIBLE_MAPPINGS.json`
- Prefer objects specific to the ore fragment's narrative
- Use body parts and clothing when the scene is sparse
- Consider environmental textures as loci (wet wall, scattered stones, shadow edge)

---

## File Structure

```
_bible-mnemonics/
├── PLANNING.md                # This file — process documentation
├── PRODUCTION_TEMPLATE.md     # Ready-to-use prompt formula
├── LOCUS_PLACEMENT_GUIDE.md   # How to break verses and assign to loci
├── BIBLE_MAPPINGS.json        # Verse→image→locus lookup + object registry
├── SOURCE_AUDIT_LOG.json      # Visual richness ratings (1-5) for 1,034 sources
├── ORE_SOURCES.json           # Legacy: 275 curated W1 sources
├── PASSAGE_QUEUE.json         # Verses queued for memorization
├── PASSAGE_QUEUE.md           # Human-readable queue
├── index.html                 # Web deployment home page
├── sessions/                  # Session HTML files
├── images/                    # Generated images
├── sources-for-bible-passages/ # Verse source material
└── _archive/                  # Archived scripts and reference docs
```

### Key Files for Stochastic Selection

| File | Purpose |
|------|---------|
| `SOURCE_AUDIT_LOG.json` | 1,034 rated sources (3+) across all types |
| `BIBLE_MAPPINGS.json` | Track what's been used, check for repetition |

**SOURCE_AUDIT_LOG.json** covers:
- `ore-fragments/` — Curated narrative fragments (806 rated 3+)
- `ore-fragments-generated/` — AI-generated fragments (72 rated 3+)
- `all-data-sets/` — Datasets with visual richness (129 rated 3+)
- `living-ledger/` — Event views (14 rated 3+)

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
3. **Note why** — Too short? No visual moments? Lacks concrete imagery?
4. **Replace** — Find a suitable replacement from the same region or category
5. **Use** — Use the replacement for the current image

### W1 and W2 Material

Both world types are valid sources for mnemonic images:

- **W1** = Densworld (imaginary world with its own physics, geography, characters)
- **W2** = Real-world settings (Godfrey Illinois, Alton, historical figures, Mississippi River)

W2 locations (McPike Mansion, Clark Bridge, Twenty-Ten coffee shop) are as visually rich as W1 and work equally well as memory palaces. The arbitrariness principle applies: any vivid scene can anchor Bible verses, regardless of which world it depicts.

**What to exclude:** Sources lacking concrete visual imagery—pure data, metadata, abstract concepts. The test is visual richness, not world origin.

---

## Deployment

GitHub Pages: https://buildlittleworlds.github.io/bible-mnemonics/

Repository: https://github.com/buildLittleWorlds/bible-mnemonics

After each session, commit and push to deploy updates.

---

## Open Questions

1. **Entity extraction** — How best to extract names, creatures, places from source files? Current approach: experiment with regex for capitalized words + known creature names from `creatures.csv`.

2. **Long verses** — What if a verse needs 10+ images? No examples yet.

3. **Repetition detection** — When should we start checking `BIBLE_MAPPINGS.json` for frequently-used paths? Current answer: not yet, track passively for now.

---

*Last updated: 2025-12-28*
