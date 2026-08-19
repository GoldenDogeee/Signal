# SIGNAL — Radar Reflex Trainer

**A fast-reflex arcade game built around a rotating radar scope.**

Contacts appear at random points on the scope and fade fast — click
green returns before they're lost. Red static costs you your streak
if you engage it. Rare amber contacts are worth big points. Forty-five
seconds on the scope, difficulty climbs the whole way.

---

## How it plays

- **Green contacts** — click before they fade. Consecutive hits build
  a streak multiplier (up to ×5).
- **Red static** — false returns. Clicking one costs points and resets
  your streak. Best left alone.
- **Amber contacts** — rare, high-value. Worth chasing.
- Missing a real contact (letting it fade unclicked) resets your streak,
  same as hitting static.
- Spawn rate and contact lifetime both ramp up as the 45-second timer
  runs down.

Score, streak, longest run, and accuracy are all tallied at the end,
with a locally-saved best score to beat next time.

## Under the hood

One self-contained `index.html` — a `<canvas>` radar rendered and
animated in real time (rotating sweep, phosphor-style fading contacts,
particle bursts), plus procedurally generated sound effects via the
Web Audio API. No images, no audio files, no external game assets —
just code, so there's nothing that can 404.

## Run it

Open `index.html` in any modern browser and click **Begin Scan**.

## Host it on GitHub Pages

**Option A — its own repo:**
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/<your-username>/<repo-name>.git
git branch -M main
git push -u origin main
```
Then in the repo: **Settings → Pages** → Source: **Deploy from a
branch** → Branch: `main`, folder `/ (root)` → **Save**. Live at:
```
https://<your-username>.github.io/<repo-name>/
```

**Option B — as a subpage of an existing site:**
Drop this `index.html` into a subfolder of a repo you already host,
e.g. `your-repo/game/index.html`. It'll be live alongside your existing
pages at:
```
https://<your-username>.github.io/<repo-name>/game/
```
No changes to your existing pages needed — just don't overwrite an
`index.html` you're already using.

Since everything is in one file, there's no separate CSS/JS path to
break — if the page loads, it loads exactly as intended.
