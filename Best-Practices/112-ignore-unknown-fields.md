---
title: Ignore unknown fields
tags: [practices, api, contracts]
status: candidate
updated: 2026-10-17
---

# Ignore unknown fields

Unless the contract says otherwise, a reader ignores object fields it does not know so a writer can add a compatible field.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Unknown enum values and unknown required discriminators are a different rule. See [Unknown values](69-unknown-values.md) and [API compatibility](12-api-compatibility.md).

## Check

Add a new field and read with an old reader. The old reader still returns the fields it knows.
