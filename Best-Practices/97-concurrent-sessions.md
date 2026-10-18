---
title: Concurrent sessions
tags: [practices, security]
status: candidate
updated: 2026-10-17
---

# Concurrent sessions

The contract says whether a person may have more than one session, and what a new login does to older sessions.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

If a new login ends the others, that effect is visible and tested. See [Session end](78-session-end.md).

## Check

Open two sessions under the published rule. The second session's effect on the first matches the contract.
