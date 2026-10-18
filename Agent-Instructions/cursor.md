---
title: Cursor
tags: [agents, cursor]
status: verified
updated: 2026-10-17
---

# Cursor

Cursor reads this library when a project points at it. Product behavior for Cursor itself is documented in the [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base), not here.

## This repo

`AGENTS.md` at the root tells agents how to maintain the library: application knowledge only, frontmatter, lesson status, and no secrets or copied manuals.

## Other projects

Add the [consultation protocol](consultation-protocol.md) to the project's `AGENTS.md`. That file is the durable place for the search rule. A chat reminder disappears with the session.

Keep the protocol short. Link the practice pages instead of pasting them into the project.

## Search from a project

From any working directory:

```powershell
python "<path-to-app-dev-knowledge-base>\Search-Index\search.py" "architecture api"
```

Phase 2 can replace that command with an MCP tool. Until [MCP-Server/README.md](../MCP-Server/README.md) is built, use the script.

## Agent behavior

Questions about how Cursor should brief, search, compare, verify, or record work are searched in the AI knowledge base. Application design questions are searched here.
