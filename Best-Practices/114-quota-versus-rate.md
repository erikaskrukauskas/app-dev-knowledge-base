---
title: Quota versus rate
tags: [practices, api]
status: candidate
updated: 2026-10-17
---

# Quota versus rate

A quota bounds how many resources a caller may hold. A rate bounds how fast they may call. Hitting one does not use the other's error.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

See [Rate limits](25-rate-limits.md). Both refusals leave state unchanged except for the call that was allowed.

## Check

Exhaust the quota and, separately, the rate. The errors differ, and only the allowed calls create resources.
