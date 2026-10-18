---
title: Personal data export
tags: [practices, security, api]
status: candidate
updated: 2026-10-17
---

# Personal data export

An export returns the personal data the application holds for that person, in a documented shape, and only to an authorized caller.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

The export is consistent as of a stated time. It does not include another person's data. See [Audit actor](63-audit-actor.md).

## Check

Export as the person and as a different person. Only the authorized export contains the first person's data.
