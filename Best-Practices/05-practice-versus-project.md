---
title: Practice versus project
tags: [practices, scope, governance]
status: verified
updated: 2026-10-17
---

# Practice versus project

Keep a reusable application practice in this repo. Keep a decision that depends on one product's constraints in that project.

## Promote a decision here when

- The rule still holds after the product name, environment names, and local deployment choices are removed.
- Another application could follow it without that project's backlog, dataset, or vendor account.
- The evidence is a check that passed, not a preference from one review.

Examples that can belong here after the project details are stripped: how to version a public API, where to validate input, how to separate authorization from authentication, how to describe an empty state, how to report an error to a caller.

## Leave it in the project when

- It names a requirement, a screen, a ticket, or a customer.
- It names an environment, a host, a URL, or a credential location.
- It chooses a local architecture because of a constraint that other applications do not share.
- Removing those details leaves nothing a future project can apply.

## How to write the promoted version

State the practice as behavior and a boundary. Link the project's write-up if one exists. Do not paste the project's configuration, sample payloads from production, or secrets.

If the same effort also taught something about how an agent should work, put that lesson in the [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base) and link it. See [SCOPE.md](../SCOPE.md).

## One canonical page

If a practice page already covers the topic, update that page. Do not add a second page that restates it with the project's nouns swapped in. See [Write findable pages](07-write-findable-pages.md).
