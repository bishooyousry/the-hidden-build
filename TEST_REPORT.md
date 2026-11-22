# Test report: The Hidden Build · Future City

## How it was tested
- Automated end-to-end run with Playwright (Chromium), using **separate browser contexts as separate players** (trainer, Messenger, Builders, spectator) against a **mock relay** that speaks the same protocol as ntfy.sh (publish, server-sent events, replay).
- Visual checks by screenshot: entry screen (Arabic), mission control, Messenger lobby and build, classified blueprint, Builder screen (desktop and 390 px phone, Arabic), projector (build, round over, leaderboard), result and reveal.

## Verified (52 automated checks passed, 0 failed)
- Join: a 5-character session code is required; a player cannot join without a team; a trainer sees players and team readiness.
- Roles: the first player to tap becomes the Messenger; Builders see who the Messenger is; a team without a Messenger becomes spectators and can watch the result.
- Blueprint secrecy: the blueprint appears only in the Messenger's classified view (63 cells, then closes); Builders never receive it; the optional pin works only when the trainer enables it.
- Zones: Builder zones together cover all 9 columns; painting before GO is ignored; a locked team cannot change.
- Communication: team chat (collapsed by default), Messenger-to-Builders messages and Builders' quick questions are delivered; the "picture named first" keyword check works.
- Timer and rounds: the countdown runs, the time-up auto-locks and scores, END ROUND NOW works.
- Locking and scoring: a perfect build scores 100% accuracy and 1000 + a time bonus (at most 100); 3 correct and 1 stray scores as expected; no time bonus below 50% accuracy. **The scoring algorithm was not changed.**
- Leaderboard: the trainer reveals it, players and the projector show it, hide works.
- Trainer: configuration (blueprint, time, pin), team cards, debrief panel, reflection, CSV export, second session with a new code, exit button, projector progress and SHOW BUILDS.
- Language: Arabic RTL layout and result re-render; resume after refresh; works with browser storage blocked.
- Not an error: no uncaught JavaScript errors were raised in the screenshot sessions (desktop and phone).

## Functional changes made (all intentional)
1. Six new blueprints replace the original six (same 9 x 7 grid and the same five materials, so all mechanics are unchanged). The "picture named" keyword lists were rewritten for them.
2. "Bricks" are called **modules** in the interface. Team emojis and decorative icons were removed.
3. Defaults changed: Arabic is the default language and music is Off by default.
4. A small fix: the quick-question chips sent their text without the leading emoji; with the emoji removed they now send the full text.
5. The projector no longer rebuilds its content every second when nothing changed, so reveal animations play once.

## Not verified (read before a real workshop)
- **The real ntfy.sh relay and real devices.** Multiplayer was verified across separate browser sessions against a mock relay, not across separate physical devices on the real relay. The free relay can rate-limit big groups. Test with two real devices first.
- **Audio** (sound effects) was not listened to.
- **Browsers:** only Chromium was run. The projector uses the CSS `:has()` selector (supported in current Chrome, Edge, Safari and Firefox); on an older browser the dashboard may show faintly behind the projector.
- **Real projector or large screen** appearance, brightness and contrast.
- **The visual reference image** (futuristic smart city) and the original ZIP were not attached to the message. The work was based on the existing source code and the palette given earlier, so the skyline is an original design, not a match to that image.
- **Arabic wording** should be reviewed by a native Saudi reader.
- The two-device checklist in the README should be run once before the session.
