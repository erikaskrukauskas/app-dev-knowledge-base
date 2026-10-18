---
title: Creation results
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Creation results

When a command creates a resource, the success result includes the new resource's identifier. The caller must not guess the URI or the id.

RFC 9110 says: "If one or more resources has been created on the origin server as a result of successfully processing a POST request, the origin server SHOULD send a 201 (Created) response containing a Location header field that provides an identifier for the primary resource created" Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

On HTTP, that identifier is a Location value on a 201 response. The body may describe status, and it points at the new resource rather than replacing the identifier. See [Stable identifiers](14-stable-identifiers.md).

## Check

Create one resource and follow the returned identifier. A second lookup with that identifier returns the created fact.
