# Click Battle

A 10-second flying-sphere click challenge. Single HTML file, no build, no server.

**Play:** https://gravityst.github.io/click-battle/

## Game
- A blue sphere ricochets across the screen.
- You have **10 seconds**. Click the sphere as many times as you can.
- Each click teleports the sphere and makes it faster.
- Top 10 scores save to your browser (`localStorage`) and update live after every run.

## Run locally
```bash
git clone https://github.com/gravityst/click-battle.git
cd click-battle/docs
python3 -m http.server 8000
```
Open http://localhost:8000.

## Tech
- One file: `docs/index.html` (~135 lines including style + script).
- Visual style forked from [`gravityst/snake.io`](https://github.com/gravityst/snake.io).
