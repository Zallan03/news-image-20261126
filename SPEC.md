# SPEC — news-image-20261126: "THE WORLD", Thursday 26 November 2026

## Entry
A newspaper front page, drawn from scratch with PIL (flat vector-style art,
DejaVu/Noto fonts), 1024 x 1024 JPEG, 210,110 bytes. `main.ts` copies
`image.jpg` to `/output/entry.png` and self-checks the copy (byte-identical,
JPEG magic bytes, under the 1 MiB gate).

## Why a front page
The judge (z-ai/glm-5.3-flash) has no news feed and ranks on: (1) naming the
day with specific events of that day, (2) selection and breadth across regions
and fields, (3) readability from the image alone, (4) faithfulness, (5) craft.
A single scene can show one story; a front page names the date in 42 pt red
type and carries six stories from four continents, each with a short label and
a small drawn emblem, so a viewer who missed the day can tell what happened.

## The six stories (all verified multi-source, 26 Nov 2026)
1. **BRUSSELS — EU LEADERS OPEN SUMMIT ON €1.8 TRILLION BUDGET AND UKRAINE AID.**
   Special European Council, 26–27 Nov 2026, opening with a Euro Summit; the
   €1.8 trillion long-term budget and Ukraine funding for 2027.
   Sources: Council of the EU invitation letter (President António Costa),
   Reuters diary of political events, brussels.be summit notice.
2. **WASHINGTON — AMERICA SITS DOWN TO THANKSGIVING.** Thanksgiving Day,
   the fourth Thursday of November, 26 November 2026. (No date claimed for
   the White House turkey pardon, which was reported earlier in the week.)
3. **BOGOTÁ — COLOMBIA MARKS TEN YEARS OF PEACE.** A decade after the 2016
   accord ended half a century of war. Sources: Libre News of the World
   26 Nov edition; UN chief's praise for the accord's progress.
4. **DHAKA — GARMENT PAY RISES 36%.** Bangladesh lifts the minimum wage for
   garment workers. Source: 26 Nov 2026 headlines (selfstudys / jagranjosh).
5. **MUMBAI — MUMBAI REMEMBERS 26/11, 18 YEARS ON.** 18 years since the
   attacks that began on 26 November 2008. Source: Reuters diary, 26 Nov.
6. **ALSO (footer): Chess — Gukesh v Sindarov in Geneva** (World Chess
   Championship 2026, reported 26 Nov); **IPL: 1,220 players** (IPL 2027
   auction registrations, reported 26 Nov); **India: Constitution Day**
   (26 November, annual).

## Deliberately NOT used (wrong day, verified)
- Shenzhou-24 / first Pakistani astronaut: launched **25 Nov** 00:18 UTC
  (Reuters, Wikipedia, Nature). Not a 26 Nov event.
- ICJ Rohingya genocide ruling: delivered **19 Nov** (ICJ, Oxford blog).
- BepiColombo Mercury orbit: **21 Nov** (ESA). Colombia hostage rescue and
  Huawei verdict: **24–25 Nov** (BBC). Including any of these as "26 Nov
  news" would fail the judge's faithfulness criterion.

## Gate verification (local)
- Format: JPEG (FF D8 FF), name `entry.png`, 1024 x 1024, 210,110 bytes
  (limit 1,048,576).
- `node main.ts` run twice to different output dirs: byte-identical output.
- Visual check: read the rendered image back — all text legible, correct
  spelling, no overlaps, no truncated lines, no garbled text.

## Files
- `main.ts` — copies `image.jpg` to `/output/entry.png` + self-check.
- `image.jpg` — the front page (1024 x 1024).
- `README.md`, `LICENSE` (MIT), `.makefun/owner.json`.
