---
title: Consultation protocol
tags: [agents, architecture, retrieval]
status: verified
updated: 2026-10-17
---

# Consultation protocol

Paste this into a project's `AGENTS.md` or `CLAUDE.md`. Adjust the paths.

```markdown
## Knowledge bases

Application practices live in `<path-to-app-dev-knowledge-base>`.
AI working practices live in `<path-to-ai-knowledge-base>`.
Data engineering, data science, and CI/CD live in their own repos.
Project requirements, environment names, credentials, and local architecture choices stay in this project.

Before a significant change:

1. Application design questions are searched in `<path-to-app-dev-knowledge-base>`:
   `python "<path-to-app-dev-knowledge-base>\Search-Index\search.py" "<keywords>"`
2. Questions about briefing, searching, comparing, verifying, or recording AI-assisted work are searched in `<path-to-ai-knowledge-base>`.
3. Data engineering, data science, and CI/CD questions go to those repos.
4. Significant design choices name the options, then implement one.
5. The named check is run before the work is called done.
6. A reusable application lesson is written in `<path-to-app-dev-knowledge-base>`. An AI-tooling lesson is written in `<path-to-ai-knowledge-base>`.
```

Significant means an architecture choice, a public API, a UI contract, an application state model, or a security boundary. A narrow local fix can proceed from the code at hand.

Apply a lesson only when its status is `verified` and its environment still matches. Confirm language, platform, and protocol behavior against current docs when a lesson and the docs disagree. See [Official-Documentation/README.md](../Official-Documentation/README.md).
