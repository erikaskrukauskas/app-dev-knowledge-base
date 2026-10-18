---
title: Backfill
tags: [practices, state]
status: candidate
updated: 2026-10-17
---

# Backfill

A new required fact is backfilled on existing records before any reader treats it as required.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

The backfill is idempotent and visible as progress. See [Expand then contract](55-expand-then-contract.md).

## Check

Read an old record after the backfill. The new fact is present, and running the backfill again does not duplicate it.
