---
title: Permission cache
tags: [practices, security, state]
status: candidate
updated: 2026-10-17
---

# Permission cache

A cached authorization decision has a maximum age. A revocation or a role change is visible by the end of that age.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

An unbounded permission cache is not revocation. See [Revocation](106-revocation.md) and [Response caching](17-response-caching.md).

## Check

Remove a permission and call again after the cache age. The call is forbidden.
