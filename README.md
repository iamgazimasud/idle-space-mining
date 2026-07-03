# 🛸 Idle Space Mining

A polished idle/incremental browser game. Start with a single mining drone on a lonely asteroid and build the largest automated mining empire in the galaxy.

**Easy to learn in 30 seconds. Difficult to master. Endless progression.**

## ✨ Features

- **16 resources** across 4 rarity tiers — from Stone to Singularity Fragments
- **13 planets** to unlock, from a humble asteroid to the Unknown Dimension, each with unique visuals, ores, and mining multipliers
- **10 miner tiers** — Mining Drone → AI Swarm → Reality Extractor
- **Factories** that refine raw ore into far more valuable goods
- **Energy grid** — generators vs. consumption, with production throttling when you overload it
- **25-node research tree**, 5 AI managers, 6 upgradeable ships
- **Exploration missions** with timed rewards and flavor outcomes
- **10 random events** — mining rushes, alien merchants, pirate raids
- **37 achievements**, each granting a permanent production bonus
- **Prestige** — Galactic Ascension for permanent +2%-per-point bonuses
- **Interactive tutorial** + full How to Play guide
- **Offline progress**, autosave, save export/import
- Procedural WebAudio soundtrack & effects, animated canvas planet scene — no assets, no dependencies, no build step

## 🎮 Play

Open `index.html` in any modern browser — that's it. Or serve it locally:

```sh
python3 -m http.server 4173
# → http://localhost:4173
```

## 🎹 Controls

| Input | Action |
|---|---|
| Click planet / `Space` | Mine ore |
| `1`–`9`, `0`, `-` | Switch tabs |
| x1 / x10 / x100 / Max | Bulk-buy amount |

## 🏗️ Architecture

Vanilla HTML/CSS/JS, zero dependencies:

- `js/data.js` — all game content as data (resources, planets, buildings, research, events…). Add content here without touching logic.
- `js/game.js` — production math, purchases, prestige, events, offline progress
- `js/ui.js` — DOM panels; rebuilds on structural change, cheap bound updates at 5 Hz
- `js/render.js` — canvas starfield, planet, drones, particles
- `js/sound.js` — procedural WebAudio (no audio files)
- `js/tutorial.js` — objective-based tutorial + help guide
- `js/state.js` — save/load/export (localStorage)

---

🤖 Built with [Claude Code](https://claude.com/claude-code)
