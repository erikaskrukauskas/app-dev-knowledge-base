---
title: Application Development Knowledge Base
tags: [overview, architecture, scope]
status: verified
updated: 2026-10-17
---

# Application Development Knowledge Base

This repository is the shared library for **application-development knowledge**: architecture, design patterns, API and UI contracts, application state, coding standards, testing, accessibility, error handling, and application security. Other projects consult it for practices that still apply after a single product's constraints are removed.

AI tooling, data engineering, data science, and CI/CD keep their own repositories. This repo stores how an application is designed and checked, not how an agent is briefed and not how a pipeline is released.

## What belongs here

- Stable practices for application design, contracts, state, testing, accessibility, error handling, and application security.
- Lessons from real application work, after they have been checked.
- Pointers to current language, platform, HTTP, accessibility, and testing documentation.
- Citations and original notes for application-development references. Full copyrighted books and PDFs stay out of git.

## How another project uses it

1. Point that project's agent instructions at this checkout. Copy the snippet from [Agent-Instructions/consultation-protocol.md](Agent-Instructions/consultation-protocol.md).
2. Search before a significant application design choice:

```powershell
python Search-Index/search.py "application security"
python Search-Index/search.py --tag architecture
python Search-Index/search.py --list
```

3. Apply what is reusable. Leave requirements, environment names, credentials, and local architecture choices in the project repo.
4. After a verified application lesson, add a file under `Lessons-Learned/` using the template.

Questions about briefing, searching, comparing, verifying, or recording AI-assisted work belong in the [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base). On this machine that checkout is `C:\Users\erika\Cursor Projects\ai-knowledge-base`.

## Layout

| Path | Role |
| --- | --- |
| `Best-Practices/` | Stable application-development practices |
| `Lessons-Learned/` | Findings from real work and their validation state |
| `Agent-Instructions/` | Pointers for Cursor, Codex, Claude Code, and ChatGPT |
| `Official-Documentation/` | Links to current language, platform, HTTP, accessibility, and testing docs |
| `Books/` | Citation and notes policy for references |
| `Search-Index/` | Local keyword search over this repo |
| `MCP-Server/` | Design for a later shared retrieval service |
| `AGENTS.md` | Rules for agents editing this repo |
| `SCOPE.md` | Boundary between this repo and sibling repos |

## Roadmap

| Phase | Outcome | State |
| --- | --- | --- |
| 1. Foundation | Folder layout, practices, lessons template, keyword search | In this repo |
| 2. MCP | Local MCP tools so agents can search from any project | Designed, not built |
| 3. Lessons memory | Validation workflow, superseding, retrieval of verified lessons | Template and rules are in place |
| 4. Remote access | Authenticated API or connector for agents that cannot read a local checkout | Later, after a local workflow is proven |

## Principles

- Search this repo for an application design question. Search the AI knowledge base for how an agent should work.
- Record a lesson after a test or an exercised user path. Mark replacements as superseded.
- Keep one copy of each practice. Agent-specific files link to it.
- Keep a product's requirements, credentials, and local choices in that project.
