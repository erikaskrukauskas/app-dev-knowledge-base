---
title: Impersonation
tags: [practices, security]
status: candidate
updated: 2026-10-17
---

# Impersonation

If an operator can act as another user, the application records both identities and shows that the action was impersonated.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

The operator's own permissions must allow impersonation. The target user's permissions bound the action. See [Audit actor](63-audit-actor.md).

## Check

Impersonate and perform a write. The audit shows the operator and the target, and an operator without the right is refused.
