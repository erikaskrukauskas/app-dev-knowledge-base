---
title: Dependency direction
tags: [practices, architecture]
status: candidate
updated: 2026-10-17
---

# Dependency direction

A module depends on a contract that is more stable than it is. A stable contract does not depend on a caller's private types.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Cycles that force every module to change together are a design defect. See [Compare before choosing](03-compare-before-choosing.md).

## Check

Inspect the dependency edges of a change. The new edge points at a published contract, not at another module's private store.
