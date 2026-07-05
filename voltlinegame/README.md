# VOLTLINE — Neon Horizon Runner

A high-fidelity cyberpunk endless runner built with Three.js. Weave through night-city
traffic on a neon-lit, rain-slicked highway — and whatever you do, don't crash twice.

## Play

Open `index.html` from any static web server (or GitHub Pages). No build step.

- **Swipe left / right** (or `←`/`→`, `A`/`D`) — change lanes
- **Swipe up** (or `↑`, `W`, `Space`) — jump
- **Swipe down** (or `↓`, `S`) — slide / fast-fall
- `P` / `Esc` — pause

## Features (v2)

- **High-fidelity rendering** — real-time planar reflections on the wet road,
  Unreal-style bloom post-processing, image-based lighting on all metals,
  volumetric-ish headlight beams, rain, lightning, animated signage.
- **Traffic** — moving civilian vehicles (sedans, taxis, vans, sports cars) that
  drive ahead of you, telegraph lane changes with indicators, and reward
  near-misses with score bonuses.
- **Pursuit system** — a hard crash puts a police interceptor on your tail for
  12 seconds, sirens and strobes blazing. Crash again while pursued and it takes
  you out. Survive the timer to earn an evasion bonus (+score, +credits).
- **Garage** — spend earned credits on four purchasable vehicles, each with its
  own 3D model and speed / handling / armor stats:

  | Vehicle | Type | Price |
  |---|---|---|
  | VOLT RUNNER | rebel concept bike (balanced) | free |
  | DRIFTER | street cruiser | 250 ◆ |
  | KATANA ZX | fast, agile, fragile superbike | 450 ◆ |
  | RONIN GT | armored muscle coupe | 1,000 ◆ |
  | SPECTRE X | fastest; gravlift hoverbike | 1,800 ◆ |
  | AEGIS MK-II | heavily armored trike | 2,800 ◆ |

- **Speed** — cruising/top speed up ~150% over v1, with FOV stretch, speed
  lines and retuned spawning to match.
- Fully synthesized music and SFX (no audio assets), localStorage save,
  adaptive quality fallback for weaker devices.

## Asset credits

- VOLT RUNNER: "Audi Rebel F1" concept bike — free Sketchfab download (add author credit here)
- Enemy chase car: "2058 Quadra Turbo-R V-Tech" — free Sketchfab download (add author credit here)
- KATANA ZX: "Motorcycle concept sketch" — free Sketchfab download (add author credit here)
- SPECTRE X: "Hoverbike post-apocalypse" — free Sketchfab download (add author credit here)
- Garage character: "Empire of Future" — free Sketchfab download (add author credit here)
- DRIFTER: "Motorcycle" by [Poly by Google](https://poly.pizza/u/Poly%20by%20Google) — CC-BY, via Poly Pizza
- Traffic & police cars: [Quaternius](https://poly.pizza/u/Quaternius) — CC0 (public domain), via Poly Pizza
- Skyline towers: "Sci-fi buildings pack low-poly" — free Sketchfab download (add author credit here)
- Street frontage: "Building pack" — free Sketchfab download (add author credit here)
- Overhead gantries: "Highway modular street assets vol. 04" — free Sketchfab download (add author credit here)
- Blockade operator: "Tactical stance cyberpunk armored operator" — free Sketchfab download (add author credit here)
- Remaining vehicles, the rider, city and effects are procedurally generated in code

> Note: most free Sketchfab downloads are CC-BY — fill in each author's name above
> (from the model's Sketchfab page) before public release. Trademarked designs
> (Audi, the Cyberpunk 2077 Quadra) are fine for prototyping but should be
> replaced or renamed before an App Store / Play Store release.

## Development

- `vendor/` contains Three.js r128 plus the post-processing/reflector modules,
  vendored locally so the game works offline and can later be wrapped for the
  App Store / Play Store (e.g. with Capacitor) without CDN dependencies.
- Append `?debug=1` to the URL to expose `window.__VL` test hooks
  (`spawnCar`, `startPursuit`, `pursuitKill`, `setCredits`, …).

## Hosting on GitHub Pages

Repo → Settings → Pages → Source: `main` branch, root folder. The game is a
static site; nothing else is required.
