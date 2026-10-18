---
title: Default deny
tags: [practices, security]
status: candidate
updated: 2026-10-17
---

# Default deny

If no authorization rule allows an action, the action is denied. A missing rule is not an allow.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

New actions are unreachable until a rule names them. See [Application security](06-application-security.md).

## Check

Call an action with no allow rule. The call is forbidden.
