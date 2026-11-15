# BestOf

A personal app for logging the best wrestling matches and segments of the year while watching, then turning them into end-of-year awards: Wrestler, Match, Segment, Promotion and Show of the Year.

Everything is in a single file, `index.html`, with no build step. Open it in a browser or serve it with GitHub Pages.

## Features

- **Log it:** quick entry for matches or segments. Wrestler names are suggested as you type, promotions come from a dropdown (AEW, WWE, NJPW, AAA, then the rest, plus Other…), the show and date are remembered, and a heart marks of-the-year contenders.
- **List:** every entry for the selected year, with search, filters and sorting.
- **Stats:** headline counts, a Wrestler of the Year podium, Match and Segment of the Year shortlists, Promotion and Show of the Year, and a month-by-month chart. "Copy as text" gives you a list ready to paste.
- **Years:** a summary card for each year, all-time leaders, bulk import, and a JSON backup.

## Where data is saved

- **Claude artifact version:** entries sync to the owner's Claude account.
- **Anywhere else** (GitHub Pages, a local file): entries are saved in that browser's local storage. Use **Years → Copy backup (JSON)** and **Import** to move entries between places.

## Importing past years

Paste one entry per line, with columns separated by tabs or `|`:

```
date | promotion | show | who | type | notes
2025-01-04 | NJPW | Wrestle Kingdom 19 | Zack Sabre Jr. vs. Shota Umino
```
