# Test report: The Hidden Build · Executive Mission (parts and live structures)

## How it was tested
Automated end-to-end run with Playwright (Chromium), separate browser contexts as separate players (trainer, Messenger, Builders, spectator) against a mock relay that speaks the same protocol as ntfy.sh. Screenshots of the builder surface, the classified blueprint with the pin button, the reveal with STRUCTURE ONLINE for three of the four structures (tower, bridge, network), and the earlier projector and phone checks of the same design system.

## Verified (52 automated checks passed, 0 failed)
Join with a 5-character code and a team; Messenger claim and roles; the blueprint reaches only the Messenger (63 cells, then closes); Builder zones (parts) cover all 9 columns; painting before GO is ignored; chat and quick questions; timer, time-up auto-lock, END ROUND NOW; locking and scoring (perfect build 100% with 1000 + bonus; 3 right + 1 stray scored correctly; no bonus under 50%); leaderboard reveal on players and projector; trainer dashboard, debrief panel, CSV, second session, exit; Arabic RTL; resume; storage blocked; the Messenger pin On by default. **The scoring algorithm and the relay protocol were not changed.**

## What changed in this version
1. **No blocks:** cells share edges and render as one continuous surface with only the silhouette lit. The data model is unchanged (the same 9 x 7 cells), so scoring, sync and the tests are unchanged.
2. **Four structures** instead of six: Strategy Tower, Execution Bridge (cable-stayed), KPI Dashboard, Team Network. Cables and links are edge-connected so they read as continuous lines.
3. **The structure comes alive** on a perfect build (shape-specific light show, pointer spotlight, tap ripples), on the player's reveal and on the projector leaderboard.
4. The palette is a row of round component chips with captions (Actuator, Steel, Core, Energy, Glass, Erase).
5. Earlier in this series: Arabic default, music Off, Messenger pin On by default, emojis removed, quick-chip and projector re-render fixes.

## Not verified
- **The real ntfy.sh relay and real devices.** Multiplayer was verified across separate browser sessions against a mock relay. Test with two real devices before the workshop.
- The Dashboard light show was not captured on screen (the Tower, Bridge and Network were). The animation uses standard SVG (SMIL) and CSS; reduced-motion disables it.
- Audio was not listened to; only Chromium was run (the projector uses CSS `:has()`).
- Appearance on a real projector or a very large screen; performance of the live animation on a low-end phone.
- The visual reference image and the original ZIP were not attached; the skyline and structures are original designs.
- Arabic wording should be reviewed by a native Saudi reader.
- A "part" is a vertical slice of the structure (the existing zone mechanic): with one Builder that Builder holds the whole structure; with five Builders each holds one or two columns.
