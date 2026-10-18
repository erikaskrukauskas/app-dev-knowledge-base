---
title: Notification versus state
tags: [practices, state, architecture]
status: candidate
updated: 2026-10-17
---

# Notification versus state

A notification tells a consumer that state may have changed. The consumer reads the current state. The notification payload is not the authority.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Lost or repeated notifications are safe because the read is the authority. See [Derived representations](43-derived-representations.md).

## Check

Emit a notification, change the fact again, and let the consumer read. The consumer sees the current fact, not a stale payload.
