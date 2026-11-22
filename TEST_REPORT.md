# Test report: The Hidden Build · Executive Mission

## How it was tested
Automated end-to-end run with Playwright (Chromium) using separate browser contexts as separate players (trainer, Messenger, Builders, spectator) against a mock relay that speaks the same protocol as ntfy.sh. Visual checks by screenshot: entry screen, mission control, blueprint view with the pin button, builder screen with the new materials, final reveal with "STRUCTURE ONLINE", and the earlier projector and mobile checks of the same design system.

## Verified (52 automated checks passed, 0 failed)
Join with a 5-character code and a team; roles and Messenger claim; the blueprint reaches only the Messenger (63 cells, closes); Builder zones cover all 9 columns; painting before GO is ignored; chat and quick questions; timer, time-up auto-lock, END ROUND NOW; locking and scoring (perfect build 100% and 1000 + bonus; 3 right + 1 stray scored correctly; no bonus below 50%); leaderboard reveal on players and projector; trainer dashboard, debrief panel, CSV, second session, exit; Arabic RTL; resume; storage blocked; the Messenger pin now On by default and working. **The scoring algorithm was not changed.**

## Changes made in this version
1. Blueprints are now Strategy Tower, Execution Bridge, KPI Dashboard, Team Network, Customer Journey and Leadership Hub (same 9 x 7 grid and the same five materials).
2. The five colours render as structural components (glass, steel, energy line, power core, actuator).
3. The Messenger pin is **On by default** (was Off); the trainer can switch it in the console.
4. Result headlines: Structure online / Structure stable / Partial activation / Rebuild required; a perfect build glows.
5. Earlier in this series: Arabic default, music Off by default, emojis removed, quick-chip fix, projector re-render fix.

## Not verified
- The real ntfy.sh relay and real devices: multiplayer was verified across separate browser sessions against a mock relay. Test with two real devices before the workshop.
- Audio was not listened to; only Chromium was run (the projector uses CSS `:has()`).
- Appearance on a real projector or a very large screen.
- The visual reference image and the original ZIP were not attached to the message; the skyline is an original design.
- Arabic wording should be reviewed by a native Saudi reader.
- The verbal difficulty of "Customer Journey" (a winding path) is higher than the others: try it in a dry run before using it for senior groups.
