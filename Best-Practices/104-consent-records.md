---
title: Consent records
tags: [practices, security, state]
status: candidate
updated: 2026-10-17
---

# Consent records

When an action needs consent, the application stores who consented, to what, and when. A missing consent record means the action is not allowed.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Consent text is versioned. A later change to the text does not rewrite the old record. See [Stored event contracts](54-stored-event-contracts.md).

## Check

Perform the action without consent and with consent. Only the consented call succeeds, and the record names the text version.
