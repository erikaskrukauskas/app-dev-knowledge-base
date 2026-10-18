---
title: Exactly-once claims
tags: [practices, api, state]
status: tested
updated: 2026-10-17
---

# Exactly-once claims

Do not promise that a message is delivered exactly once. Promise that applying it more than once has the same intended effect as applying it once, or that duplicates are detected.

RFC 9110 says: "A request method is considered "idempotent" if the intended effect on the server of multiple identical requests with that method is the same as the effect for a single such request." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

A retry exists because the first response can be lost. That is at least once. The idempotent effect is what makes the retry safe.

## Check

Deliver the same message twice. The stored fact matches one application of the message.
