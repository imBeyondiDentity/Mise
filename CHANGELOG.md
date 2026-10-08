[Русская версия](CHANGELOG_ru.md)

# Changelog

## 1.2.0 - 2026-10-08

- The bottom-right chip now reads "Github" and opens the repository `imBeyondiDentity/Mise` in a new tab (it used to be "← iDentity" pointing to `../`).
- Fixed the GitHub Pages address in README, README_ru and the PDF guide to match the real repository name (`/Mise/`).
- Re-wrapped `LICENSE` to short lines so it no longer scrolls sideways on phones.
- Rebuilt the drop-down styling as a single background rule with an inline arrow icon (the previous fix still showed system-grey lists with an oversized arrow on iPhone).
- Replaced the native drop-downs with custom faces (the system list still opens on tap), because Safari kept repainting them grey with a giant arrow. Footer now shows the version (v1.2.2).
- Footer rebuilt as in the other projects: the chips are part of the page (no longer floating), "Github" on the left, "Contact" ("Написать") on the right linking to the author's email, and the project name MiSE with orange dots between them.
- Language switch pinned to the header (scrolls with the page instead of floating), as in the other projects.
- The "Model" label now sits centred above the version switch.

## 1.1.0 - 2026-10-08

- Named the tool **MiSE**. The header now shows only the name, centred, with a small bilingual kicker above it; the two tagline sentences are gone.
- Browser tab title, `.json` export and docs renamed to MiSE.
- README and README_ru rewritten in the Trio format: licence and "Open MiSE" pill badges, language switcher, structure, GitHub Pages publishing, limitations.
- Added `MiSE_guide.pdf`, a bilingual (RU and EN) plain-words guide to every feature, explained for a fifth grader.
- Fixed drop-down lists and fields showing system styling in Safari on iPhone (added `-webkit-appearance` resets) and stopped iOS zooming in on focus.
- Fixed "Strip empty words" in *Improve my prompt* leaving a stray full stop at the start of the text.

## 1.0.0 - 2026-10-08

- First release: Seedance 2.0 and 2.5 in one generator, RU/EN interface.
- Rules engine: 13 scene archetypes, physical light stacks, camera-move safety rules, timing allocation, dialogue extraction.
- LLM mode (meta-prompt), Improve mode with a linter, history with favourites, share links, `.txt` and `.json` export.
