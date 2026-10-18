---
title: Content negotiation
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Content negotiation

When one resource has more than one representation, the contract says which request fields select it. Callers that send the same selection get the same representation.

RFC 9110 says: "An algorithm, usually based on content negotiation (Section 12), would be used to select one of those representations as being most applicable to a given request." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

A different language, media type, or encoding is a different representation of the same fact, not a different resource, unless the contract says otherwise. See [Media types](27-media-types.md) and [Cache vary](41-cache-vary.md).

## Check

Request two selections. Each response matches its selection, and both describe the same identity.
