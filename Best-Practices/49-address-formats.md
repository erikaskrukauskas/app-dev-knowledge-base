---
title: Address formats
tags: [practices, i18n, contracts]
status: tested
updated: 2026-10-17
---

# Address formats

An address contract does not require one country's field order, street type, or postal-code shape for every person.

W3C Internationalization Quick Tips says: "Support local formats of names/addresses, times/dates, etc." Checked 2026-10-17 at <https://www.w3.org/International/quicktips/>.

Ask only for the parts the application actually uses. A single recipient line plus a country code is often enough. See [Country codes](36-country-codes.md) and [Internationalization](15-internationalization.md).

## Check

Store an address that has no street number and one that orders locality before the street. Both round-trip.
