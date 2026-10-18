---
title: Correlation identifiers
tags: [practices, api]
status: candidate
updated: 2026-10-17
---

# Correlation identifiers

A call can carry a correlation identifier that the application returns and writes on related logs. The identifier is not a secret and not an authorization.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

If the caller omits it, the application may assign one and return it. See [Audit actor](63-audit-actor.md).

## Check

Send a correlation id, force an error, and find that same id on the response and the diagnostic.
