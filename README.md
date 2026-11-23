# Everdell Scorer

A single-page score calculator for the end of a game of **Everdell** (base game only). Built for use on a phone at the table.

**Live:** https://david-saeteros.github.io/everdell-scorer/

## What it counts

For each player (up to 4):

| Category | How it's entered |
|---|---|
| Printed card points | Sum of the point values on every card in the city |
| Point tokens | Count of 1- and 3-point tokens (as points) |
| Journey | Sum of Journey points (2 shared · 3 · 4 · 5) |
| Basic Events | Count achieved, 3 points each |
| Special Events | Count achieved + total printed points |
| Prosperity bonuses | Tick the purple cards in the city; bonuses are calculated |
| Leftover resources | Twigs, resin, pebbles, berries (Architect + tiebreak) |

### Prosperity bonuses

- **Architect** – +1 per leftover resin and pebble (max 6)
- **Castle** – +1 per Common Construction
- **Ever Tree** – +1 per purple Prosperity card (incl. itself), counted from the ticked cards
- **King** – +1 per Basic Event, +2 per Special Event
- **Palace** – +1 per Unique Construction (incl. itself)
- **School** – +1 per Common Critter
- **Theatre** – +1 per Unique Critter
- **Gatherer** – +3 per Gatherer paired with a Harvester

A purple card's printed points still go in "Printed card points"; the tick only adds its bonus.

### Tiebreak

Most events achieved, then most leftover resources.

## Game log

- **Save game** stores the result in a log on the page.
- **Export CSV** downloads the whole log.
- **New game** clears scores but keeps player names.

All data is stored in the browser's `localStorage`, so it stays on that device and browser only.

## Running it

It's one static file (`index.html`) with no build step. Open it locally, or serve it with GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).
