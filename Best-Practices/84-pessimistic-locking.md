---
title: Pessimistic locking
tags: [practices, state]
status: candidate
updated: 2026-10-17
---

# Pessimistic locking

If the application locks a fact for editing, the lock has an owner and an expiry. A crashed holder does not lock the fact forever.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

This is different from a conditional write. See [Conditional updates](11-conditional-updates.md).

## Check

Take a lock, let it expire, and take it as another caller. The second caller acquires it only after expiry or release.
