---
title: Sequence gaps
tags: [practices, state]
status: candidate
updated: 2026-10-17
---

# Sequence gaps

An ordered stream that promises contiguous sequence numbers treats a gap as a missing record, not as a license to skip.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

The consumer waits, retries, or raises a stated error. It does not invent the missing item. See [Poison messages](111-poison-messages.md).

## Check

Deliver sequence 1 and 3. The consumer does not apply 3 as if 2 had arrived.
