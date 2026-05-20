# Click Battle

How fast can you click? Two modes (mouse and spacebar), a flying sphere with gravity, parallax stars, and a 4-player live multiplayer room.

**Play:** https://gravityst.github.io/click-battle/

## Game
- **10 seconds.** Mash to score. Each click sends your sphere up; gravity drags it back down.
- **Solo:** localStorage top-10 saved per browser. Mouse and Spacebar scores share one board with a mode badge.
- **Multiplayer:** create a room, share the 4-character code, up to 4 players see each other's spheres live. Final standings shown at the end.

## Run locally
Solo only (no server needed):
```bash
cd docs && python3 -m http.server 8000
```
Multiplayer (start the relay server too):
```bash
npm install
npm start          # ws://localhost:3000
# in another terminal:
cd docs && python3 -m http.server 8000
```
The client auto-points at `ws://localhost:3000` when you load it from localhost.

## Deploy
- **Client (GitHub Pages):** already wired. Push to `main` → `docs/` is served.
- **Server (Render):** [render.com](https://render.com) → New Web Service → connect this repo. `render.yaml` provisions a service named `click-battle`, so the WebSocket URL becomes `wss://click-battle.onrender.com` — which is exactly what the client expects in production.
