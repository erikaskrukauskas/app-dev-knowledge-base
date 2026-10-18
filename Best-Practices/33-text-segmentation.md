---
title: Text segmentation
tags: [practices, i18n, contracts]
status: tested
updated: 2026-10-17
---

# Text segmentation

A limit, a cursor, or a truncation boundary counts grapheme clusters, not bytes and not UTF-16 code units, when the limit is about what a person sees.

UAX #29 says: "This annex describes guidelines for determining default segmentation boundaries between certain significant text elements: grapheme clusters ("user-perceived characters"), words, and sentences." Checked 2026-10-17 at <https://www.unicode.org/reports/tr29/>.

The checked annex is Unicode 18.0.0, dated 2026-09-01. Confirm the current annex before relying on a boundary rule. See [Unicode normalization](32-unicode-normalization.md) before comparing the text you counted.

## Check

A string with a combining mark or an emoji sequence counts as the user-perceived characters the contract states, and truncation does not split that cluster.
