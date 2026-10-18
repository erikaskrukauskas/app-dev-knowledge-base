---
title: Cache vary
tags: [practices, api, state]
status: tested
updated: 2026-10-17
---

# Cache vary

If the representation depends on a request field, the cache key includes that field. Otherwise a later caller can receive someone else's selection.

RFC 9111 says: "the cache MUST NOT use that stored response without revalidation unless all the presented request header fields nominated by that Vary field value match those fields in the original request" Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9111>.

Name those fields in Vary. See [Content negotiation](23-content-negotiation.md) and [Response caching](17-response-caching.md).

## Check

Store a response that varies on a selection field, then request a different selection. The second caller does not receive the first selection.
