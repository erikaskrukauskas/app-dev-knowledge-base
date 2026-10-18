---
title: Clock skew
tags: [practices, contracts, security]
status: candidate
updated: 2026-10-17
---

# Clock skew

A check that compares timestamps from two machines allows a stated skew. Outside that window the check fails closed.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Do not accept an arbitrarily old or future timestamp as fresh. See [Date and time contracts](13-date-and-time.md).

## Check

Submit a timestamp older than the window and one inside it. Only the inside timestamp passes.
