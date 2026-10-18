---
title: Conditional updates
tags: [practices, state, api]
status: tested
updated: 2026-10-17
---

# Conditional updates

When two callers can write the same stored fact, a write carries the version the caller read. If that version is no longer current, the write is rejected.

RFC 9110 describes the lost-update case: "An ETag field in a 201 (Created) response communicates the entity tag of the newly created resource's representation, so that the entity tag can be used as a validator in later conditional requests to prevent the "lost update" problem." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

## The rule

Return a validator when the caller reads a fact it may later change. On write, require that validator. Strong comparison is the one that rejects any change to the representation. Do not accept a blind overwrite of a shared fact.

The rejection is an [error contract](09-error-contracts.md): the caller's copy is stale, state did not change to the stale write, and the caller can read the current fact and try again.

For HTTP, `If-Match` with a strong entity tag is the precondition. Confirm the current RFC section before relying on a header. Choosing how the version is stored is an application state decision. See [Compare before choosing](03-compare-before-choosing.md).

## Check

Two callers read the same fact. The first write succeeds. The second write, still carrying the original version, is rejected and leaves the first write in place.
