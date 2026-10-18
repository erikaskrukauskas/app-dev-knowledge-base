---
title: Sensitive response storage
tags: [practices, security, api]
status: tested
updated: 2026-10-17
---

# Sensitive response storage

A response that carries a secret, a credential, or a one-time value is not stored by a cache. Say so on the response.

RFC 9111 says: "The no-store request directive indicates that a cache MUST NOT store any part of either this request or any response to it." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9111>.

Private caching is not enough when the value must not be written to storage at all. See [Response caching](17-response-caching.md).

## Check

Fetch a one-time secret twice from a cache in between. The second fetch does not replay the secret from cache.
