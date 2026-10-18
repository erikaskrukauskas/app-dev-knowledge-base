---
title: Country codes
tags: [practices, contracts]
status: tested
updated: 2026-10-17
---

# Country codes

A country in a contract is an ISO 3166 code, not a display name and not a flag.

ISO 4217 says: "The alphabetic code is based on another ISO standard, ISO 3166, which lists the codes for country names." Checked 2026-10-17 at <https://www.iso.org/iso-4217-currency-codes.html>.

Display names are localized text. See [Internationalization](15-internationalization.md). The ISO 4217 overview points at ISO 3166 as the country-name codes behind currency letters. Confirm the current ISO 3166 list before accepting a code.

## Check

Store a country code and a localized name. The identity that round-trips is the code.
