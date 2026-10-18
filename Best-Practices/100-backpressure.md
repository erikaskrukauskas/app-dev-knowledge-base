---
title: Backpressure
tags: [practices, api, state]
status: candidate
updated: 2026-10-17
---

# Backpressure

When a consumer cannot keep up, the producer is refused or delayed. The application does not grow an unbounded queue.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

The refusal is a stated error or a retry time. See [Rate limits](25-rate-limits.md).

## Check

Fill the consumer until the bound. The next produce is refused or delayed, and the queue length stays within the bound.
