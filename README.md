# The Hidden Build · Executive Mission (Future City)

A premium, futuristic leadership simulation for senior managers and executives, in English and Arabic (RTL). Every mechanic of the original Hidden Build is kept (Messenger and Builders, secret blueprint, zones, chat, locks, scoring, trainer dashboard, projector, CSV, resume, relay). The build is now an **executive mission**: each team assembles one **structure** of the organisation of the future, **part by part**.

Single file: `index.html`. No frameworks, no external images or fonts: everything is CSS, SVG and Canvas.

## Parts of one structure, not blocks
- There are no blocks. The structure is **one continuous surface**: its parts join edge to edge and only the silhouette is lit.
- **Each Builder holds one part of the structure** (a slice of it) and works on it together with the others. The Messenger sees the whole structure and guides them. When the parts are joined, the team's structure is compared with the original.
- Five structural components replace colours: **steel plating** (blue), **glass facade** (white), **energy line** (cyan), **power core** (orange, glowing), **actuator** (coral).

## The four structures
| Structure | Arabic | Description |
| --- | --- | --- |
| Strategy Tower | برج الاستراتيجية | A stepped tower with a power core on top, glass floors, energy foundation |
| Execution Bridge | جسر التنفيذ | A cable-stayed bridge: a tall steel pylon, energy-line cables fanning to a glass deck |
| KPI Dashboard | لوحة المؤشرات | A framed screen with three bars of different heights |
| Team Network | شبكة الفريق | Four corner nodes linked by energy lines to a central hub |

## When the structure is built correctly it comes alive
A perfect build gets a **STRUCTURE ONLINE** banner and a light show that belongs to the structure: the tower's beacon pulses and a scan runs up its body, vehicles cross the bridge and pulses run down the cables, the dashboard draws a rising trend line with a scanning cursor, data packets travel along the network to the hub. The structure also **reacts to touch and mouse**: a spotlight follows the pointer and a tap sends a ripple. The same life appears on the projector leaderboard for perfect teams. Reduced-motion settings turn the animation off.

## Messenger pin: on by default
The Messenger can pin the blueprint to their screen. It is **On by default**; the trainer switches it Off in the console before a round for a "memory only" challenge.

## Publish on GitHub Pages
1. Create a repository and upload `index.html` and `.nojekyll` to the root.
2. Settings > Pages > Deploy from branch > `main` / root.
3. Open the published address (a preview viewer blocks the network).
4. The default language is Arabic; add `?lang=en` for English.

## Run a session
1. **Trainer dashboard** > access code `2026` (hides the interface only).
2. Share the player link or the 5-character session code. Players enter name + code and pick a team.
3. The first player in each team to tap **I'm the Messenger** becomes the Messenger; everyone else builds a part.
4. Pick the structure (or Random), the time and the pin option; press **START ROUND**.
5. **Projector view** for the live city and team progress (**SHOW BUILDS**), then **Reveal leaderboard**.

## Other defaults
Music is Off (breakout rooms need voices). Scoring is unchanged: accuracy x 10 + time bonus (0-100, only if every Builder locked early and accuracy is at least 50%).

## Limits
Live sync uses the public ntfy.sh relay: not confidential, fictional play only. 4 teams, up to 6 people per team. See `TEST_REPORT.md`.
