---
title: Monotonic reads
tags: [practices, state]
status: candidate
updated: 2026-10-17
---

# Monotonic reads

After a caller has observed a version of a fact, a later read by that caller does not show an older version.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

This is a read guarantee, not a write lock. See [Read your writes](44-read-your-writes.md).

## Check

Read a fact, let a writer advance it, and read again. The second version is the same or newer, never older.
