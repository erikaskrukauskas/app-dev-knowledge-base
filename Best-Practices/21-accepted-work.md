---
title: Accepted work
tags: [practices, api, state]
status: tested
updated: 2026-10-17
---

# Accepted work

If the application accepts work it has not finished, the result says the work is accepted, not that the fact already changed.

RFC 9110 says: "a 202 (Accepted) status code if the action will likely succeed but has not yet been enacted" Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

The response names how the caller reads completion later: a status resource, or a later representation of the same resource. Do not return the success shape of a finished write. See [Error contracts](09-error-contracts.md) when the later attempt fails.

## Check

Submit a command the application finishes after the response. The first result does not show the new fact. A later read shows either still in progress or finished.
