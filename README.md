# Brick by Brick

A cozy idle game. You're the local wall maker, building a wall — and then a tower — toward a hole in the sky.

## Versions

- `index.html` — the landing page: tiles for the 2D original, the 3D version, and a changelog.
- `brick-by-brick-2d.html` — the 2D original, fastest to load.
- `brick-by-brick-3d.html` — the latest version, 3D (v8.0).

## How to play

Open `index.html` in a browser and pick a version. Mold bricks in the kiln, place them to build courses, earn money per brick and per row, buy upgrades, and chase combos. Reach 50 courses to win, then keep building in endless mode.

Made for a November game jam.

## History

Built iteratively across several versions (Oct–Nov 2026), with AI assistance directed by playtesting and feedback after each version — not generated in a single pass.

### 2D original — Oct 19, 2026

- Cozy idle core: hold to mold bricks in the kiln (~2s per brick), place them with a timing minigame.
- A course is 8 bricks; win at 50 courses, then endless mode.
- Economy: $1 per brick, $5 per row; combo streak pays $N per brick, a miss resets it.
- Special bricks: golden ($8 flat), hot (~12%, 10s fuse, pays 2× streak), lead (~6%, swings 50% faster, pays 3×). Golden keystone every 10th course.
- Upgrade tree: Kiln Fill Speed, Auto-Kiln, Auto-Layer, Second Chance, Precision Tools, Gilded Clay, Hot Mortar, Steady Hands.
- Story: a hole in the sky with silhouettes inside; the town's wall maker must build high enough to reach it.

### 3D rebuild (v10) — Nov 3, 2026

- The game rebuilt in 3D (Three.js), same core loop.

### 3D improvements build — Nov 3, 2026

- Kiln starts manual — it only bakes while you hold it; Auto-Kiln becomes a purchase.
- Upgrade costs rebalanced, with a clear reason to buy upgrades throughout.
- Full economy rebalance (bonuses, chains, gold/lead/hot bricks).
- Combo stash cascades: at combo 25 the stash pays out 5 bricks, 50 → 10, 100 → 25, 250 → all, then every 100 past 250 → all. Cascaded bricks place in rapid succession and keep the combo climbing.
- The Hand hazard: after the course-25 story beat, a hand descends and tries to grab bricks off the wall — place a brick on its fingers to fight it off, or it may tear down a course or two.

### 3D v2.0 — Nov 9, 2026 (feedback round, actioned)

- Opening reworked: more enticing loading and start screens; Start goes straight to making bricks, with the story dripping in after rows instead of up front.
- Story: first story popup after row 1 (a little about the hole in the sky); villagers join after each finished row up to row 5 and talk about the hole; at row 5 they ask you to build closer to the hole — a tower, not a wall — rebuilding the four other sides with a full rotation around it in 3D.
- Pay: rows 1–5 are unpaid (it's your job); pay starts when the tower build begins, with a reworked gold-and-coins burst effect.
- Next-brick placement outline is now blue, for color accessibility.
- Kiln is now a little building you tap, with a circular fill indicator on top (above your thumb); a finished brick animates down to a little storage building instead of in-hand storage. (Supersedes the earlier kiln-button idea.)
- Streak reworked: better look, and slower scaling so the max comes after more bricks laid.
- New upgrades: Predictable Placement (the mechanical arm always spawns the next brick a set distance away, so you always get about the same time to place it), More Apprentices, Faster Apprentices.
- Apprentices: the placement spot glows for a second before they place a block, pulsing as a countdown (1s, 0.5s, 0.25s).
- Background life: below row 50, nice things float by (birds from row 10, a kite, glow bugs); past row 50, spooky things (eyes, peepers, limbs, imps, ghost-jellies).

### 3D v3.2 — Nov 9, 2026 (round 2 feedback, actioned)

- First 5 days' wall shortened to 6 bricks wide; tower sides lengthened to 6 (6×6 footprint, 24-brick tower).
- Villagers gather slower at the start.
- Villager speech bubbles now pop up below their heads, so they don't cover the top layer of bricks.
- First payday highlighted with a popup card and a coin shower.
- Costs rebalanced for the slower cash flow (re-priced for the 6-wide wall and 24-brick tower).

### 3D v8.0 — Nov 9, 2026 (round 3 feedback, completed)

- Brick Sorter unlock: one warehouse per brick type, with warehouse tabs inside the storage building; the active warehouse feeds the crane, and apprentices build from the warehouse you have selected.
- Same-type streak bonuses: every lead / silver / gold brick in a finished row adds +2 / +2.5 / +3 × rate to that row's payout; a whole row of one metal pays a pure-row bonus on top.
- Tower sides are no longer auto-built — you build them yourself.
- Full economy rebalance: upgrade prices reflect their value, and the unlockable brick types (lead, silver, gold) are rebalanced around the more frequent per-face pay.

### 3D v7.3 — Nov 9, 2026 (round 3 feedback, most of it)

- Villager text now appears below their heads; background music added — calm medieval for the first 5 rows, upbeat energetic medieval after that, a bit eerie at row 25, spooky at row 50, melty and weird (but still enjoyable) at row 75.
- Crowd builds 1 person on day 2, 2 on day 3, 4 on day 4, 6 on day 5; automatic saving added.
- Tower: villagers spread around every side, and pay per row now means per row per face (one full side, one layer).
- Upgrade prices reflect their value: Hotter Kiln first upgrade $10, Piece Work (pay per brick) $50; initial pay per brick is $1.
- Combo celebrations: backflips every 5, triple-height somersaults every 25, triple jumps every 50.
- Silver added as an unlockable brick type; unlock order lead → silver → gold; all buyable unlocks now chained in a visual skill-tree tab interface.
- Perfects as a paid upgrade; the coin shower now shows the actual amount paid; birds and things flying by are tappable with per-type reactions; the streak rises 0.01 per brick.
- Still open: Brick Sorter with separate warehouses per brick type, apprentices pulling from the selected warehouse (round 3 items 16, 17, 20); same-type streak bonuses, whole-row bonus, gold +3 / lead +2 row bonuses (18, 19, 21–23); tower sides built by hand instead of auto-built (5); the full economy rebalance (7, 8, 27), since those prices depend on the above.

### Repo — Nov 9, 2026

- 2D original published as `index.html`; 3D improvements build published as `brick-by-brick-3d.html`; v2.0 published the same day, replacing the 3D file; v3.2 published later the same day, replacing the 3D file again; v7.3 published later still, replacing the 3D file again; landing page published later still as the new `index.html`, with the 2D original moved to `brick-by-brick-2d.html`; v8.0 published later still, replacing the 3D file again.
