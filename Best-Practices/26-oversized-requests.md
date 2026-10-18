---
title: Oversized requests
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Oversized requests

Publish the maximum size the application will accept for a header, a body, or an upload. Over the maximum, reject the request and do not apply a prefix of it.

RFC 6585 says: "The 431 status code indicates that the server is unwilling to process the request because its header fields are too large." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc6585>.

HTTP uses 431 when header fields are too large. A body limit uses the error contract with the same idea: the caller can shrink the request and resend. See [Error contracts](09-error-contracts.md).

## Check

Send one request over the published maximum. It is rejected and no partial fact is stored.
