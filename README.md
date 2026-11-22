# The Hidden Build · Future City (Leadership Mission)

A premium, futuristic edition of the Skills Bank team activity **The Hidden Build** for senior managers and executives, in English and Arabic (RTL). It keeps every mechanic of the original (Messenger and Builders, secret blueprint, zones, chat, locks, scoring, trainer dashboard, projector, CSV, resume, relay) and changes the experience around it.

Single file: `index.html`. No frameworks, no external images, no external fonts. All visuals are CSS, SVG and Canvas.

## The idea
Teams are given one mission: rebuild a classified section of a future smart city. One **Messenger** (mission controller) sees the blueprint. The **Builders** (construction crew) never do, and each builds only their own zone. Parts are combined and compared with the original in a final reveal.

## Publish on GitHub Pages
1. Create a repository and upload `index.html` and `.nojekyll` to the root.
2. Settings > Pages > Deploy from branch > `main` / root.
3. Open the published address (not a preview viewer: it blocks the network).
4. Optional: add `?lang=en` to open in English. The default language is Arabic.

## Run a session
1. Open the page > **Trainer dashboard** > access code `2026` (hides the interface only).
2. Share the player link or the 5-character session code. Each player enters name + code and picks a team on one screen (one team colour per breakout room works well).
3. In every team the first person to tap **I'm the Messenger** becomes the Messenger; everyone else is a Builder.
4. Choose the blueprint (or Random), the round time and the Messenger pin option (Off by default), then press **START ROUND**.
5. Use the **Projector view** for the live city, **SHOW BUILDS** for each team's current structure, then **Reveal leaderboard** for the staged final reveal.

## Blueprints (9 x 7, five materials)
Smart City Core · Executive Headquarters · Strategy Bridge · Digital Command Center · Connected Network · Customer Experience Hub. Materials: coral (R), blue (B), orange (Y), cyan (G), white (W).

## What is new
Look and feel only, plus the Future City story: cinematic skyline background, holographic panels, architectural module grid, mission wording, staged leaderboard reveal on the projector, calmer effects. See `VISUAL_SYSTEM.md`. What was verified and what was not: see `TEST_REPORT.md`.

## Defaults you should know about
- Opens in **Arabic** (the language button or `?lang=en` switches).
- **Music is Off** by default (breakout rooms need voices); the ♪ button turns it on.
- Scoring is unchanged: accuracy x 10 + time bonus (0-100, only if every Builder locked early and accuracy is at least 50%).

## Limits
Live sync uses the public ntfy.sh relay: not confidential, fictional play only. 4 teams, up to 6 people per team (1 Messenger + up to 5 Builders). Test with two real devices before a large session.
