---
title: Read-only mode
tags: [practices, state, api]
status: candidate
updated: 2026-10-17
---

# Read-only mode

In read-only mode, writes are rejected with a stated error and reads still follow the read contract.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

The mode is visible to callers. It is not a timeout. See [Safe operations](19-safe-operations.md).

## Check

Enable read-only mode, attempt a write, and perform a read. The write fails and the read succeeds.
