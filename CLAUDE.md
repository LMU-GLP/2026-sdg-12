# How this wiki works

This repo is a research wiki. It has three layers, and the order matters.

- `sources/` — one markdown file per source. Raw notes: title, URL, date read,
  key figures, short direct quotes, two-sentence summary. Never edit a source
  file to make it fit an argument. If a source says something inconvenient,
  that's information.
- `wiki/` — pages written *from* the sources. Every claim traces back to a file
  in `sources/`. A page with no citation behind it is a placeholder, not a page.
- `CLAUDE.md` — this file. The rules.

## Rules for Claude

1. Never write a figure into `wiki/` that isn't in a file in `sources/`.
   If a number is needed and no source has it, say so instead of supplying it.
2. Quote figures exactly as the source states them. Don't round, convert, or
   restate a percentage as "about half."
3. When two sources disagree, keep both and say they disagree. Don't average.
4. Cite by linking the source file, e.g. `[USC brief](../sources/la-food-insecurity.md)`.
5. Do not compare a figure from one country to a figure from another unless
   both measure the same thing the same way. Say so when they don't.
6. When asked to interview the team, ask **one question at a time** and give
   multiple-choice options where you can. Wait for the answer before the next
   question. Don't decide for them.

## This team's challenge

**How might we help a household reduce waste and make smarter choices about what members buy, use, and throw away?**

**Angle: fast fashion.** Framed as connected, not two separate stories —
households elsewhere buy fast fashion, it's manufactured and/or dumped in
Southeast Asia, and the pollution and waste land on households there. Cover
all three of: textile waste & disposal, manufacturing pollution, and the
secondhand/import clothing trade.

**Region: Southeast Asia, not yet narrowed.** Comparing three candidates
before committing to one:
- Indonesia (Citarum River area) — textile dyeing pollution, secondhand
  clothing imports despite a ban
- Cambodia (Phnom Penh) — garment manufacturing hub
- Vietnam (Ho Chi Minh City) — garment manufacturing plus fast-growing
  domestic fast-fashion consumption

**The two sources already in `sources/` (LA and South Korea, food waste) are
from before this pivot.** Leave them in place, but they are not part of this
challenge's angle — don't build wiki pages from them.

UN targets for this goal: https://sdgs.un.org/goals/goal12
