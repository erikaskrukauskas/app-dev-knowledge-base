---
title: Agent rules for this repository
tags: [agents, governance]
status: verified
updated: 2026-10-17
---

# Agent rules

You are in the application-development knowledge base. Other projects consult this repo for application design, contracts, state, testing, accessibility, error handling, and application security. AI tooling, data engineering, data science, and CI/CD have their own repos.

## While editing this repo

- Add or update application-development knowledge only. Read [SCOPE.md](SCOPE.md) before creating a document.
- Put stable guidance in `Best-Practices/`. Put findings from real work in `Lessons-Learned/`.
- Give every document YAML frontmatter with `title`, `tags`, `status`, and `updated`.
- Lessons also have `id`, `environment`, `scope`, and `superseded_by`.
- Keep one canonical copy of a practice. Link to it from agent-specific files.
- Do not commit secrets, credentials, copyrighted books, or verbatim official documentation.
- Do not present an untested finding as `verified`. Use the lifecycle in [Lessons-Learned/README.md](Lessons-Learned/README.md).
- When a newer document replaces an older one, set the old document to `superseded` and point `superseded_by` at the replacement. Do not delete it.

## Status values

`candidate` → `tested` → `verified`

Use `superseded` when a newer document replaces this one. Keep the old file so past references still resolve.

## Questions that belong elsewhere

- How an agent should brief, search, compare, verify, or record work: the [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base).
- Data engineering, data science, and CI/CD: those repos.
- One product's requirements, environment names, credentials, and local architecture choices: that project.

## Skills

- A topic this repo does not yet cover: `.cursor/skills/add-uncovered-app-topic/SKILL.md`
- Whether a covered topic still matches current sources: `.cursor/skills/review-covered-app-topics/SKILL.md`

## Before you finish a documentation change

Search for an existing page on the same topic:

```powershell
python Search-Index/search.py --list
python Search-Index/search.py "your topic"
```

Update the existing page when the topic already exists.
