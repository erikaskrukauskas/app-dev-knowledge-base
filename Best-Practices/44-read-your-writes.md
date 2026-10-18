---
title: Read your writes
tags: [practices, state, api]
status: tested
updated: 2026-10-17
---

# Read your writes

After a successful write, the caller that wrote can read the new state. A later read does not show the pre-write fact to that caller.

RFC 9110 says: "In a successful response to a state-changing request, validator fields describe the new representation that has replaced the prior selected representation as a result of processing the request." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

A cache or a replica that still holds the old fact is not the read the writer uses. See [Conditional updates](11-conditional-updates.md) for the validator on that new representation.

## Check

Write a fact and read it as the same caller. The read returns the written value.
