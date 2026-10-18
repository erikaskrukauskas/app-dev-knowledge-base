---
title: Token audience
tags: [practices, security]
status: candidate
updated: 2026-10-17
---

# Token audience

A token is accepted only when its audience is this application. A token minted for another audience is rejected.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Expiry is checked. An expired token fails closed. See [Application security](06-application-security.md).

## Check

Present a token for another audience and an expired token. Both are rejected.
