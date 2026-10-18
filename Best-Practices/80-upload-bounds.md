---
title: Upload bounds
tags: [practices, api, security]
status: candidate
updated: 2026-10-17
---

# Upload bounds

An upload states a maximum size, the accepted media types, and what happens to a type the application did not ask for.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

The application does not trust the caller's filename for a storage path. See [Caller-supplied URLs](38-caller-supplied-urls.md) when the upload is fetched from a URL instead.

## Check

Upload an oversized body and a disallowed type. Both are rejected and nothing is stored under a caller-chosen path.
