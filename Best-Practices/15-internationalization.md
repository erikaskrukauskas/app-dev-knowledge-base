---
title: Internationalization
tags: [practices, i18n, contracts]
status: tested
updated: 2026-10-17
---

# Internationalization

User-facing text is data in the reader's language and script. Do not build a sentence by gluing fragments in the author's word order.

The W3C internationalization quick tips say: "Use care when composing sentences from multiple strings." They also say: "Use the UTF-8 (Unicode) character encoding for content, databases, etc." Checked 2026-10-17 at <https://www.w3.org/International/quicktips/>.

## Text

Keep a whole message, with named placeholders, rather than concatenating translated pieces. Declare the language of the text. Accept and store Unicode. On the web, UTF-8 is the encoding those tips require. Always declare the encoding you use.

Do not assume one shape for a person's name, an address, or the order of day, month, and year. An instant still follows [Date and time contracts](13-date-and-time.md). The local presentation of that instant can differ.

## Direction and checks

When the interface can show a right-to-left script, the layout follows the base direction of that text. A string that is not the author's language belongs in the check, including a case where word order or direction differs. Language that a person hears or reads is also an accessibility fact. See [Accessibility](08-accessibility.md).

Confirm the current quick tips before relying on a markup attribute.
