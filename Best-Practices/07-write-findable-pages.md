---
title: Write findable pages
tags: [practices, retrieval, search]
status: verified
updated: 2026-10-17
---

# Write findable pages

Write each page so a later keyword search can find it. The Phase 1 search matches words and frontmatter. It does not infer synonyms.

## One topic per page

Give the page one decision a future application can apply. If a draft covers architecture and secrets and test style, split it and link the pages.

Link to the canonical page instead of copying its rules into a second file. Agent pointers in `Agent-Instructions/` stay short for this reason.

## Words a search can match

Use the words a later project will type: `architecture`, `api`, `state`, `testing`, `accessibility`, `error`, `security`, `contract`.

- Put those words in the title, the tags, and the opening paragraphs when they are the topic.
- Tags are lowercase search words. Prefer the term the rest of the library already uses.
- If a search for the obvious phrase misses the page that should have answered it, add the missing words to that page.

## Frontmatter

Every page starts with `title`, `tags`, `status`, and `updated`. A lesson also has `id`, `environment`, `scope`, and `superseded_by`.

Status moves from `candidate` to `tested` to `verified`. When a newer page replaces this one, set status to `superseded`, set `superseded_by` to the replacement path, and keep the file.

## After adding a page

Search for the topic before you finish:

```powershell
python Search-Index/search.py "the words a project would use"
python Search-Index/search.py --tag architecture
```

Update the index in [Best-Practices/README.md](README.md) or [Lessons-Learned/README.md](../Lessons-Learned/README.md) so a reader can open the page without guessing the file name. The search script skips `Search-Index/` itself. See [Search-Index/README.md](../Search-Index/README.md).
