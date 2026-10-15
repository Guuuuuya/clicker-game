# RAMBO CLICKER

A dark neon / crypto-themed browser clicker. Cookie Clicker's structure rebuilt from
scratch in one self-contained HTML file: six buildings generate cookies per second,
twenty upgrades multiply them, and two prestige layers sit on top.

No build step, no dependencies, no CDN, no external assets. Plain HTML, CSS and
JavaScript in `index.html`.

Play it: **https://guuuuuya.github.io/clicker-game/**

## How to play

Click the bill to earn cookies. Buy buildings to automate production. Buy upgrades to
multiply both — each one is a one-shot that disappears when you take it.

When you have earned **1,000,000 in a single run** you can **Ascend**, trading everything
for permanent skill-tree points. After three ascends, **Legacy** unlocks: a second layer
that resets your cookies and upgrades but *keeps your buildings*, so it is worth taking
mid-run rather than only after one.

## How to open

Double-click `index.html`. It runs straight from disk.

Firefox blocks `localStorage` on `file://`, and Safari does the same in private mode. The
game detects this, runs in memory and shows a warning. To get real saving from Firefox,
serve the folder over http instead:

```
python -m http.server
```

then open `http://localhost:8000/`. (The hosted site is https, so saving just works there.)

## Where your save lives

`localStorage`, key `clicker.v1`. Preferences → Export writes a JSON file, which is the
only way to back up or move a save while the game is in fallback mode. Import refuses any
save written by a newer build rather than overwriting yours with something it cannot read.

## What's in the game

**Buildings** — six tiers, 1000 units each, with Cookie Clicker's shared 1.15× cross-boost:
every purchase lifts every other building's output.

**Upgrades** — 20 one-shot multipliers across a click branch, a per-building branch and a
global branch. They unlock as you play, appear as icons beside the bill, and are lost on
Ascend and on Legacy.

**Skill tree** — 18 nodes, 591 ascend points, five branches, spending the currency from
Ascend. Permanent, survives everything.

**Legacy perks** — 8 nodes, 365 legacy points, spending the currency from Legacy. `Eternal`
dissolves the reset mechanic entirely.

**Achievements** — 12, multiplying together to a ×12.82 bonus to all gains.

**Cookie Clicker parity** — milk that drops from clicks and can be traded back for points,
seasons that multiply production for 15 minutes, golden cookies that wander the building
column, building lore, a handful of easter eggs, and log-scale production graphs.

**Also** — offline progress up to 20 hours, a debug console, three themes, WebAudio sound
with nine events, and full keyboard support.
