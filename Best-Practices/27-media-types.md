---
title: Media types
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Media types

Every representation names its media type. Callers do not sniff bytes to guess the format.

RFC 9110 says: "The "Content-Type" header field indicates the media type of the associated representation" Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

A changed media type that old callers cannot read is an incompatible change. See [API compatibility](12-api-compatibility.md). Confirm the current media type registration before relying on a parameter.

## Check

Read a resource and parse it only as the named media type. A wrong type fails the check rather than being guessed.
