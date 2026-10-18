---
title: Side effects after commit
tags: [practices, state, architecture]
status: tested
updated: 2026-10-17
---

# Side effects after commit

An external effect that is not itself idempotent is emitted only after the state write that authorizes it has committed. A crash then retries the write, not a second copy of the effect.

RFC 9110 says: "A request method is considered "idempotent" if the intended effect on the server of multiple identical requests with that method is the same as the effect for a single such request." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

Record the intent in the same commit as the fact, then send. If the send can repeat, the receiver dedupes. See [Exactly-once claims](52-exactly-once-claims.md).

## Check

Crash after the send is prepared and before it completes. Recovery produces one external effect, not two.
