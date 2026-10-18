---
title: Search index
tags: [retrieval, search]
status: verified
updated: 2026-10-17
---

# Search index

Phase 1 retrieval is keyword search over the markdown in this repo. It uses the Python standard library and does not need PostgreSQL, an embedding model, or a running server.

Semantic search belongs with the MCP service in Phase 2. See [MCP-Server/README.md](../MCP-Server/README.md).

## Commands

From the repo root:

```powershell
python Search-Index/search.py --list
python Search-Index/search.py "application security"
python Search-Index/search.py --tag architecture
python Search-Index/search.py --status verified "testing"
```

`--list` prints every document's path, status, title, and tags. A query requires every keyword to appear in the file. `--tag` and `--status` filter YAML frontmatter. `--tag` matches when the tag appears in the `tags` field. `--status` matches the `status` field exactly, ignoring case.

The script skips `.git`, `.venv`, `__pycache__`, and this `Search-Index` folder, so this page is not itself a search hit.

## How to think about a miss

A miss means no page used those words. Try the terms from the task (`architecture`, `api`, `state`, `testing`, `security`) or list the catalog and open the closest title. Add the missing words to the page that should have matched, or write the page if the topic is new. See [Write findable pages](../Best-Practices/07-write-findable-pages.md).

## What this search will not do

- It does not search the AI knowledge base or other sibling repos.
- It does not search the web or official docs.
- It does not rank by meaning. A synonym that never appears in the file will not hit.
