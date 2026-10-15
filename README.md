# RAMBO CLICKER

A dark neon / crypto-themed browser clicker. Cookie Clicker's structure, rebuilt from
scratch in one self-contained HTML file: six buildings generate cookies per second,
twenty upgrades multiply them, and two prestige layers sit on top.

No build step, no dependencies, no CDN, no external assets. Plain HTML, CSS and
JavaScript in `index.html`.

## How to play

Click the bill to earn cookies. Buy buildings to automate production. Buy upgrades to
multiply both. When you have earned 1e6 in a run, **Ascend** for permanent skill-tree
points. After three ascends, **Legacy** unlocks — a second currency for permanent perks.

## How to open

Double-click `index.html`. It runs straight from disk.

Firefox blocks `localStorage` on `file://`, and Safari does the same in private mode.
The game detects this, runs in memory, and shows a warning. To get real saving from
Firefox, serve the folder over http instead:

```
python -m http.server
```

then open `http://localhost:8000/`.

## Where your save lives

`localStorage`, key `clicker.v1`. Preferences → export/import writes a JSON file, which
is the only way to back up or move a save while the game is in fallback mode.

## What is in the game

Under construction — built in stages. See `index.html` for current progress.

- 6 buildings (1000 units each), Cookie Clicker 1.15x cross-boost
- 20 upgrades, permanent for the run
- Ascend / Legacy prestige
- 591-point skill tree, 365-point legacy perks
- 12 achievements, milk, seasons, golden cookies