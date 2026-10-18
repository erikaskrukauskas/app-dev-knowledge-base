---
title: Loading states
tags: [practices, contracts]
status: candidate
updated: 2026-10-17
---

# Loading states

While a result is loading, the interface says it is loading and does not present stale data as the final result unless the contract allows a stale view.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

A load failure uses the error path, not an endless loading state. See [Empty states](89-empty-states.md).

## Check

Slow the read and observe the loading state, then the result. A failed read leaves the loading state.
