---
title: Personal data deletion
tags: [practices, security, state]
status: candidate
updated: 2026-10-17
---

# Personal data deletion

A deletion request removes or irreversibly anonymizes the personal data the application holds for that person, except data the contract says is retained for a named reason.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Retained data has a reason and a limit. The identifier is not given to a new person. See [Identifier reuse](56-identifier-reuse.md).

## Check

Delete a person and search ordinary reads and exports. The personal payload is gone, and the audit does not contain the payload.
