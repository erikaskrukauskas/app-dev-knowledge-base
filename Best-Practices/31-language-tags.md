---
title: Language tags
tags: [practices, i18n, contracts]
status: tested
updated: 2026-10-17
---

# Language tags

A language label uses a language tag, not a private word such as a country name. The contract says where the tag appears.

RFC 5646 says: "This document describes the structure, content, construction, and semantics of language tags for use in cases where it is desirable to indicate the language used in an information object." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc5646>.

Tags are for the language of the content. They are not a substitute for translated text. See [Internationalization](15-internationalization.md). Confirm the current registry before relying on a subtag.

## Check

Store a tag and read it back unchanged. An invented tag that is not in the contract is rejected.
