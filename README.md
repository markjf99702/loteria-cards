# loteria-cards

Cards for playing lotería — a single-page digital tabla board that runs entirely in the browser.

`index.html` is the whole app: no build step, no dependencies, no server required. The 54 card
images live alongside it at the repository root.

## Running it

Open `index.html` in a browser, or serve the folder locally:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

The layout is built for a tablet — four 4×4 tablas fill one screen, so a group can
play off a single shared device.

## Playing

- **Tap a card** to mark it. Marking is by card, not by cell: tapping *La Sirena* marks her on
  every board at once, which is what lets one screen serve four players.
- **CLEAR** removes all markers and starts a new round. Your board layouts are kept.
- Each board has one **double spot** — a single card printed in two cells. This is
  intentional (house rule: one double per board), so marking that card fills both of its
  cells at once and gives that board a small head start.
- A winning board gets a green glow, and a **"Buenas!"** banner appears for a few seconds.

## Win modes

Open the **MODE** menu to pick how a win is scored:

| Mode | Wins when |
| --- | --- |
| Siete Loco *(default)* | Any 7 cards on a board are marked |
| Classic | Any full row, column, diagonal, the 4 corners, or any 2×2 block |
| The "L" | Left column plus the bottom row |
| Rails | The two middle rows |
| Escalera | The two middle columns |
| Small Square | The middle 2×2 block |
| 4 Corners | The four corner cells |
| The "X" | Both diagonals |
| The "O" | The full perimeter |
| Blackout | All 16 cells |

Picking any of the shaped patterns turns on a guide: cells outside the pattern are dimmed so
players can see the target at a glance.

## Customizing boards

Press **EDIT**, tap any cell, and choose a replacement from the full 54-card library. Press
**EDIT** again to leave edit mode.

The four default tablas each carry one double spot; editing over it removes that board's
double, so re-add a duplicate if you want to keep the house rule.

The ⚙️ panel sets the marker color and offers **RESET BOARDS**, which restores the four default
tablas.

Board layouts and marker color persist in browser `localStorage` under the keys
`loteria-images` and `loteria-color`, so they survive a reload but are per-browser and not
shared between devices.
