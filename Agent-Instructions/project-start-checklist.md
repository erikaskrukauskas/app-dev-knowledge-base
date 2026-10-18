---
title: Project-start checklist
tags: [agents, architecture, testing]
status: verified
updated: 2026-10-17
---

# Project-start checklist

The consultation protocol states the rule. This checklist is the stronger version: run it at the start of a project and again before a large application change.

## Checklist

- [ ] Project agent instructions include the [consultation protocol](consultation-protocol.md) and the correct path to this repo.
- [ ] The AI knowledge base is linked for questions about how an agent should work.
- [ ] Data engineering, data science, and CI/CD repos are linked from the project when this work depends on them.
- [ ] Searched this repo for practices that match the design (`architecture`, `api`, `state`, `security`, `testing`, or `accessibility`).
- [ ] Searched `Lessons-Learned/` for verified lessons in a similar environment.
- [ ] Named the behavior, the boundary, and the check that defines done.
- [ ] For a significant design, named the real options before implementing one.
- [ ] Confirmed language, runtime, UI, HTTP, accessibility, or testing behavior that the design depends on, using current official docs.

## After the work

- [ ] The named check was run: a test, an exercised user path, or both.
- [ ] A reusable application lesson was added here only if a later application would otherwise repeat the same investigation.
- [ ] An AI-tooling lesson, if any, was written in the AI knowledge base and linked.
- [ ] No secrets, environment credentials, or copyrighted sources were copied into this repo.

## Where the notes go

Application design stays in this repo. Agent method stays in the AI knowledge base. A single product's requirements stay in the project. See [Practice versus project](../Best-Practices/05-practice-versus-project.md).
