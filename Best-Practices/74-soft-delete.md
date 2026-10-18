---
title: Soft delete
tags: [practices, state, api]
status: candidate
updated: 2026-10-17
---

# Soft delete

A soft delete hides a fact from ordinary reads and keeps its identifier reserved. A later create does not reuse that identifier.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Say whether an administrator can still read it, and whether undelete exists. See [Identifier reuse](56-identifier-reuse.md).

## Check

Soft-delete a fact, list the collection, and create a replacement. The list omits the old fact, and the old identifier does not return the new one.
