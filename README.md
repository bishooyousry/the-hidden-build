# The Hidden Build — Skills Bank team game

Single-file HTML game (`index.html`). Teams of one **Messenger** (sees the secret brick blueprint) and **Builders** (each builds one part, never sees it). Parts are assembled and compared with the blueprint. Bilingual EN/AR, sounds + procedural music, live trainer console.

## Publish (GitHub Pages)
1. Create a repo, upload `index.html` and `.nojekyll` to the root.
2. Settings → Pages → Deploy from branch → `main` / root.
3. Open the published URL (do **not** use a preview/artifact viewer: it blocks the network).

## Run a session
1. Open the page → **Trainer Dashboard** → PIN `2026` (hides the UI only, not real security).
2. Copy the player link (or the Arabic link) and share it. Players enter a name, pick a style and a team; the first to tap "I'll be the Messenger" is the Messenger.
3. Check the ready row, pick the blueprint (or Random) and the time, press **START ROUND**.
4. After the round: **Reveal leaderboard**, projector view, CSV export.

## Scoring
Accuracy = correct bricks / (blueprint bricks + stray bricks), as %. Team score = accuracy × 10 + time bonus (0–100, only if every builder locked early AND accuracy ≥ 50%). Max < 1100. Everyone on the team gets the team score.

## How it works / honest limits
- Live sync uses the public **ntfy.sh** relay (SSE + POST). No backend, no keys. Public and not confidential: use fictional play only. `?relay=https://your-ntfy` uses your own server.
- The clock uses the relay's server time, so devices with wrong clocks stay in sync (±1 s).
- 4 teams, max 6 people per team (1 Messenger + up to 5 Builders). A team needs a Messenger and at least one Builder. No solo mode.
- "Picture named" is a keyword check on the Messenger's chat, not a quality judgement. Style chips are a self-pick, not an assessment.
- Free ntfy.sh may rate-limit or cap messages and ~30 streams per IP. Not measured: test before a large class.
- Tested headless (Playwright + mock relay): full team round, scoring, peek, chat, time-up, resume, Arabic, storage blocked. **Not tested:** real ntfy.sh, real phones/two devices, audio by ear, SSE-blocked polling for this game.

## Two-device checklist
1. Trainer on laptop, 2 phones as Messenger and Builder (same team).
2. Roster appears on both; the trainer's ready row turns green.
3. Start: countdown, timers match; Builder paints, Messenger peeks and chats.
4. Lock → reveal animation, score equals the trainer's team card.
