---
title: Action links
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Action links

When the next action depends on state, the response links to that action and names the relation. Callers do not invent a URI the contract did not give them.

RFC 8288 says: "In the simplest case, a link relation type identifies the semantics of a link." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc8288>.

Registered relations keep their registered meaning. A private relation is named as an extension, not by overloading a registered one. Paging is a special case. See [Paging collections](16-paging-collections.md).

## Check

Read a resource in two states. The offered relations differ with the state, and a relation that is absent is not called anyway.
