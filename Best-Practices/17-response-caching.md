---
title: Response caching
tags: [practices, api, state]
status: tested
updated: 2026-10-17
---

# Response caching

Say which responses may be reused, for how long, and by whom. A response that depends on who the caller is must not be reused for someone else.

RFC 9111 says: "The unqualified private response directive indicates that a shared cache MUST NOT store the response (i.e., the response is intended for a single user)." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9111>. The same specification says a shared cache must not use a cached response to an authorized request for a later request unless the response explicitly allows that reuse.

## What may be stored

A shared cache serves more than one user. A private cache serves one. Personalized content, including a response that used the caller's identity or permission, is private unless you have named a shared representation that is safe for every recipient.

State the freshness lifetime. When the underlying fact changes, the cached read is stale. A writer and a cache that can overwrite each other need a validator. See [Conditional updates](11-conditional-updates.md).

Caching is not a substitute for authorization. See [Application security](06-application-security.md). Confirm the current caching specification before relying on a directive name.

## Check

Two different callers request a personalized resource. The second does not receive the first caller's representation. A response you marked reusable is still the same fact until its stated lifetime ends or the fact changes.
