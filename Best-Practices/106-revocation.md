---
title: Revocation
tags: [practices, security]
status: candidate
updated: 2026-10-17
---

# Revocation

A revoked credential fails even if its expiry is still in the future. The application has a way to observe the revocation.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

How fast revocation is visible is part of the contract. An unbounded delay is not revocation. See [Session end](78-session-end.md).

## Check

Revoke a credential and call with it. The call is refused before the original expiry.
