---
title: Account enumeration
tags: [practices, security]
status: candidate
updated: 2026-10-17
---

# Account enumeration

Authentication and account-recovery responses do not reveal whether an identifier is registered. Both existing and missing accounts take the same observable path.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Timing and wording match closely enough that the difference is not the signal. See [Credential guessing](46-credential-guessing.md).

## Check

Request recovery for a known account and an unknown one. The observable response matches.
