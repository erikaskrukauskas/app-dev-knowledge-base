---
title: Receipt immutability
tags: [practices, state, contracts]
status: candidate
updated: 2026-10-17
---

# Receipt immutability

A receipt, invoice, or other issued record is not edited in place. A correction is a new record that points at the original.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

The original remains readable. See [Audit actor](63-audit-actor.md).

## Check

Issue a receipt and attempt to change its total. The original total remains, and the correction is a separate record.
