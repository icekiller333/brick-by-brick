# Brick by Brick

A cozy idle game. You're the local wall maker, building a wall — and then a tower — toward a hole in the sky.

## Versions

- `index.html` — the 2D original, fastest to load.
- `brick-by-brick-3d.html` — the latest version, 3D (v2.0).

## How to play

Open either file in a browser. Mold bricks in the kiln, place them to build courses, earn money per brick and per row, buy upgrades, and chase combos. Reach 50 courses to win, then keep building in endless mode.

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

### Repo — Nov 9, 2026

- 2D original published as `index.html`; 3D improvements build published as `brick-by-brick-3d.html`; v2.0 published the same day, replacing the 3D file.
