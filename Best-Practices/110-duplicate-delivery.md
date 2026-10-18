---
title: Duplicate delivery
tags: [practices, state, api]
status: candidate
updated: 2026-10-17
---

# Duplicate delivery

A consumer treats duplicate delivery as normal. The message identity is stable, and applying the message twice matches applying it once.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

See [Exactly-once claims](52-exactly-once-claims.md).

## Check

Deliver one message twice. The resulting state matches a single delivery.
