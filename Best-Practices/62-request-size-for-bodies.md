---
title: Body size limits
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Body size limits

The contract states a maximum length for each text field and for the whole body. Input over the maximum is rejected and is not truncated into a stored value.

RFC 6585 says: "The 431 status code indicates that the server is unwilling to process the request because its header fields are too large." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc6585>.

RFC 6585 gives 431 for header fields that are too large. Apply the same refusal to a body or a field the contract bounds. See [Oversized requests](26-oversized-requests.md).

## Check

Send a field one unit over the maximum. The call fails and the previous value remains.
