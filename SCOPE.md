---
title: Scope of this repository
tags: [scope, governance, architecture]
status: verified
updated: 2026-10-17
---

# Scope

This repository is the application-development knowledge base. Other projects read it for practices and verified lessons about designing, contracting, and checking applications.

## In this repo

- Architecture choices that still apply after one product's constraints are removed.
- Design patterns stated as application structure, not as a framework tutorial.
- API and UI contracts: observable behavior, boundaries, and compatibility.
- Application state: where state lives, who may change it, and how a caller observes it.
- Coding standards that transfer across a stack.
- Testing, accessibility, and error handling.
- Application security: input handling, authentication and authorization boundaries, and secrets kept out of git.

## In other repos

| Topic | Where it lives |
| --- | --- |
| AI tooling, agent instructions, prompting, retrieval, and MCP | [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base) |
| Data engineering | Its own knowledge repo |
| Data science | Its own knowledge repo |
| CI/CD and release automation | Its own knowledge repo |
| A single project's requirements, environment names, credentials, and local architecture choices | That project |

On this machine the AI knowledge base checkout is `C:\Users\erika\Cursor Projects\ai-knowledge-base`.

A lesson about prompting an agent, a warehouse model, a statistical method, or a release pipeline is recorded in the matching repo. If that work also produced a reusable application lesson (for example, a clearer API boundary or a test that defines done), write the application lesson here and link to the other write-up.

## Where a new note goes

Ask what a future application in an unrelated project could reuse.

- If the answer is how to shape, contract, or check an application, add it here.
- If the answer is how an agent should brief, search, compare, verify, or record work, add it to the AI knowledge base.
- If the answer depends on a dataset, a model, or a release system, add it to that domain repo.
- If the answer only makes sense with this product's requirements, environment names, or credentials, keep it in the project.
- If one effort produces both an application lesson and an AI-tooling lesson, split the note. This repo keeps the application lesson. The AI knowledge base keeps the tooling lesson.

## Reusable practice and project knowledge

Reusable practice in this repo applies across projects: how to specify behavior, how to compare an architecture, how to draw an authorization boundary.

Project knowledge stays in the project: requirements, environment names, credential locations, local architecture choices, and test results that only make sense there.

Do not copy a project decision into this repo to make it feel official. Promote it only after it is stated as a practice that still holds without that project's constraints.
