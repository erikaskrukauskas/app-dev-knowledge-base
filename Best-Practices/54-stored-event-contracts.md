---
title: Stored event contracts
tags: [practices, state, api]
status: tested
updated: 2026-10-17
---

# Stored event contracts

A stored event that another component reads is a public contract. Name its fields. A change that breaks a consumer is a new version, not a quiet edit of old events.

Semantic Versioning 2.0.0 says: "Software using Semantic Versioning MUST declare a public API." Checked 2026-10-17 at <https://semver.org/>.

See [API compatibility](12-api-compatibility.md). Consumers skip or transform versions they do not know. They do not crash the whole stream on one new field they can ignore.

## Check

Write an event, then add an optional field. An old consumer still reads the old fields. Removing an old field is rejected by the compatibility check.
