# Catch the Zoomies

[![Play Live](https://img.shields.io/badge/Play-Live_Demo-brightgreen)](https://catch-the-zoomies-riansap1.vercel.app/)
[![Powered by Squeekchain](https://img.shields.io/badge/Powered_by-Squeekchain-f5a623)](https://squeekchain.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/Riansap88/catch-the-zoomies)](https://github.com/Riansap88/catch-the-zoomies/commits/main)

A timing game powered by Squeekchain. Squeektoshi runs his wheel live — press CATCH when his speed lands inside the target zone.

## Play

Live demo: https://catch-the-zoomies-riansap1.vercel.app/

No install needed. Open the link and play in the browser, or open `index.html` locally.

## How it works

- Live wheel speed comes from Squeekchain's public status API (`https://api.squeekchain.com/v1/status`, `measurement.rpmMilli`).
- Each round shows a target RPM zone. Press CATCH while the live RPM is inside the zone to score.
- Hits near the middle of the zone score more. Streaks add bonus points. Tries and round time depend on difficulty: Easy (12 tries, 90 seconds), Normal (10 tries, 90 seconds), Hard (8 tries, 75 seconds).
- Three difficulty modes: Easy (50 RPM zone), Normal (40 RPM zone), Hard (30 RPM zone). Switch with the buttons or keys 1 / 2 / 3; your choice is saved in the browser and switching starts a fresh round.
- Sound effects, synthesized in the browser with the Web Audio API (no audio files): a chime for hits, a low buzz for misses, a jingle on level-up, and clicks for pause and round changes. Mute with the Sound button or the M key; your choice is saved in the browser.
- Share your best score: the Share button under the local leaderboard (or the S key) opens the device share sheet, or copies a ready-to-post score line to the clipboard when sharing is not available. The button stays disabled until a score is on the board.
- Every 150 points you level up and the target zone gets narrower.
- Tip: press the Space bar (or Enter) to CATCH, no mouse needed.
- Your best score is shown under the local leaderboard.
- If the live API is unreachable, the game falls back to a clearly labelled simulated wheel so it stays playable.
- Scores are kept in a local leaderboard in the browser.

## Rules

Built for Squeekchain following the rules at https://squeekchain.com/genesis/code — it is a game that uses Squeekchain's live rounds, not a read-only dashboard, landing page, or thin API wrapper.

## Run it

Static site, no build step. Open `index.html` or deploy the folder to any static host.
