---
title: Lessons learned
tags: [lessons, index, testing]
status: verified
updated: 2026-10-17
---

# Lessons learned

Lessons are evidence from real application work. Best-practice pages are the stable rules. A lesson becomes a practice only after the reusable part still holds with the original project's constraints removed.

## Lifecycle

`candidate` → `tested` → `verified`

| Status | Set it when |
| --- | --- |
| `candidate` | The finding is written down and has not been re-checked |
| `tested` | The check was reproduced or the evidence was reviewed in this environment |
| `verified` | Another session can apply the application lesson without re-discovering the dead ends |
| `superseded` | A newer lesson or practice page replaces it |

Superseded files stay in the folder. Set `superseded_by` to the replacement path. Do not delete them.

## File names

`LL-0001-short-slug.md`

Increment the number. Do not reuse an id.

## What to record

Use [_template.md](_template.md). A useful lesson includes the environment, the approaches that failed, the working approach, and the check that showed it worked.

Record an application lesson here: architecture, a contract, state, testing, accessibility, error handling, or application security. Record an AI-tooling lesson in the [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base). If both exist, link them.

## Current lessons

| ID | Title | Status |
| --- | --- | --- |
| [LL-0001](LL-0001-application-development-only.md) | Keep this repo to application development | verified |
