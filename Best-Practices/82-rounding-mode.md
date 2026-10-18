---
title: Rounding mode
tags: [practices, contracts]
status: candidate
updated: 2026-10-17
---

# Rounding mode

When the application rounds, the contract names the mode and the scale. Callers can reproduce the result.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Do not change the mode for existing stored values without a version. See [API compatibility](12-api-compatibility.md) and [Minor units](57-minor-units.md).

## Check

Round a halfway value under the published mode. The stored result matches that mode.
