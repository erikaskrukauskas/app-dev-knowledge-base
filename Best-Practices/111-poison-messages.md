---
title: Poison messages
tags: [practices, error, state]
status: candidate
updated: 2026-10-17
---

# Poison messages

A message that fails the contract on every attempt is parked after a stated number of tries. It does not block the rest of the stream forever.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

The failure is recorded with the message identity. See [Error contracts](09-error-contracts.md).

## Check

Inject a permanently invalid message. After the stated tries, later messages still move and the invalid one is visible as parked.
