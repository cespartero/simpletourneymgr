# Up Down Tournament Manager

A single-page app for running a **court up-and-down doubles tournament** for pickleball (or any doubles court game) on a club night. It is one self-contained HTML file and needs no server, internet connection or sign-in.

## How an up-and-down tournament works

- Players add their names to the queue. When everyone is in, the admin starts the tournament and entries close.
- Players go onto courts in queue order, starting from court 1. Each court needs 4 players. If the numbers don't divide evenly, the leftover players sit out that round.
- Every round starts and ends together.
- **Winners move one court toward court 1. Losers move one court away.**
- Partners change every round. Nobody partners the same person they played with in their previous game.
- If a game finishes level, the admin chooses which team moves up, and both teams record a draw.
- The board calls out players who have stayed on court 1 for several rounds in a row.

## Features

- **Set up the tournament from the board**: once admin is unlocked, the Setup tournament card on the Board shows the options and a Start tournament button.
- **Player List**: players join by typing their name. The admin can reorder by dragging, mark someone as sitting out (they keep their place) or remove them before the tournament starts, and re-add everyone from the last session in one tap.
- **Planned rounds**: choose how many rounds to play when starting (suggested numbers keep games level). The board shows "Round 3 of 8" and asks before going past the plan.
- **Untimed or timed rounds**: untimed rounds end when every court has a result. Timed rounds run for a set time (minutes and seconds) after a 10 second setup, with beeps and a spoken countdown. The round time can be changed between rounds.
- **Pause, resume and end round** controls for the admin. Ending a round early asks for the winning team on each court.
- **Full screen timer**: switch the board to just the round timer, for a TV or big screen.
- **Shuffle courts**: randomise courts and partners for the coming round.
- **Score entry**: enter both scores per court; the higher score wins.
- **Page tabs**, styled like the Round Robin Tournament Manager: Board, Standings (including average points per game and streaks), Courts (every court in your court layout, with team names) and Match history, plus a copyable results summary.
- **Help** built into the app, opened from the header or footer.
- **Court layout**: arrange the court tiles to match the venue.
- **Undo** for the last action.

## Admin

Admin actions (starting and ending a session, removing players, resets, admin tools) are protected by an **admin PIN**. You choose the PIN the first time you use an admin action. Admin unlocks for 30 minutes, then locks again automatically.

Admin tools include:

- Change PIN
- Add test players (for trying the app out)
- Arrange courts
- Download backup / Restore backup (JSON file)
- Start new session
- Full reset (type `RESET` to confirm)

## Running it

**Online:** open the GitHub Pages site for this repo (served from `index.html`).

**Offline:** download `index.html` and open it in a browser. Everything, including fonts, is embedded in the file.

## Where data is stored

All data is kept in the browser's own storage (`localStorage`) on the device running the board. Nothing is sent anywhere.

- Tabs open in the same browser stay in sync.
- Other devices do **not** share the board; each device has its own copy.
- Clearing browser data clears the board. Use **Download backup** in the admin tools to keep a copy, and **Restore backup** to load it again.

## Project structure

```
index.html   The whole app: markup, styles, scripts and embedded fonts
help.html    Standalone copy of the help guide
README.md    This file
```

## Related

This app is the up-and-down tournament mode of **Court Manager**, packaged on its own as a simpler tool.
