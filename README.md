# BestOf

A personal app for logging the best wrestling matches and segments of the year while watching, then turning them into end-of-year awards: Wrestler, Match, Segment, Promotion and Show of the Year.

The app is a single file, `index.html`, with no build step, plus its icons (`icons/`) and `manifest.webmanifest`. Open it in a browser or serve it with GitHub Pages. On a phone, use **Add to Home Screen** to install it with its own icon, full-screen.

## Features

- **Log it:** quick entry for matches or segments. Wrestler names are suggested as you type, promotions come from a dropdown (AEW, WWE, NJPW, AAA, then the rest, plus Other…), the show and date are remembered, and a heart marks of-the-year contenders.
- **List:** every entry for the selected year, with search, filters and sorting.
- **Stats:** headline counts, a Wrestler of the Year podium, Match and Segment of the Year shortlists, Promotion and Show of the Year, and a month-by-month chart. "Copy as text" gives you a list ready to paste.
- **Years:** a summary card for each year, all-time leaders, backup & restore, and bulk import.

## Where data is saved

- **Claude artifact version:** entries sync to the owner's Claude account.
- **Anywhere else** (GitHub Pages, a local file): entries are saved in that browser's local storage. The app asks the browser to keep that storage, but browsers can still clear it, so keep backup files.

## Backup & restore (Years tab)

- **Save backup file** downloads `best-of-backup-YYYY-MM-DD.json` (on a phone it opens the share sheet, so you can pick *Save to Files*). **Copy backup** puts the same JSON on the clipboard.
- The panel shows when you last backed up and how many entries have been added or edited since.
- **Restore from file** previews the backup before changing anything: how many entries are new, updated, already here, or newer on this device. Then choose:
  - **Add** — merge the new and changed entries into your list (nothing is deleted).
  - **Replace my list with this** — make your list match the backup exactly (asks for a second tap).
- Every restore or import can be undone, from the toast or the *Undo it* link under the panel.
- Pasted lines that are already in your list (same date, who and show) are skipped, so importing the same sheet twice won't create duplicates.

## Importing past years

Paste one entry per line, with columns separated by tabs or `|`:

```
date | promotion | show | who | type | notes
2025-01-04 | NJPW | Wrestle Kingdom 19 | Zack Sabre Jr. vs. Shota Umino
```
