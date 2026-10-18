---
title: Error contracts
tags: [practices, error, api]
status: tested
updated: 2026-10-17
---

# Error contracts

Every failure a caller can observe needs a contract: what was rejected or what failed, whether state changed, and what the caller can do next.

## What the caller receives

Separate a caller mistake from a failure inside the application. A missing field, a value outside the accepted range, and a missing permission are caller mistakes. A dependency the application could not reach is not the caller's mistake. Say which is which.

The error names the condition in a stable token the caller can branch on. Human text can change. The token should not. Do not put a stack trace, a secret, or another caller's data in the error. See [Application security](06-application-security.md).

Say whether the failed call changed stored state. A caller that retries needs that fact. See [Idempotent operations](10-idempotent-operations.md).

## HTTP APIs

Do not invent a new error document for an HTTP API when problem details already fit. RFC 9457 says: "This document defines a "problem detail" to carry machine-readable details of errors in HTTP response content to avoid the need to define new error response formats for HTTP APIs." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9457>. It obsoletes RFC 7807.

Confirm that page before relying on a field name. The status code and the problem type still have to match the contract you named in [Specify behavior and done](02-specify-behavior-and-done.md).

## Check

Include one rejected call and one internal failure in the check. See [Verify, then record](04-verify-and-record.md).
