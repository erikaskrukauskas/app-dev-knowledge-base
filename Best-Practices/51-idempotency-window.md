---
title: Idempotency window
tags: [practices, api, state]
status: tested
updated: 2026-10-17
---

# Idempotency window

If the application recognizes a retry by a key, it keeps the first result at least as long as a caller is allowed to retry. After that window, a reuse is a new command or a stated rejection, not a silent second effect.

RFC 9110 says: "A request method is considered "idempotent" if the intended effect on the server of multiple identical requests with that method is the same as the effect for a single such request." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

See [Idempotent operations](10-idempotent-operations.md). The window is part of the contract.

## Check

Complete a command, retry inside the window, and retry after the window. The inside retry returns the first result. The late call follows the published rule.
