# plug-source-media

Public static media for [Plug Source](https://plug-source.deed.page) (Revere Fire hydrant map / apparatus 3D viewer).

Served via GitHub Pages: **https://rking78192.github.io/plug-source-media/**

## Contents
- `models/e1/` — Engine 1 compartment and pump-panel photos
- `models/l1/` — Ladder 1 compartment photos
- `models/stations/` — Station 1–5 popup logos (WebP, transparent background)
- `models/*.glb` — apparatus 3D models

## Adding new photos
1. Add the optimized JPEG under `models/e1/` or `models/l1/` (EXIF-transposed, ~1600px, q82 is fine).
2. Commit and push to `main`.
Station logos (v4.80+, navy fill + gold outline) live at `models/stations/station-N-v480.webp` (N = station number). The earlier v4.79 files `station-N.webp` remain for any old cached clients.

3. In the Plug Source app `models/compartments.json`, set the compartment `photo` to the same relative path (e.g. `models/e1/e1-8.jpg`). The app prefixes the Pages base URL at runtime.

No app code, hydrant data, or secrets belong in this repo.
