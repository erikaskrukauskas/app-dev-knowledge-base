---
title: Official documentation
tags: [documentation, sources, testing]
status: verified
updated: 2026-10-17
---

# Official documentation

Language, platform, and protocol behavior changes. These rows are entry points, not copied manuals. Confirm the current page before relying on a feature. Record the version you checked when a decision depends on it.

When a practice page and an official page disagree about a product feature, the official page for the version you run wins. Update or supersede the practice page afterward.

Checked as entry points on 2026-10-17.

## Languages and runtimes

| Source | Entry |
| --- | --- |
| Python | https://docs.python.org/3/ |
| Go | https://go.dev/doc/ |
| Java | https://docs.oracle.com/en/java/ |
| .NET | https://learn.microsoft.com/dotnet/ |
| Rust | https://doc.rust-lang.org/ |
| TypeScript | https://www.typescriptlang.org/docs/ |
| JavaScript (MDN) | https://developer.mozilla.org/docs/Web/JavaScript |

## UI platforms

| Source | Entry |
| --- | --- |
| Web platform (MDN) | https://developer.mozilla.org/docs/Web |
| Apple platforms | https://developer.apple.com/documentation/ |
| Android | https://developer.android.com/docs |

## HTTP and API specifications

| Source | Entry |
| --- | --- |
| HTTP semantics (RFC 9110) | https://www.rfc-editor.org/rfc/rfc9110 |
| JSON (RFC 8259) | https://www.rfc-editor.org/rfc/rfc8259 |
| OpenAPI | https://spec.openapis.org/oas/latest.html |

## Accessibility

| Source | Entry |
| --- | --- |
| WAI overview | https://www.w3.org/WAI/ |
| WCAG | https://www.w3.org/WAI/standards-guidelines/wcag/ |
| ARIA Authoring Practices | https://www.w3.org/WAI/ARIA/apg/ |

## Testing tools

These are places to confirm a tool's current behavior. The practice of naming a check lives in [Verify, then record](../Best-Practices/04-verify-and-record.md). This list does not choose a test stack.

| Source | Entry |
| --- | --- |
| pytest | https://docs.pytest.org/en/stable/ |
| JUnit 5 | https://junit.org/junit5/docs/current/user-guide/ |
| Playwright | https://playwright.dev/docs/intro |

## How to add a source

Add a row with the official entry URL, the date you checked it, and the decision it supports. Keep AI product docs in the AI knowledge base. Keep warehouse, analytics, and CI vendor docs in those repos.

## Local notes

If you need a short note about a documentation page, add a file next to this README:

- Name it for the topic, not the whole product.
- State the version and the date checked.
- Quote only the minimum needed to support a decision, with the URL.
- Link the note from the practice or lesson that depends on it.
