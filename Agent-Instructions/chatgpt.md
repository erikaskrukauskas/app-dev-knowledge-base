---
title: ChatGPT
tags: [agents, chatgpt]
status: verified
updated: 2026-10-17
---

# ChatGPT

ChatGPT uses the same application practices and lessons. The connection method differs. Product behavior for ChatGPT itself is documented in the [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base), not here.

## Now

Work that starts in ChatGPT can still use this library:

- Retrieve the relevant page locally with `Search-Index/search.py`.
- Paste the relevant section into the ChatGPT task, with the file path.
- Ask ChatGPT to follow that section.

That keeps one canonical copy. A summary pasted into a chat is not a second source of truth.

## Later

Remote use needs an authenticated connector and an explicit decision about which documents are exposed. A local MCP config on this PC is not automatically visible to ChatGPT. See [MCP-Server/README.md](../MCP-Server/README.md).

## Same rules

ChatGPT output that will be reused is still subject to [Verify, then record](../Best-Practices/04-verify-and-record.md). A suggestion becomes a lesson after a check, not when the chat ends. Application lessons are written here. AI-tooling lessons are written in the AI knowledge base.
