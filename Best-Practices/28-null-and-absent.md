---
title: Null and absent
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Null and absent

Null is a value. An absent member is the lack of a member. The contract says which one it uses, and it does not treat them as the same unless it says so.

RFC 8259 says: "A JSON value MUST be an object, array, number, or string, or one of the following three literal names" Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc8259>.

RFC 8259 includes null among the literal names, and those names must be lowercase. Clearing a field is a different command from omitting the field on a partial update. See [API compatibility](12-api-compatibility.md) before changing which one a caller must send.

## Check

Send a body with the member absent and a body with the member null. The stored results differ in the way the contract describes.
