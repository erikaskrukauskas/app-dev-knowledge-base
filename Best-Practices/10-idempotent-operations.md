---
title: Idempotent operations
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Idempotent operations

A command the caller may retry must have the same intended effect the second time as the first.

RFC 9110 says: "A request method is considered "idempotent" if the intended effect on the server of multiple identical requests with that method is the same as the effect for a single such request." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

## When a retry is possible

The caller can miss the response and not know whether the command was applied. If repeating the command would create a second charge, a second record, or a second message, the operation is not safe to retry as written.

Give that command an idempotent form: the same identity resolves to the same result, or a key the caller sends so the application can recognize the repeat. Logging the attempt is not a second business effect. The RFC allows a server to log each idempotent request separately.

A caller should not automatically retry a command whose repeat would apply a second effect, unless it can tell that the first attempt never landed.

## Check

Send the same command twice. The stored outcome matches one success, and the second response points at that outcome rather than a new one. A conflict or a replay uses the [error contract](09-error-contracts.md).
