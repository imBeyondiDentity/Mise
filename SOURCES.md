# MiSE: where the information came from

[Русская версия](SOURCES_ru.md)

This report lists the kinds of material MiSE's rules were built from,
which part of the code each one feeds, and what is and is not
recorded. MiSE suggests; the model still decides. Nothing here is an
official ByteDance statement unless marked as such.

## 1. Source groups

| # | Group | What it gave |
|---|---|---|
| A | Official Seedance 2.0 / 2.5 guides and model pages | Hard limits, reference types, ratios, prompt structure |
| B | Community practice: manuals, prompt collections, GitHub repositories, posts on X and forums | Prompt patterns, camera-move safety, "one action per shot", what breaks |
| C | The author's own `seedance-prompt-engineer` skill | Prompt anatomy, reference roles, audit checklist ("check everything") |
| D | An "expensive look" reference | The anti-"plastic" vocabulary: camera bodies, lenses, film grain, micro-detail |
| E | Physical lighting practice (film-set terms) | Light stacks: source, angle, Kelvin, key-to-fill ratio |
| F | Third-party comparison of Seedance 2.0 Fast and Standard (Morphed) | Facts about Fast; **not yet in the app** |
| G | The author's own projects (iDentity Prompt Engine, Peel, Airband, Trio) | Visual design, footer, switches, tone |

## 2. Where each group lands in the code

| File and block | Built from |
|---|---|
| `data.js` `LIM` (length, file counts, ratios, shot limits) | A, with B for the soft character limits |
| `data.js` `ROLES` (reference roles and their sentences) | A, C |
| `data.js` `BODY`, `BLOCK`, `COLOR`, `LENS` | D |
| `data.js` `LIGHT` (time of day, weather, genre) | E |
| `data.js` `MOVES` and the camera-safety rules | B, C |
| `data.js` `ARCH` (13 scene types, with RU and EN keywords) | B, C |
| `data.js` `SLOP` (empty words to strip) and `CONS` (constraints) | B, C |
| `data.js` `PACE` | B (one action per shot, shot length) |
| `engine.js` `lint()` and the score out of 100 | C |
| `engine.js` `buildMeta()` (LLM mode) | A, B, C |
| `src/style.css`, `template.html` | G |

## 3. Version facts

- **2.0:** 4 to 15 s, 12 files (9 images, 3 videos, 3 audio), numbered
  `Shot N`, fixed ratio list.
- **2.5:** 4 to 30 s, 50 files (30 images, 10 videos, 10 audio),
  whole-second stages (`0-5s:`), ratios 0.4 to 2.5, extra roles to
  edit or extend a clip.
- **2.0 Fast** (group F, a single secondary source): 720p maximum,
  4 to 15 s, cheaper, softer detail, works best with one action and
  one camera move per 4 to 8 s. Reference limits unknown.

## 4. What is recorded and what is not

- **Recorded:** the groups above, the mapping to code, and the one
  URL below.
- **Not recorded:** exact links and dates for groups A and B from the
  first research pass. They were not saved at the time, so this
  report does not invent them.
- **Needs checking before a release:** limits and ratios in group A
  can change when ByteDance updates the models. Re-check `LIM`
  against the official pages.
- **Untested:** everything in the engine is checked by a headless
  browser and a manual audit of outputs; no prompt was run on a paid
  generator for testing.

## 5. Known URL

- Seedance 2.0 Fast vs Standard (Morphed):
  https://morphed.app/blog/seedance-2-0-fast-vs-standard

## 6. To make this report complete

Send or re-run the research for group A and B and record, per
source: title, URL, date read, and which rule it supports.
