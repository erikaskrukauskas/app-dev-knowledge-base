---
title: Case sensitivity
tags: [practices, api, contracts]
status: candidate
updated: 2026-10-17
---

# Case sensitivity

The contract says whether case matters for identifiers, codes, and search. It does not depend on a database default.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

If comparison is case-insensitive, state the case-folding rules and the normalization form. See [Unicode normalization](32-unicode-normalization.md).

## Check

Store a value and look it up with different case. The result matches the contract in both directions.
