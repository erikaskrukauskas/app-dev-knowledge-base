---
title: Accessibility
tags: [practices, accessibility, contracts]
status: tested
updated: 2026-10-17
---

# Accessibility

Name the accessibility behavior for a user-visible change, and include that behavior in the check that defines done.

## What to name

State the path a person must be able to complete, including what they perceive, operate, and understand. A screenshot of the first paint is not that behavior. See [Specify behavior and done](02-specify-behavior-and-done.md) and [Verify, then record](04-verify-and-record.md).

For web content, use the latest W3C Recommendation of WCAG and name the conformance level. The WAI overview says: "W3C encourages you to use the latest version of WCAG." Checked 2026-10-17 at <https://www.w3.org/WAI/standards-guidelines/wcag/>.

On that date the latest Recommendation is WCAG 2.2. Its success criteria are the conformance test. WCAG 3 is a separate draft on that site. Do not use the draft as the requirement.

WCAG 2.2 groups its guidelines under four principles: perceivable, operable, understandable, and robust. Use those principles to choose which success criteria the change can break. Do not copy the guideline text into this repo. Confirm the current page before relying on a criterion number.

## Interfaces that are not web pages

That overview says WCAG can also be applied to non-web information and communications technologies, including native apps, software, and documents, as described in WCAG2ICT. When the interface is not a web page, say whether the requirement is WCAG2ICT or the platform accessibility API. Confirm the current platform page in [Official-Documentation/README.md](../Official-Documentation/README.md) before relying on a feature.

## Names, keyboard, and widgets

A control needs an accessible name. A control a person can reach with a pointer needs a keyboard path, unless the specification says the platform already provides that path.

Do not invent a role or keyboard behavior for a custom control. For web widgets, use the ARIA Authoring Practices Guide. It "describes how to apply accessibility semantics to common design patterns and widgets." Checked 2026-10-17 at <https://www.w3.org/WAI/ARIA/apg/>.

## What this page does not decide

It does not choose a component library or a test tool. The check is the success criteria the change touches, exercised on the user path.
