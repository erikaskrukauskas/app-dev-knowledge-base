---
title: Paging collections
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Paging collections

Pagination is part of a collection contract. State a bound. Do not make an unbounded list the only way to read the collection.

RFC 8288 says: "This specification defines a model for the relationships between resources on the Web ("links") and the type of those relationships ("link relation types")." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc8288>.

## The page

Say how many items a caller receives, how to ask for the next page, and what an empty page means. On the web, a registered link relation such as `next` can point at the following page. Do not give a registered relation a private meaning.

Say whether a page stays stable if a writer inserts or deletes a row while the caller walks the collection. A cursor into a stable order is a different contract from an offset into a list that shifts. Changing that contract later is an [API compatibility](12-api-compatibility.md) question.

## Check

Request a middle page and a page past the end. The past-the-end result is the empty contract, not a new error shape, unless the specification says a bad cursor is rejected. See [Error contracts](09-error-contracts.md).
