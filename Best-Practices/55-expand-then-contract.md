---
title: Expand then contract
tags: [practices, state, api]
status: tested
updated: 2026-10-17
---

# Expand then contract

Change a stored shape by expanding first: add the new form, write both, move readers, then remove the old form. Do not remove the old form while a reader still requires it.

Semantic Versioning 2.0.0 says: "increment the MAJOR version when you make incompatible API changes" Checked 2026-10-17 at <https://semver.org/>.

SemVer treats an incompatible change as a major change. A stored schema has the same duty to existing readers. The project names its own migration tool. This page only orders the steps.

## Check

Deploy the reader of the new form before the writer stops filling the old form. The reader never observes a row it cannot read.
