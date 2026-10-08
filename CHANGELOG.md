[Русская версия](CHANGELOG_ru.md)

# Changelog

## 1.3.0 - 2026-10-08

- New example "Music video · 2.5" (with an audio reference); the four examples now sit in an even 2 × 2 grid.
- Look & camera gets three new fields: **Colour grade** (eight grades, previously automatic only), **Pace** (calm, steady, fast; limits how many shots the text is split into and adds a pacing phrase) and **Lens** (24, 35, 85 mm, macro, anamorphic; replaces the focal length of the chosen camera body). The grid is now 2 × 4 with no gaps. Camera body names shortened to fit.
- References rebuilt as cards: tag and remove button on top, role and description at full width below. "+ Add reference" is replaced by three equal chips, "+ Image", "+ Video" and "+ Audio", so tags number themselves (@Image1, @Video1, @Audio1) and the role list shows only roles for that type.

## 1.2.4 - 2026-10-08

- Chip sizes worked out as one scale: action buttons 40 px, chips and small buttons 34 px, footer chips 40 px. Copy, .txt, .json, Link and Save now share one row at equal size; "Save" is back as a text chip (no star). A one-line hint explains Copy, Link and Save. The "LLM mode" tab is now just "LLM", and the counter reads "1424 chars · 219 words" with the limit on the right.
- "What I understood" rebuilt as an even grid of equal tiles (label above, value below) instead of ragged pills; the "text says 12 s" suggestion is an outlined tile. Fixed counts and units: "1 line", "3 stages", RU "1 реплика", "3 отрезка", "12 с".

## 1.2.3 - 2026-10-08

- Added the brand icon: orange viewfinder corners with a play mark on the dark rounded square. Embedded in the page as the favicon and the iPhone home-screen icon; `MiSE_icon.svg` and `MiSE_icon.png` (512 px) added for reuse.

## 1.2.2 - 2026-10-08

- Footer rebuilt as in the other projects: the chips are part of the page (no longer floating), "Github" on the left, "Contact" ("Написать") on the right linking to the author's email, and the project name MiSE with orange dots between them.
- Language switch pinned to the header (scrolls with the page instead of floating), as in the other projects.
- The "Model" label now sits centred above the version switch.
- Version tag moved from the footer into the top-left corner of the header, mirroring the language switch.

## 1.2.1 - 2026-10-08

- Rebuilt the drop-down styling as a single background rule with an inline arrow icon (the previous fix still showed system-grey lists with an oversized arrow on iPhone).
- Replaced the native drop-downs with custom faces (the system list still opens on tap), because Safari kept repainting them grey with a giant arrow.

## 1.2.0 - 2026-10-08

- The bottom-right chip now reads "Github" and opens the repository `imBeyondiDentity/Mise` in a new tab (it used to be "← iDentity" pointing to `../`).
- Fixed the GitHub Pages address in README, README_ru and the PDF guide to match the real repository name (`/Mise/`).
- Re-wrapped `LICENSE` to short lines so it no longer scrolls sideways on phones.

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
