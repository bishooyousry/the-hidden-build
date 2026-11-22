# Visual system: Future City

## Palette (Skills Bank only)
| Colour | Hex | Use |
| --- | --- | --- |
| Deep Navy | #080828 | Background, environment, depth |
| Soft White | #EBF4FF | Typography, white material, blueprint detail |
| Soft Blue | #4D88E8 | Holographic panels, borders, interactive elements, blue material |
| Moderate Cyan | #40BDA9 | System activation, progress, connection, success, cyan material |
| Light Orange | #FFBC3A | Key objectives, timer warnings, rewards, the winner, orange material |
| Bright Coral | #F26A44 | Alerts, critical time, errors, coral material |
Transparency, gradients and glows are derived from these. No gold, brown or purple is used as a brand colour.

## Environment
- A **living skyline** drawn on a Canvas (three parallax layers of towers with lit windows, antennas with coral beacons, light streaks of traffic), a **perspective grid floor** in CSS, and a glass-and-navy atmosphere. It slows to a still image when the user prefers reduced motion.
- The **hero hologram** on the entry screen is an inline SVG smart city with a beam, an orbit ring and data links.

## Components
- **Holographic panels:** glass gradients, soft-blue borders, HUD corner brackets.
- **Construction grid:** a 9 x 7 holographic board. Modules (formerly bricks) are flat architectural panels with a light bevel, an inner panel line and a material glow. Empty cells are dashed holograms; zones outside a Builder's range are hatched "restricted" cells.
- **Classified blueprint:** a navy hologram that opens with a vertical scan-in, with a timer bar and a player watermark.
- **Mission HUD:** stage rail (team up, build, reveal), time bar that turns orange then coral, team marker, score.
- **Mission control (trainer):** one console for configuration, readiness, live team cards, debrief panel, CSV and import.
- **Projector:** a cinematic city, large mission timer, team progress, the original blueprint beside each team's structure, and a staged leaderboard.

## Motion and sound
- Motion is purposeful: scan-in for the blueprint, module drop and light-up on reveal, a light sweep across the compared boards, staged rank reveal. Confetti and shake are reduced. `prefers-reduced-motion` disables animation.
- Sound effects are the original synthesised set, kept quiet. Music is Off by default.

## Language and layout
LTR English and RTL Arabic. Boards and zone labels always stay left to right so "left" means the same in both languages. Arabic letter-spacing is disabled to keep letters joined. Digits are Western. Arabic copy is formal Modern Standard Arabic.

## Terminology
Bricks became **modules**. Messenger / **الناقل**, Builders / **البنّاؤون**.
