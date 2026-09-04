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
- Account with anon public key
- Export / import JSON backups
