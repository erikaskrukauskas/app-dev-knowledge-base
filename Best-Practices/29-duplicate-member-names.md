---
title: Duplicate member names
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Duplicate member names

A request object uses each member name once. The application rejects a duplicate instead of picking the first or the last in private.

RFC 8259 says: "The names within an object SHOULD be unique." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc8259>.

If a parser keeps one of the duplicates, the contract still says which, and tests cover it. Silent dependence on parser order is not a contract.

## Check

Submit the same name twice with different values. The application rejects the body, or it documents the single value it kept.
