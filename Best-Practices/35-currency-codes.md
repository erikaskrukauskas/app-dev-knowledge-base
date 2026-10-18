---
title: Currency codes
tags: [practices, contracts]
status: tested
updated: 2026-10-17
---

# Currency codes

A money amount names its currency with an ISO 4217 code. A bare number is not money.

ISO 4217 says: "This standard establishes internationally recognized codes for the representation of currencies that enable clarity and reduce errors." Checked 2026-10-17 at <https://www.iso.org/iso-4217-currency-codes.html>.

Alphabetic codes are three letters. The standard also defines numeric codes and, where a currency has minor units, how those units relate to the currency. See [Minor units](57-minor-units.md). Confirm the current code list before accepting a code.

## Check

Write an amount with its code and read it back. An unknown code is rejected.
