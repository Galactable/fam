# FAM — Financial Allocation Monitor

A single-file budget tracker for **weekly** income. Instead of calendar months,
it works in rolling cycles of N paychecks, generated from one anchor payday.

## Why cycles instead of months

Weekly pay doesn't divide into months — some months have four paydays, some
have five. Anchoring to a payday and working in fixed cycles removes that
problem entirely, and lets a bill be split across several checks so no single
paycheck gets wiped out by rent.

## Features

- Rolling pay cycles generated from one anchor date; navigate forward and back
- Split any expense across any combination of checks (evenly, one check, or custom)
- Per-slice paid toggles, scoped to the cycle
- Due-date vs funding-date comparison, flagging bills funded late
- Frequencies: every cycle, once a year, one time only — with optional
  set-aside so a yearly bill doesn't land as a lump
- Warns rather than silently dropping anything assigned outside the cycle
- Export / import JSON backups

## Data

Everything is stored in this browser's `localStorage` under `fam_state_v3`.
Nothing is transmitted anywhere; there are no network requests of any kind.

**Storage is tied to the origin (domain), not the path.** Changing the URL
makes existing data unreachable. Export before any domain change.

**Never commit your exported backups** — they contain real financial data.
`.gitignore` covers the default filenames.

## Deploying

Static files only, no build step. Push to a repo and enable GitHub Pages,
or drag the folder onto any static host.
