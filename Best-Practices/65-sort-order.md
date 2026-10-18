---
title: Sort order
tags: [practices, api, contracts]
status: candidate
updated: 2026-10-17
---

# Sort order

A collection response states the sort. Position in an unspecified order is not part of the contract.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Name the fields and the direction. If the order can change between requests, say so. See [Paging collections](16-paging-collections.md).

## Check

Request the collection twice with the same sort. The order matches, or the contract says it is unstable.
