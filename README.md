# Brick by Brick

A cozy idle game. You're the local wall maker, building a wall — and then a tower — toward a hole in the sky.

## Versions

- `index.html` — the 2D original, fastest to load.
- `brick-by-brick-3d.html` — the latest version, 3D.

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

### Repo — Nov 9, 2026

- 2D original published as `index.html`; 3D improvements build published as `brick-by-brick-3d.html`.

### Planned — feedback round (Nov 8, 2026, not yet built)

- More enticing loading and start screens; Start goes straight to making bricks, with the story dripping in after rows instead of up front.
- Villagers appear after each row up to row 5, then ask for a tower instead of a wall — rebuild the four other sides with a full rotation around it in 3D.
- No pay for row 1; pay starts at the tower, with a better gold-and-coins shower effect.
- Kiln and storage become little buildings you tap; the streak gets a visual rework and slower scaling.
- New upgrades (Predictable Placement, More Apprentices, Faster Apprentices) and an apprentice placement glow-pulse countdown.
- Background life: nice things floating by below row 50 (birds from row 10, a kite, a glow bug), spooky things past row 50.
