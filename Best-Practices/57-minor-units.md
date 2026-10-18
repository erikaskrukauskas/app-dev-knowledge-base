---
title: Minor units
tags: [practices, contracts]
status: tested
updated: 2026-10-17
---

# Minor units

A money amount states its currency and its scale. Where the currency has minor units, the contract uses that scale instead of a binary floating-point approximation.

ISO 4217 says: "For currencies having minor units, ISO 4217:2015 also shows the relationship between the minor unit and the currency itself (i.e. whether it divides into 100 or 1000)." Checked 2026-10-17 at <https://www.iso.org/iso-4217-currency-codes.html>.

See [Currency codes](35-currency-codes.md). Currencies differ in how many minor units they have. Confirm the current ISO 4217 list before hard-coding an exponent.

## Check

Add two amounts of a currency whose minor unit is not a hundredth. The result matches decimal minor-unit arithmetic, not a binary float.
