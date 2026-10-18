---
title: Redirect contracts
tags: [practices, api]
status: tested
updated: 2026-10-17
---

# Redirect contracts

A redirect names the next URI and lets the caller decide whether to follow it. The application does not assume every caller will follow.

RFC 9110 says: "the origin server MUST send an appropriate 3xx (Redirection) response; the user agent MAY then make its own decision regarding whether or not to redirect the request." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

The target is a URI the application chose, not a raw value from the caller. See [Redirect targets](58-redirect-targets.md). A redirect is not a 200 that hides the move.

## Check

Send a request that should move. The response is a redirection with a target. A caller that does not follow still has an unambiguous result.
