---
title: Partial responses
tags: [practices, api]
status: tested
updated: 2026-10-17
---

# Partial responses

A partial response is a slice of one representation, not a second contract. Say whether ranges are supported. If they are not, reject the range instead of returning a whole body with a success code that claims a part.

RFC 9110 says: "A client can alter the semantics of GET to be a "range request", requesting transfer of only some part(s) of the selected representation, by sending a Range header field in the request" Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

A 206 body is the requested part. A range the application cannot satisfy is an error, not a silent full download. This is not [Paging collections](16-paging-collections.md), which pages records rather than bytes.

## Check

Request a middle range of a known representation and compare those bytes to the full representation.
