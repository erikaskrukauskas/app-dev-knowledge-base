---
title: Offline queue
tags: [practices, state]
status: candidate
updated: 2026-10-17
---

# Offline queue

Commands captured offline replay in a stated order when the connection returns, and each command is idempotent.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

A conflict with newer server state uses the conditional-update rule rather than a silent overwrite. See [Idempotent operations](10-idempotent-operations.md) and [Conditional updates](11-conditional-updates.md).

## Check

Queue two commands offline, replay them, and replay them again. The stored result matches one replay.
