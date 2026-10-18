---
title: URI identity
tags: [practices, api]
status: tested
updated: 2026-10-17
---

# URI identity

A resource has one URI identity in the contract. Superficial spelling differences are not extra resources unless the URI specification says they differ.

RFC 3986 says: "A Uniform Resource Identifier (URI) is a compact sequence of characters that identifies an abstract or physical resource." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc3986>.

Do not put a secret, a password, or a session token in the URI. See [Logging credentials](59-logging-credentials.md). Relative references resolve against a stated base. Confirm RFC 3986 before relying on equivalence rules.

## Check

Request the canonical URI and a spelling the contract says is equivalent. Both identify the same resource, or the odd spelling is rejected.
