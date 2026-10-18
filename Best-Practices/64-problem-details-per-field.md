---
title: Field errors
tags: [practices, error, api]
status: tested
updated: 2026-10-17
---

# Field errors

When the caller can fix the input, the error identifies the field. A single undifferentiated failure is not enough when several fields can be wrong.

RFC 9457 says: "This document defines a "problem detail" to carry machine-readable details of errors in HTTP response content to avoid the need to define new error response formats for HTTP APIs." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9457>.

Keep the caller's submitted values available to correct. Do not invent a second error document if problem details can carry the field list. See [Error contracts](09-error-contracts.md).

## Check

Submit two invalid fields. The response names both, and the stored state is unchanged.
