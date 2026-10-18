---
title: Bounded staleness
tags: [practices, state]
status: candidate
updated: 2026-10-17
---

# Bounded staleness

If a read can be stale, the contract states the maximum staleness. An unbounded replica is not a current read.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Writers still follow [Read your writes](44-read-your-writes.md). Other callers may see the lag the contract allows.

## Check

Write a fact and read it from the stale path inside the bound and after a forced lag. The results match the stated bound.
