# Bible Mnemonics — Planning

## System Sketch

**What's established:**

1. **Registry of W1 sources** — `ORE_SOURCES.json` contains ~100 curated ore fragments with high image potential, organized by region. Randomly select from these.

2. **One image per verse** — Each Bible verse gets its own Densworld image.

3. **Non-systematic approach** — Verses are added as they strike me during Bible study. No sequential plan, no target count.

4. **6 object loci per image** — Default structure. Verse is broken into 6 phrases mapped to the zigzag path (see `LOCUS_PLACEMENT_GUIDE.md`).

---

## What Needs Development

**Visual prompting method** — The ore fragments contain vivid narrative moments, but translating them into effective image prompts requires:

- Identifying the most imageable moment in a fragment
- Extracting 6 distinct, spatially separable objects from that moment
- Writing prompts that produce the cartographic illustration style
- Ensuring objects are visually distinct and memorable

This will be developed in a separate session focused on prompt engineering.

---

## Workflow (Current Understanding)

1. I provide a verse reference (e.g., "Matthew 10:34")
2. Claude randomly selects from `ORE_SOURCES.json` (high-potential sources)
3. Claude reads the selected ore fragment
4. Claude identifies the most vivid, unused moment
5. Claude writes an image prompt
6. I generate the image in Nano Banana Pro
7. Claude breaks the verse into 6 phrases and assigns to loci
8. Update `BIBLE_MAPPINGS.json`

---

## Files in This Folder

| File | Purpose |
|------|---------|
| `PLANNING.md` | This file — project overview |
| `ORE_SOURCES.json` | Registry of ~100 curated W1 sources |
| `LOCUS_PLACEMENT_GUIDE.md` | How to assign phrases to object loci |
| `BIBLE_MAPPINGS.json` | Tracking data (to be created when first image is complete) |

---

## Source Refinement Process

The curated list in `ORE_SOURCES.json` is a starting point, not a fixed inventory. When random selection produces a source that turns out to be unsuitable (W2 material, dialogue-only, too abstract, no visual moments), the workflow is:

1. **Stop** — Do not select another random source
2. **Remove** — Delete the unsuitable source from `ORE_SOURCES.json`
3. **Replace** — Find a suitable replacement from ore fragments in the same region
4. **Add** — Add the replacement to the curated list
5. **Use** — Use the replacement for the current image generation

This refines the curated list over time, ensuring it converges toward reliably usable W1 sources.

---

## Open Questions

1. **Verse phrase breaks** — Should Claude propose, or should I provide? (Current default: Claude proposes, I approve/adjust)

2. **Tracking "used moments"** — How granular? Per-fragment? Per-scene within fragment?

3. **Image storage** — Folder structure TBD

4. **Cross-project object registry** — Share with Commedia or keep separate?

---

*Last updated: 2025-12-27*
