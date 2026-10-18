---
title: Preserve form input
tags: [practices, error, contracts]
status: candidate
updated: 2026-10-17
---

# Preserve form input

A failed submission shows the errors and keeps the values the person entered, except secrets.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Passwords and other secrets are cleared on purpose. See [Field errors](64-problem-details-per-field.md) and [Password storage](34-password-storage.md).

## Check

Submit an invalid form. The non-secret fields still show what was typed, and the errors name the fields.
