---
title: Cancellation
tags: [practices, api, state]
status: candidate
updated: 2026-10-17
---

# Cancellation

If accepted work can be cancelled, the contract says which states allow cancel and what a late cancel returns.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Cancel is idempotent after the work is already cancelled or finished. See [Accepted work](21-accepted-work.md).

## Check

Cancel in-progress work and cancel it again. The work stops once, and the second cancel returns the same outcome.
