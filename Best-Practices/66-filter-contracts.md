---
title: Filter contracts
tags: [practices, api, contracts]
status: candidate
updated: 2026-10-17
---

# Filter contracts

A filter is part of the contract: the field, the operator, and what an unknown filter does.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Unknown filters are rejected, not ignored, unless the contract says unknown filters are ignored. Combining filters has a stated meaning, usually conjunction.

## Check

Request an unknown filter and a known filter. The unknown one fails as specified, and the known one returns only matching items.
