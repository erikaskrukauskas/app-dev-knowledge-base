---
title: Safe operations
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Safe operations

A read must not change stored state. The caller does not expect a query, a preview, or a lookup to create, update, or delete a fact.

RFC 9110 says: "Request methods are considered "safe" if their defined semantics are essentially read-only; i.e., the client does not request, and does not expect, any state change on the origin server as a result of applying a safe method to a target resource." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

Logging the read or refreshing a cache is not a change to the caller's fact. A control that looks like navigation but submits a command is not a safe operation. Name the safe operations in the contract. See [Idempotent operations](10-idempotent-operations.md) for commands that may be retried.

## Check

Call the read twice. Stored business state is unchanged, and the two results describe the same fact unless a writer changed it between them.
