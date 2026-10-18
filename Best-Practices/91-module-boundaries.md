---
title: Module boundaries
tags: [practices, architecture]
status: candidate
updated: 2026-10-17
---

# Module boundaries

A module does not read or write another module's stored facts except through that module's contract.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

The contract is the calls or events the owning module publishes. See [Single writer](45-single-writer.md).

## Check

Trace a change to a fact. The write goes through the owning module's contract.
