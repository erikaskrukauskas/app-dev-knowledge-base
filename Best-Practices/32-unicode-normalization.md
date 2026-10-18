---
title: Unicode normalization
tags: [practices, i18n, contracts]
status: tested
updated: 2026-10-17
---

# Unicode normalization

Text that the contract treats as the same is stored and compared in one stated normalization form. Two different byte sequences that the Unicode standard calls equivalent must not become two records.

UAX #15 says: "When implementations keep strings in a normalized form, they can be assured that equivalent strings have a unique binary representation." Checked 2026-10-17 at <https://www.unicode.org/reports/tr15/>.

Name the form. Do not normalize only sometimes. Confirm the current annex before relying on a form's exact mapping.

## Check

Submit the same user-perceived text in two equivalent Unicode sequences. One record exists, and a lookup with either sequence finds it.
