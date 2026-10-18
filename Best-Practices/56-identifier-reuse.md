---
title: Identifier reuse
tags: [practices, api, state]
status: tested
updated: 2026-10-17
---

# Identifier reuse

An identifier that a caller has stored is not reissued for a different fact. Uniqueness is across time, not only across the rows that exist today.

RFC 9562 says: "A UUID is 128 bits long and is intended to guarantee uniqueness across space and time." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9562>.

See [Stable identifiers](14-stable-identifiers.md). A tombstone or a retired-id record is one way to keep the promise after deletion.

## Check

Delete a fact and create another. The new fact has a new identifier. A read of the old identifier does not return the new fact.
