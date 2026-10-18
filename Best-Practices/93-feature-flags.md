---
title: Feature flags
tags: [practices, architecture]
status: candidate
updated: 2026-10-17
---

# Feature flags

Unfinished behavior is behind a flag that is off until the check passes. The off path remains the contract callers already have.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

A flag is config, not a permanent branch. Remove it after the decision. See [Config versus code](39-config-versus-code.md).

## Check

Run with the flag off and on. Off matches the previous contract. On matches the new behavior under test.
