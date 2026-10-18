---
title: Derived representations
tags: [practices, state]
status: tested
updated: 2026-10-17
---

# Derived representations

One stored fact is the authority. A summary, a feed, or a second format is derived from it and is not updated as if it were another copy of the truth.

RFC 9110 says: "A target resource might be provided with, or be capable of generating, multiple representations that are each intended to reflect the resource's current state." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

When the fact changes, derived views catch up or they are computed on read. A writer does not patch the derived view and leave the fact stale.

## Check

Change the stored fact. Every derived view the contract promises then shows the new fact, or it shows a stated lag.
