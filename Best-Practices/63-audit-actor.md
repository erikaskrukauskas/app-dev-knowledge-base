---
title: Audit actor
tags: [practices, security, state]
status: tested
updated: 2026-10-17
---

# Audit actor

A privileged write records the authenticated actor's identifier and the time. The display name is not the record of who did it.

NIST SP 800-63B says: "The authentication process results in an identifier that uniquely identifies the subscriber each time they authenticate to that RP." Checked 2026-10-17 at <https://pages.nist.gov/800-63-4/sp800-63b.html>.

NIST says authentication yields an identifier for the subscriber. That identifier is what the audit stores. See [Stable identifiers](14-stable-identifiers.md) and [Date and time contracts](13-date-and-time.md).

## Check

Perform a privileged write and read the audit. The actor identifier matches the authenticated caller and does not change when the display name changes.
