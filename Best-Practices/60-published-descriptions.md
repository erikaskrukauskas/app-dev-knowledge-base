---
title: Published descriptions
tags: [practices, api, testing]
status: tested
updated: 2026-10-17
---

# Published descriptions

If the application publishes an API description, the check runs against that description. A description that drifts from the behavior is a bug in one of them.

OpenAPI Specification says: "OpenAPI Specification v3.2.1" Checked 2026-10-17 at <https://spec.openapis.org/oas/latest.html>.

The latest document fetched on 2026-10-17 identifies itself as OpenAPI Specification v3.2.1, dated 10 September 2026. Confirm the current specification before relying on a keyword. The description is not a second behavior. See [Specify behavior and done](02-specify-behavior-and-done.md).

## Check

Compare one published operation with the running behavior. The status codes, required fields, and media types agree.
