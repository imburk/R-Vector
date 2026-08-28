# R-VECTOR

A keyboard-driven horizontal shooter in the spirit of R-Type, built as a single
self-contained HTML file. No frameworks, no build step, no assets — everything
(graphics and sound) is generated at runtime with Canvas 2D and the Web Audio API.

## ▶ Play

**Option 1 — locally:** download `index.html` and open it in any modern browser.

**Option 2 — GitHub Pages:** if this repo has Pages enabled
(Settings → Pages → Deploy from branch → `main` / `/root`), the game is playable at:

> `https://<your-username>.github.io/r-vector/`

## 🎮 Controls

| Key | Action |
|---|---|
| **Arrow keys / WASD** | Move ship |
| **Z / Space** (tap) | Fire twin blasters |
| **Z / Space** (hold, release) | Charge and fire the Wave Cannon (3 power levels) |
| **X** | Launch the Force pod forward (returns like a boomerang) |
| **P** | Pause |
| **M** | Toggle sound |

## ✨ Features

- **Wave Cannon** — hold fire to charge through three power levels; the release
  unleashes a piercing wave beam with hit-stop, screen shake, and a flash.
- **Force pod** — an orbiting pod that can be launched as a forward shield:
  it damages enemies on contact and destroys enemy bullets, then boomerangs back.
- **Procedural terrain** — scrolling cave walls generated from layered sine waves,
  with terrain-mounted turrets. Colliding with terrain is fatal.
- **Five enemy types** — sine-weaving drones, aimed-shot gunners, drifting
  asteroids, gunships, and terrain turrets.
- **Boss battle** — at the end of every area loop, the Guardian boss alternates
  between aimed fans and spiral barrages from its opening core.
- **Loop-based difficulty** — 4 areas per loop; each loop scales enemy speed,
  HP, and fire rates.
- **Hi-score persistence** — saved locally via `localStorage`.
- **Game feel** — hit-stop on big kills, screen shake, particle explosions,
  score popups, and synthesized sound effects (no audio files).

## 🛠 Tech

- **Single file:** one `index.html`, zero dependencies (one Google Font via CDN,
  which degrades gracefully to monospace if offline).
- **Rendering:** Canvas 2D at 960×540, scaled responsively to the window.
- **Audio:** all SFX are synthesized on the fly with the Web Audio API —
  oscillators and noise buffers, no samples.
- **Fixed pattern:** delta-time game loop with time-scale support for hit-stop.

## 📝 Notes

- Works in any modern desktop browser (Chrome, Firefox, Edge, Safari).
- Keyboard required; there is currently no touch or gamepad support.
- Audio starts on the first keypress (browser autoplay policy).

## 📄 License

MIT — feel free to fork, modify, and remix.
