---
title: Deprecating a contract
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Deprecating a contract

Deprecation keeps the old behavior working, tells the caller it will stop, and names the replacement. Removal is a later, incompatible change.

RFC 8594 says: "This specification defines the Sunset HTTP response header field, which indicates that a URI is likely to become unresponsive at a specified point in the future." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc8594>. That specification is informational. The header is a signal for HTTP. It does not replace a documented replacement.

## The window

Do not remove the behavior in the same release that first announces the deprecation. Callers need a release where the old contract still succeeds and the announcement is visible. Semantic Versioning treats the deprecation notice as a compatible change and the removal as an incompatible one. See [API compatibility](12-api-compatibility.md).

The announcement includes the date or version when the old behavior ends, and where the caller should go instead. A sunset header without that explanation is not the contract.

## Check

During the window, an old caller still succeeds, and the response or the docs expose the deprecation. After the announced end, the old call fails through the [error contract](09-error-contracts.md), not through a timeout that looks like an outage.
