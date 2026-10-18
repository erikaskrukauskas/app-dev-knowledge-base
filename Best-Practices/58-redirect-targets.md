---
title: Redirect targets
tags: [practices, security, api]
status: tested
updated: 2026-10-17
---

# Redirect targets

A redirect target is chosen from an allow list or built by the application. A caller-supplied URL is not copied into the redirect.

RFC 9110 says: "the user agent MAY then make its own decision regarding whether or not to redirect the request." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9110>.

RFC 9110 leaves the follow decision to the user agent, so a malicious target would run in the caller's session. See [Caller-supplied URLs](38-caller-supplied-urls.md).

## Check

Pass an external URL as the next location. The response does not redirect there.
