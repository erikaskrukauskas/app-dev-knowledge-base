---
title: Stable identifiers
tags: [practices, api, state]
status: tested
updated: 2026-10-17
---

# Stable identifiers

An identifier a caller stores keeps finding the same thing after the display name, the sort order, or the host changes.

RFC 9562 says: "A UUID is 128 bits long and is intended to guarantee uniqueness across space and time." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9562>. This specification obsoletes RFC 4122.

## What may be an identifier

Use an identifier the application assigns, not a list index, a localized label, or a secret. A UUID is one way to get uniqueness without a single counter. Confirm the RFC before relying on a version's bit layout or on how a version should be generated.

The public identifier is part of the API. Changing it is an incompatible change. See [API compatibility](12-api-compatibility.md). Who may mint the identifier is a state decision. See [Compare before choosing](03-compare-before-choosing.md).

## Check

Rename the thing and reorder the collection. The previous identifier still returns it. A guessable secret is not the identifier. See [Application security](06-application-security.md).
