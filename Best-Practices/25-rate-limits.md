---
title: Rate limits
tags: [practices, api, security]
status: tested
updated: 2026-10-17
---

# Rate limits

When the application refuses work because the caller is too fast, the refusal is a rate limit, not a failure of the fact and not a permission denial.

RFC 6585 says: "The 429 status code indicates that the user has sent too many requests in a given amount of time ("rate limiting")." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc6585>.

Say the window and the limit the caller can rely on. A rate-limit response should say when to try again. Do not cache it as a successful representation. See [Credential guessing](46-credential-guessing.md) for guesses of a secret.

## Check

Exceed the published limit. The next call is refused, state is unchanged, and a later call inside the rules succeeds.
