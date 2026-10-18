---
title: Consult before a design choice
tags: [practices, architecture, retrieval]
status: verified
updated: 2026-10-17
---

# Consult before a design choice

Search this repository before a significant application design choice. Search the AI knowledge base when the question is how an agent should work.

## Choose the library

| Question | Search |
| --- | --- |
| How should this application be structured, contracted, or checked? | This repo |
| How should an agent brief, search, compare, verify, or record work? | [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base) |
| How should data be moved, modeled for analysis, or released? | The data-engineering, data-science, or CI/CD repo |
| What did this product already decide? | That project's docs and history |

A new project does not need a private copy of these practices. It needs a pointer to this checkout and a habit of searching it. The consultation snippet is in [Agent-Instructions/consultation-protocol.md](../Agent-Instructions/consultation-protocol.md).

## Sequence

1. Name the behavior, the boundary, and the decision you are about to make. See [Specify behavior and done](02-specify-behavior-and-done.md).
2. Search this repo for an application practice that applies.
3. Search the AI knowledge base only when the open question is about the agent's working method.
4. Read the current official documentation when the decision depends on a language, runtime, UI platform, protocol, or test tool. See [Official-Documentation/README.md](../Official-Documentation/README.md).
5. Name the real options, then implement one. See [Compare before choosing](03-compare-before-choosing.md).
6. Run the named check. See [Verify, then record](04-verify-and-record.md).
7. Write a reusable application lesson here. Write an AI-tooling lesson in the AI knowledge base.

## What counts as significant

Search and compare when the work chooses an architecture, a public API, a UI contract, an application state model, an error-handling policy, an accessibility commitment, or a security boundary.

A narrow local fix with an obvious edit can proceed from the code in front of you. Record a lesson afterward if the diagnosis would help another application.

## Enforcement

The consultation protocol asks agents to do this. A project-start checklist is stronger because it is explicit. Use [Agent-Instructions/project-start-checklist.md](../Agent-Instructions/project-start-checklist.md) when a project should require the search.
