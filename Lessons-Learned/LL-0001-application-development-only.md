---
id: LL-0001
title: Keep this repo to application development
tags: [lessons, scope, governance]
status: verified
updated: 2026-10-17
environment: "Cursor, Windows, app-dev-knowledge-base repo"
scope: global
superseded_by:
---

# Keep this repo to application development

## Problem

Application design, agent workflow, data work, and release automation were easy to store in one library. A search in that library would return a prompting habit next to an API boundary, and a later project could treat a product-specific choice as a general rule.

## Approaches that failed

- Approach: Plan one engineering library that holds application design, AI tooling, data engineering, data science, and CI/CD.
- Why it failed: Each of those subjects has its own repo. Mixing them makes search results noisier and encourages an agent to apply a data-pipeline or release decision as if it were an application practice.
- Evidence: Scope decision for this repository, 2026-10-17.

## Working solution

Use this repository only for application-development knowledge: architecture, design patterns, API and UI contracts, application state, coding standards, testing, accessibility, error handling, and application security.

Put agent briefing, retrieval, and lesson-capture method in the [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base). Put data engineering, data science, and CI/CD in their own repos. Put requirements, environment names, credentials, and local architecture choices in the project.

When one effort produces both an application lesson and an AI-tooling lesson, write the application lesson here and link to the AI knowledge base for the tooling lesson. See [SCOPE.md](../SCOPE.md).

## Verification

- Check run: Scope review against the repository decision and the folder layout.
- Result: Root docs and best-practice pages describe application design and checks. Agent workflow, data platforms, and release automation appear as subjects that belong in other repos.

## Scope

`global` for any future project that consults this knowledge base.

## References

- [SCOPE.md](../SCOPE.md)
- [Practice versus project](../Best-Practices/05-practice-versus-project.md)
