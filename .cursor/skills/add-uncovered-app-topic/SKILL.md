---
name: add-uncovered-app-topic
description: >-
  Add a missing application-development topic to this knowledge base after
  confirming no page covers it. Use when the user asks to document, add, or
  update this knowledge base on a topic it does not yet cover, including
  architecture, design patterns, API or UI contracts, application state,
  coding standards, testing, accessibility, error handling, or application
  security.
---

# Add an uncovered application topic

Add one new application-development topic. If a page already answers it, edit that page. Refreshing a covered page from current sources uses [review-covered-app-topics](../review-covered-app-topics/SKILL.md).

Do not commit or push unless the user asks.

## Decide where it goes

Read [SCOPE.md](../../../SCOPE.md). Add the topic here only when a future application in an unrelated project could reuse it.

Stop and name the other home when the topic is:

- How an agent should brief, search, compare, verify, or record work: the AI knowledge base
- Data engineering, data science, or CI/CD: that repo
- One product's requirements, environment names, credentials, or local architecture: that project

## Confirm it is uncovered

From the repo root:

```bash
python Search-Index/search.py --list
python Search-Index/search.py "topic words"
```

Search `Best-Practices/`, `Lessons-Learned/`, `Official-Documentation/`, `Agent-Instructions/`, and `Books/`. Ignore hits under `.cursor/`.

A page that answers the question means the topic is covered. Edit that page, or follow [review-covered-app-topics](../review-covered-app-topics/SKILL.md) when the task is to refresh it.

A near match is still covered when the missing part is a paragraph, not a new decision. Add the paragraph there.

## Research before writing

Open the current official page with WebSearch or WebFetch. Start from [Official-Documentation/README.md](../../../Official-Documentation/README.md), then open the section that supports the rule. Confirm that page before relying on a feature.

A blog or community post is a lead. Confirm it on an official page before writing it as a practice.

Quote only the sentence needed, with the URL. Do not paste a manual, a book chapter, or a secret.

Stay stack-neutral. A framework, language, or platform belongs on an official-doc pointer, not as the practice itself.

## Write one page

Follow [Write findable pages](../../../Best-Practices/07-write-findable-pages.md).

| Kind of knowledge | Where to put it |
| --- | --- |
| Stable rule another application can apply | Next numbered file in `Best-Practices/`, plus a row in its README |
| Pointer to current language, UI, HTTP, accessibility, or testing docs | A row or a short note under `Official-Documentation/` |
| Citation and original notes for a book | A catalog row and `Books/notes/<slug>.md` |
| Finding from a checked change | Next `LL-####` file, using `Lessons-Learned/_template.md` |

One topic per page. Link the canonical page instead of copying it. Tags are lowercase search words. Set `updated` to the day you write the page.

Status:

- `candidate` when the only support is an unconfirmed lead
- `tested` when you opened the current official page and the new page states the rule with that URL and the date checked
- `verified` only when the check named on the page was run, or the user explicitly asks for `verified`

Do not mark a lesson `verified` unless that check was run. A new lesson starts as `candidate` or `tested`.

## Finish

Search the words a later project would type and confirm the new page hits. Update the index README for the folder you changed.

```markdown
# Topic added
- Page:
- Why it was uncovered:
- Primary source: [title](url)
- Status:
```

If you refused the topic, say where it belongs.
