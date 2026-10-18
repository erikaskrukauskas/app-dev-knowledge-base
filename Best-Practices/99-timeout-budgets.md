---
title: Timeout budgets
tags: [practices, api]
status: candidate
updated: 2026-10-17
---

# Timeout budgets

Every outbound call has a deadline. When the deadline passes, the caller stops waiting and follows the error contract.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

A caller does not wait without a bound. See [Error contracts](09-error-contracts.md) and [Accepted work](21-accepted-work.md) when the work should continue in the background.

## Check

Force a dependency to exceed the deadline. The caller returns the timeout error and does not hang.
