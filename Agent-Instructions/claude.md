---
title: Claude Code
tags: [agents, claude]
status: verified
updated: 2026-10-17
---

# Claude Code

Claude Code should follow the same consultation steps as Codex. Product behavior for Claude Code itself is documented in the [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base), not here.

## Instructions

Add the [consultation protocol](consultation-protocol.md) to the global `CLAUDE.md`. Use the project's `CLAUDE.md` for constraints that are true only in that repository.

Do not paste a second copy of the practice pages into `CLAUDE.md`. Link to the page in this repo.

## Search until MCP exists

```powershell
python "<path-to-app-dev-knowledge-base>\Search-Index\search.py" --status verified "<keywords>"
```

When the local MCP server from [MCP-Server/README.md](../MCP-Server/README.md) exists, register that server in Claude's MCP configuration. Do not create a second copy of this library for Claude.

## Lessons

When Claude finds a reusable application result, it writes the lesson here with status `candidate` or `tested`, using the template. It does not mark the lesson `verified` until the check in the lesson has been run. An AI-tooling lesson goes to the AI knowledge base.
