---
title: MCP server design
tags: [mcp, retrieval, roadmap]
status: candidate
updated: 2026-10-17
---

# MCP server

Phase 2 adds a local MCP server so an agent can search this library from any project. Phase 1 uses [Search-Index/search.py](../Search-Index/search.py) instead. This page is the contract to build against. The server is not implemented yet.

Do not add PostgreSQL, pgvector, FastAPI, or book ingestion in Phase 1. Those choices wait until keyword search has been used enough to show what it misses.

## Why a server later

Keyword search already works on one machine. An MCP server is worth adding when agents in other projects should call a tool instead of remembering a Python path.

## Proposed tools

| Tool | Purpose |
| --- | --- |
| `search_knowledge` | Keyword search first. Returns paths, titles, status, and a short snippet. Every keyword must match. Optional tag and status filters read frontmatter. |
| `get_document` | Return one markdown file by repo-relative path. |
| `list_lessons` | Filter lessons by status, tag, and environment. |
| `record_lesson` | Create a candidate lesson from the template. It must not set status to `verified`. |

`record_lesson` writes a file under `Lessons-Learned/` with `status: candidate` and the next unused `LL-` id. A person or a later review promotes it to `tested` or `verified` after the check in the lesson has been run.

Tools read and write only this repository. They do not search the AI knowledge base or other domain repos unless a later, explicit tool is added for that.

## Deployment order

1. Local process on this PC, started by the agent client, with the repo path as configuration.
2. Optional packaging after the four tools behave like `search.py` and the lesson template.
3. Authenticated remote access only after you decide which documents may leave the machine.

ChatGPT does not automatically see a local MCP server. Remote access is a separate phase. See [ChatGPT](../Agent-Instructions/chatgpt.md).

## Data rules the server must keep

- Do not index `.env` files, PDFs, or anything outside the markdown library.
- Skip `.git`, `.venv`, `__pycache__`, and `Search-Index`, matching the Phase 1 script.
- Return `superseded` documents only when the query asks for them.
- Include `status` in every hit so the caller can prefer `verified`.
- Refuse to store secret-shaped values in `record_lesson`.
- Refuse to mark a new lesson `verified`.

## Open choices

- Whether `record_lesson` only writes the file for review, or also commits it. Phase 1 does not commit from this design.
- Whether a later ranking pass is worth adding after keyword misses are recorded as lessons.
- The auth design for any future remote API.

Resolve those when Phase 2 starts, using the lessons collected from Phase 1 search.
