# Brick by Brick

A cozy idle game. You're the local wall maker, building a wall — and then a tower — toward a hole in the sky.

## Versions

- `index.html` — the landing page: tiles for the 2D original, the 3D version, and a changelog.
- `brick-by-brick-2d.html` — the 2D original, fastest to load.
- `brick-by-brick-3d.html` — the latest version, 3D (v19.1).

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

### 3D v19.1 — Nov 14, 2026 (visual upgrade + slight optimization — round 10 feedback NOT included)

- Visual upgrade: a cel-shading pass — the cel bands are drawn in the shader instead of read from a ramp, with anti-aliased band edges, shadows leaning cool violet and lit faces leaning warm, and a soft rim of sky light picking out every silhouette, for a painted-storybook look.
- Slight optimization alongside it.
- Round 10 feedback is not in this version — it is still being collected.

### 3D v18.5 — Nov 11, 2026 (round 9 feedback, actioned)

- Screen flashes fixed (best-supported causes — couldn't be reproduced): the dragon and griffin are now anchored to the camera and stay on the horizon; balloons, floating islands, and giant mushrooms shrink away when the camera gets close and grow back slowly; clouds thin out near the camera; villagers step out of shot if the camera gets within 7 units. Butterflies were deliberately left alone — they still drift near the camera.
- Speech bubbles only come from villagers you can actually see — on screen, in front of the camera, not hidden behind the tower or wall. A line passes to a visible speaker or is dropped, and a bubble fades out if the camera turns its speaker out of view. The bonked villager still says "Ow!".
- The load-a-brick tutorial hint and the shed pulse now stay until the first brick is loaded, instead of vanishing after 6.5 seconds.
- Placement grades: NICE!, GOOD!, and PERFECT! pop above the brick at the moment you tap — GOOD is the middle 60% of the drop window, NICE is the rest of the hit zone, PERFECT is the white strip. PERFECT still needs the Perfect Eye upgrade, so early on the best you can earn is GOOD.
- New $4 starter upgrade, Warm-Up: shaves 0.2s off the kiln's opening bake time (4.5s → 4.3s), and only applies until you buy Hotter Kiln, so no other upgrade changed. It's also the workshop tutorial — the Shop button pulses once you hold $4, the workshop opens showing only this one card with a big BUY button and a "TAP TO BUY" arrow (a progress bar if you're under $4), and buying it gives confetti, a fanfare, "WORKSHOP UNLOCKED!", and a YAY banner before the full workshop fades in. Old saves skip the lesson and get Warm-Up for free.
- Butterflies: the flock was a flat 36 (14 on low quality); it now ramps from 3 on row 1 to 29 by row 10 (about 19% under the old max), 2 to 11 on low quality, and butterflies grow in and shrink out instead of popping.

### 3D v17.4 — Nov 11, 2026 (round 8 feedback, actioned)

- Hot bricks now show a visible cooling bar floating over the brick, so you can see how long until it's cool.
- Brick-setting time now starts at 1 second, with upgrades reducing it by 0.1s each — more upgrade steps on the way to instant.
- Workshop close X is in the top right corner.
- New miss animations: a brick lobbed at a villager's head ("OW!"), and a rare one where the brick turns into a leaf and the wind takes it ("BLOWN AWAY!").
- Hopper upgrade: automatically load multiple bricks into the crane.
- The exploding miss brick flies up in the air a little before it explodes.
- The loading wall explodes with bricks flying everywhere before the main menu.
- The first brick after buying a new brick type is always that type, so you see it demonstrated, then the normal percent chance applies.
- Tapping a hot air balloon explodes it into a shower of bricks.
- Edgar is in the workshop now: a banner of him at an anvil forging, and when you buy an upgrade he swings his hammer, the iron flares, and sparks fly.
- The storage shed's X of X count has a text shadow so it reads clearly against the background.

### 3D v16.3 — Nov 11, 2026 (round 7 feedback, actioned)

- Double gear button on the main menu fixed — the in-game gear is hidden on the title screen, which has its own gear.
- Settings cards are clickable anywhere to toggle the setting.
- Flying creatures are now tappable — the dragon and griffin (and other fly-bys) react when tapped.
- People never go transparent — villagers stay solid; only buildings and scenery fade when they're in front of the tower or wall.
- Speech bubble tails are on the bottom, not the top, and the bubbles are anchored to the people — the tail slides to stay on the speaker.
- Row-5 story cards: no more misclick-swipe on the first card — cards animate in and aren't clickable during the animation.
- The top-left number is gone as a row counter — it's now a HEIGHT counter that only appears once the goal to get to 50 is revealed.
- You can start baking another brick even if your storage is full — the finished brick waits in the kiln until there's room in the storage.
- The storage shed is narrower and starts just big enough for one brick, widening as Bigger Storage is bought.
- Backgrounds are fuller and more magical when moving around the tower.
- The next-block highlight animates in only once the turn to the new side has been made.
- People around the tower move, so it doesn't feel static.

### 3D v14.2 — Nov 11, 2026 (rounds 5 and 6 feedback, actioned)

- Upgrade famine fixed: new early upgrades Tip Jar, Lucky Brick, Hot Gloves, Coin Pouch, Cheer Bonus, Apprentice's Stool; the early game is very slow, and the earliest upgrades are speed, then storage.
- Storage now starts as a tiny shed holding 1 brick, upgradeable to 2, 3, 4, 5, 6, 7, 8, maxing out at ~16.
- Brick-setting-into-place animation added (0.5s), with an upgrade ladder 0.4s → 0.3s → 0.2s → 0.1s → instantaneous.
- Two more miss animations — an explosion and a 3D twirl toward the camera before the brick falls away — playing randomly, never the same one back to back.
- Mini kiln upgrade: a second, slower source of bricks that outputs higher-quality types more often.
- Tower-side rotation is much snappier.
- Circular tower upgrade: in the skill tree, unlocked once you've gotten the bricks down to three on a side — the square tower becomes a cylinder, one row per level, ~10–12 bricks per row.
- You now click your storage to load a brick, so background things and easter eggs are clickable again.
- Intro cards: swipe left to move forward, right to go back; the kiln card shows the real in-game kiln graphic — press and hold to bake, a mini tutorial that reinforces the one at game start; "tap anywhere" text moved to the top of the screen.
- Once all five tower rows are built and you start building higher, the citizens do subtle little dancing animations so they're not static.
- Buildings show little characters going in and out of houses, smoke from chimneys, lights in windows.
- Reset progress from the settings menu; the settings menu is cleaned up with cards and a better layout; the skill-tree UI/UX is vastly improved with good information design so it's clear what you're supposed to be doing.

### 3D v11.1 — Nov 10, 2026 (round 4 feedback, actioned)

- Upgrade text de-duplicated (e.g., kiln heating no longer repeats itself).
- Tower reworked to 5×5; objects hiding bricks drop to ~50% transparency so bricks stay visible.
- Villagers keep speaking after every finished row, even while the tower is being rebuilt.
- The 50-row goal is no longer shown at first — you're just a guy building a wall. Once the wall is 5 high and the tower is rebuilt to 5 high (total 10), you ask the villagers how many is enough and they say 50; past 50 it extends (course 100).
- Settings button on the main menu is clickable again; "A Tiny Wall Building Game" is readable against the background.
- Edgar intro cards on Start: Edgar is a gnoll from D&D (Three.js) — "Hey, this is you — you're Edgar," he loves building walls, first he makes the bricks (kiln shown), then he places them, then you play.
- Fantasy revamp: buildings more fantasy-esque, a wizard's tower in the background, dragons and griffins flying by, kept magical and mystical.
- The hole's story smoothed out: no hole on row 1; on row 2 a tiny hole appears and someone mentions they saw a hole in the sky — that's why the villager appears.
- Crowd messages now appear one at a time, fading away in a chain so they don't compete; pop-ups no longer block the kiln instructions; messages rewritten shorter, sweeter, snappier, with humor.
- People around the tower grow more magical as the rows go on (wizard hats, glowing auras, horns, hooves, satyr bodies).
- At row 5, the elder cards return: a little satyr old man with a big scarf and long horns — "Well, I'll pay you," and Edgar: "Not only do I like walls, I also like money — and I guess a tower is just four walls."

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

- 2D original published as `index.html`; 3D improvements build published as `brick-by-brick-3d.html`; v2.0 published the same day, replacing the 3D file; v3.2 published later the same day, replacing the 3D file again; v7.3 published later still, replacing the 3D file again; landing page published later still as the new `index.html`, with the 2D original moved to `brick-by-brick-2d.html`; v8.0 published later still, replacing the 3D file again; v11.1 published Nov 10, replacing the 3D file again; v14.2 published Nov 11, replacing the 3D file again; v16.3 published Nov 11, replacing the 3D file again; v17.4 published Nov 11, replacing the 3D file again; v18.5 published Nov 11, replacing the 3D file again; v19.1 published Nov 14, replacing the 3D file again.
