# Charter Rush — the ScanPass game

A browser game set at a speedboat charter dock in Simpson Bay, Sint Maarten.
Run the check-in desk as the manager, or take the helm and drive the tour.
Built to show what [ScanPass](https://scanpass.pro) does: private, on-device
passport scanning that turns guests into a crew & passenger list in one tap.

Live: https://game.scanpass.pro

## Play

- **Manager** — guests queue with passports. Copy each passport into the boat's
  list (five fields by hand, typos happen) or scan it with ScanPass once
  Captain Alex suggests the app. Cast off when the list is ready.
- **Captain** — WASD / arrows (on-screen buttons on phones). Hit the five
  yellow tour markers and return to the green ring at the dock. Fast trips earn tips.
- `Tab` or the top buttons switch roles. While you drive, the dock queue keeps growing.
- The coast guard checks the list at the first stop: $150 per error.

## Stack

One static file: `index.html` (HTML + CSS + JS), Three.js r128 from cdnjs.
No build step. Open the file in a browser or serve the folder.

Game constants live at the top of the script: `PRICE`, `FINE`, `TIP`,
`PATIENCE`, `DAY`, `STOPS`, `LAND`.

## Deploy

GitHub Pages serves the `main` branch root; `CNAME` points it at
`game.scanpass.pro`. DNS: add a `CNAME` record `game → <owner>.github.io`.
