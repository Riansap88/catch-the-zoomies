# Catch the Zoomies

A timing game powered by Squeekchain. Squeektoshi runs his wheel live — press CATCH when his speed lands inside the target zone.

## How it works

- Live wheel speed comes from Squeekchain's public status API (`https://api.squeekchain.com/v1/status`, `measurement.rpmMilli`).
- Each round shows a target RPM zone. Press CATCH while the live RPM is inside the zone to score.
- Hits near the middle of the zone score more. Streaks add bonus points. 10 tries per round, 90 seconds per round.
- Every 150 points you level up and the target zone gets narrower.
- If the live API is unreachable, the game falls back to a clearly labelled simulated wheel so it stays playable.
- Scores are kept in a local leaderboard in the browser.

## Rules

Built for Squeekchain following the rules at https://squeekchain.com/genesis/code — it is a game that uses Squeekchain's live rounds, not a read-only dashboard, landing page, or thin API wrapper.

## Run it

Static site, no build step. Open `index.html` or deploy the folder to any static host.
