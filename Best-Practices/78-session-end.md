---
title: Session end
tags: [practices, security]
status: candidate
updated: 2026-10-17
---

# Session end

Ending a session makes that session unusable. A copied cookie or token from before logout fails closed.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Logout is idempotent. See [Idempotent operations](10-idempotent-operations.md).

## Check

Authenticate, call logout, and call again with the old session. The later call is unauthorized.
