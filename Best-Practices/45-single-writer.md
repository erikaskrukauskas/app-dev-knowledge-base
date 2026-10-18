---
title: Single writer
tags: [practices, state, architecture]
status: tested
updated: 2026-10-17
---

# Single writer

Each stored fact has one writer. Other components ask that writer to change it. They do not patch the same store on their own.

RFC 9110 says: "whereas the enclosed representation in a PUT request is defined as replacing the state of the target resource." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

HTTP PUT is the protocol shape of a replacement by the component that owns the resource. Two writers need an explicit merge or they will lose updates. See [Conditional updates](11-conditional-updates.md).

## Check

Two components attempt the change. Only the owning writer commits it, and the other is rejected or forwarded.
