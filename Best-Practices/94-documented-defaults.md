---
title: Documented defaults
tags: [practices, contracts]
status: candidate
updated: 2026-10-17
---

# Documented defaults

A default is part of the contract. Changing a default that callers already rely on is a compatibility change.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Say the default in the specification. See [API compatibility](12-api-compatibility.md).

## Check

Omit the field and read the stored or returned value. It equals the documented default.
