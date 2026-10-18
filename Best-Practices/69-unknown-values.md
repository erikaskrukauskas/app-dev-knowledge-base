---
title: Unknown values
tags: [practices, api, contracts]
status: candidate
updated: 2026-10-17
---

# Unknown values

A reader states whether an unknown enum value, field, or event version is rejected or ignored.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Ignoring unknown fields is what lets a writer add a compatible field. Rejecting unknown required discriminators stops a silent misread. See [API compatibility](12-api-compatibility.md).

## Check

Send a value the current reader does not know. It follows the published ignore or reject rule.
