# MiSE

[![Licence: MIT](https://img.shields.io/badge/Licence-MIT-yellow.svg)](LICENSE)
[![Open MiSE](https://img.shields.io/badge/Open-MiSE-ff6a1a?style=flat)](https://imbeyondidentity.github.io/Mise/)

[Русская версия](README_ru.md)

**MiSE** is a prompt compiler for **Seedance 2.0 and 2.5**. You describe a video in plain words; MiSE works out what you mean, picks the right prompt format for the chosen model and splits the plot into timings.

Everything runs in your browser. No server, no uploads, no account, no API key. Once the page has loaded it also works offline.

## What it does

1. **Reads your brief.** It detects the scene type (13 kinds, from action to nature), light, weather, camera moves, aspect ratio, dialogue and the order of events, and shows what it understood.
2. **Builds the prompt.** Numbered shots for Seedance 2.0, second-level stages (`0-5s:`) for Seedance 2.5. Light is written as a physical setup (source, angle, Kelvin), cameras and lenses by name, and camera moves are kept within what the model handles.
3. **Checks its own work.** The same linter that powers *Improve my prompt* scores the result out of 100.

## Modes

- **Compile:** the rules engine. Free and offline.
- **LLM mode:** a ready-made meta-prompt with the Seedance rules inside. Paste it into Claude or ChatGPT for a fully English, polished prompt.
- **Improve my prompt:** paste any prompt to get a score, a list of problems and one-click fixes (strip empty words, add constraints).
- **History:** saved prompts with favourites, reopen and copy. Stored in your browser only.

Other features: RU/EN interface, Seedance 2.0/2.5 switch, references with roles (`@Image1`, `@Video1`, `@Audio1`), music, sound effects and dialogue, aspect ratio including custom ratios for 2.5, timeline view, `.txt` and `.json` export, and shareable links.

## Version differences

| | Seedance 2.0 | Seedance 2.5 |
|---|---|---|
| Length | 4 to 15 s | 4 to 30 s |
| Files | 12 (9 images, 3 videos, 3 audio) | 50 (30 images, 10 videos, 10 audio) |
| Structure | numbered `Shot N`, times optional | consecutive whole-second stages |
| Aspect ratio | fixed list | any from 0.4 to 2.5 |
| Extra roles | none | edit and extend a clip |

## Structure

```
index.html     the whole app (HTML, CSS and JavaScript in one file)
README.md      this file
README_ru.md   Russian version
CHANGELOG.md   history
MiSE_guide.pdf plain-words guide (RU + EN)
MiSE_icon.svg, .png brand icon (also embedded in index.html)
LICENSE        MIT
```

## Run locally

Open `index.html` in any modern browser. No build step, no dependencies. The fonts load from Google Fonts when online and fall back to system fonts offline.


## Limitations

- The rules engine does not translate. The scaffolding is English and your own wording stays as written. Use LLM mode for a fully English prompt.
- "Russian via Ukrainian tag" for speech is a community workaround, not an official feature.
- The rules come from the official Seedance guides, community practice and the iDentity `seedance-prompt-engineer` skill. MiSE suggests; the model still decides. No generation is run, so results on the paid generator may vary.

## Licence

MIT. Use, fork, modify and use commercially, provided copies keep the copyright notice and licence text. See [LICENSE](LICENSE).
