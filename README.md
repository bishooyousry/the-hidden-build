# The Hidden Build · Executive Mission (Future City)

A premium, futuristic leadership simulation for senior managers and executives, in English and Arabic (RTL). It keeps every mechanic of the original Hidden Build (Messenger and Builders, secret blueprint, zones, chat, locks, scoring, trainer dashboard, projector, CSV, resume, relay) and turns the build into an **executive mission**: each team constructs a critical structure of the organisation of the future.

Single file: `index.html`. No frameworks, no external images or fonts. Everything is CSS, SVG and Canvas.

## The six structures (blueprints)
| Blueprint | Arabic | What the team builds |
| --- | --- | --- |
| Strategy Tower | برج الاستراتيجية | A tower with an orange power core on top |
| Execution Bridge | جسر التنفيذ | A suspension bridge: two towers, cables, deck |
| KPI Dashboard | لوحة المؤشرات | A framed screen with three bars of different heights |
| Team Network | شبكة الفريق | Nodes in the four corners linked to a central hub |
| Customer Journey | رحلة العميل | A winding path from the start to the destination |
| Leadership Hub | مركز القيادة | Concentric rings around a core |

## Real components, not blocks
The five colours are five structural components: **white = glass facade**, **blue = smart steel panel**, **cyan = energy line / foundation**, **orange = power core (glows)**, **coral = actuator**. When a team gets every module right the structure comes **online** with a cyan glow and a banner.

## Messenger pin: on by default
The Messenger can pin the blueprint to their screen. **This is now On by default**; the trainer can switch it Off in the console (Mission configuration > Messenger pin) before each round. Off keeps the original "memory only" challenge.

## Publish on GitHub Pages
1. Create a repository and upload `index.html` and `.nojekyll` to the root.
2. Settings > Pages > Deploy from branch > `main` / root.
3. Open the published address (a preview viewer blocks the network).
4. The default language is Arabic; add `?lang=en` for English.

## Run a session
1. Open the page > **Trainer dashboard** > access code `2026` (hides the interface only).
2. Share the player link or the 5-character session code. Each player enters name + code and picks a team.
3. The first player in each team to tap **I'm the Messenger** becomes the Messenger; everyone else builds a zone.
4. Pick the blueprint (or Random), the time and the pin option; press **START ROUND**.
5. Use the **Projector view** (live city, team progress, **SHOW BUILDS**), then **Reveal leaderboard** for the staged reveal.

## Other defaults
Opens in Arabic. Music is Off (breakout rooms need voices); the ♪ button turns it on. Scoring is unchanged: accuracy x 10 + time bonus (0-100, only if every Builder locked early and accuracy is at least 50%).

## Limits
Live sync uses the public ntfy.sh relay: not confidential, fictional play only. 4 teams, up to 6 people per team. See `TEST_REPORT.md` for what was and was not verified.
