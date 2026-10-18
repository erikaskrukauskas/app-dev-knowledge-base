---
title: Caller-supplied URLs
tags: [practices, security]
status: tested
updated: 2026-10-17
---

# Caller-supplied URLs

The application does not fetch, redirect to, or embed a URL just because a caller sent it. Destinations are an allow list, or the feature does not exist.

CWE-918 says: "The web server receives a URL or similar request from an upstream component and retrieves the contents of this URL, but it does not sufficiently ensure that the request is being sent to the expected destination." Checked 2026-10-17 at <https://cwe.mitre.org/data/definitions/918.html>.

CWE-918 is server-side request forgery: the server is tricked into calling a destination the caller should not reach, including internal hosts and non-HTTP schemes. Resolve the address after redirects and reject unexpected schemes, addresses, and ports.

## Check

Submit a URL aimed at a local or metadata address. The application does not request it.
