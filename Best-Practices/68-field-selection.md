---
title: Field selection
tags: [practices, api, contracts]
status: candidate
updated: 2026-10-17
---

# Field selection

If a caller can ask for a subset of fields, the contract lists the selectable fields and the shape of the reduced representation.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Omitting a field the caller did not ask for is not the same as a null value. See [Null and absent](28-null-and-absent.md).

## Check

Request a subset and the full representation. The subset contains only the requested fields, and the full one still has the others.
