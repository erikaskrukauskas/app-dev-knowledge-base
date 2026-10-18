---
title: Specify behavior and done
tags: [practices, contracts, testing]
status: verified
updated: 2026-10-17
---

# Specify behavior and done

Describe the application change as observable behavior, a boundary, and the check that defines done. A topic name is not a specification.

## Include

- The behavior a user or caller can observe: what they send, what they receive, and what stays unchanged.
- The boundary: which module, API, screen, or trust edge is in scope, and which neighboring system is out of scope.
- The failure behavior: what the caller sees when input is rejected, a dependency fails, or the user lacks permission.
- The check that defines done: a test, an exercised user path, or both. Name the command or the steps.
- Constraints that are easy to violate: a public contract, a persisted shape, an accessibility requirement, or a file the change must leave alone.

## Leave out

- A tour of unrelated product history.
- A framework choice presented as the requirement. The requirement is the behavior. The framework is an implementation option. See [Compare before choosing](03-compare-before-choosing.md).
- Copies of entire standards. Link the canonical page.

## Size the change

Ask for one observable outcome when later steps depend on it. A request that mixes a new public API, a new state model, and a visual redesign is harder to check and easier to leave half done.

## Revision

When the result misses the mark, add the missing behavior or boundary to the specification. Say which check failed. A restatement that does not name the miss produces another broad attempt.

## For pages in this repo

A documentation change names the decision, the audience (a later application project), and the page to update. New pages are for new topics. Existing topics are edited in place. See [Write findable pages](07-write-findable-pages.md).
