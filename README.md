# FDA MAUDE analytics: curated data

Pre-computed monthly aggregates of U.S. FDA MAUDE medical device adverse event reports, published as static JSON for
dashboards. The files are generated weekly by a private pipeline; this repository holds only the output.

- Start with [`manifest.json`](manifest.json): schema version, when the files were generated, the newest month, and a
  SHA-256 per file.
- Files are aggregates by month. There are no individual reports, no report identifiers and no free text.

## Read this before using the numbers

- **Counts reflect reporting behavior, not true incidence.** A rise can come from media attention, litigation or a
  change in reporting rules.
- **One event can have several reports** (manufacturer, user facility, voluntary). "Reports" is not "events".
- **Recent months are incomplete and get restated.** Reports arrive over months after an event. Use the `is_mature`
  field before reading a trend.
- Months are the event month, falling back to the received month when the event date is missing
  (`scope_date_basis`).

## Sources and attribution

- FDA Manufacturer and User Facility Device Experience (MAUDE), MDR data files, U.S. Food and Drug Administration.
- openFDA device classification, 510(k) and PMA data.
- AccessGUDID, U.S. National Library of Medicine (device identifiers).

This is an independent portfolio project. It is not endorsed by, or affiliated with, the FDA or the NLM.

## License

No license is granted. Copyright 2026 Akshay Pradhan; all rights reserved. The files are published to be viewed. You
may not copy, redistribute or reuse them without written permission. This covers only the curated aggregates and
this repository; the underlying FDA, openFDA and NLM source data remain available from their original publishers
under their own terms.
