---
title: Command versus query
tags: [practices, architecture, api]
status: candidate
updated: 2026-10-17
---

# Command versus query

A command changes state or explicitly refuses to. A query does not. A single operation does not pretend to be both.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

See [Safe operations](19-safe-operations.md). A query that must start work is a command with a result, and the contract says so.

## Check

Call the query and confirm state is unchanged. Call the command and confirm the stated change.
