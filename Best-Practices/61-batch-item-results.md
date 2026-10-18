---
title: Batch item results
tags: [practices, api, error]
status: tested
updated: 2026-10-17
---

# Batch item results

A batch says whether it is all-or-nothing. If items can fail independently, each item has its own result, including a machine-readable error for the ones that failed.

RFC 9457 says: "This document defines a "problem detail" to carry machine-readable details of errors in HTTP response content to avoid the need to define new error response formats for HTTP APIs." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc9457>.

Do not hide a failed item inside a success for the whole batch. See [Error contracts](09-error-contracts.md).

## Check

Submit a batch with one valid item and one invalid item. The valid item follows the published rule, and the invalid item carries its own error.
