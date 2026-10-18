---
title: Verify, then record
tags: [practices, testing, lessons]
status: verified
updated: 2026-10-17
---

# Verify, then record

Call the work done only after the named check has run. Then record a lesson when a later application would otherwise repeat the investigation.

## The check

The check is the one named in the specification. See [Specify behavior and done](02-specify-behavior-and-done.md).

Use a test when the behavior can be asserted without a person: a contract, a state transition, an error, an authorization decision, or a regression that already failed once.

Use an exercised user path when the behavior is what a person sees and does: a screen flow, a keyboard path, a focus order, or an error message in context. Exercise the path. A screenshot of the first paint is not the check.

Run both when the change has a contract and a user-visible result. Testing the contract does not prove the path. Walking the path does not protect the contract from the next edit.

## Before calling it done

- The named check passed in this environment.
- The boundary in the specification was the boundary that changed.
- Failure behavior was checked, not only the success path.
- Accessibility behavior named for the change was part of the exercised path. See [Accessibility](08-accessibility.md).

## What to record

Add a file under `Lessons-Learned/` from [_template.md](../Lessons-Learned/_template.md) when the finding is an application lesson another project can reuse: a contract mistake, a state rule, a test that caught a real miss, an accessibility failure, or a security boundary.

Set `candidate` when the note is first written. Set `tested` when the check has been reproduced. Set `verified` when another session can apply it without rediscovering the dead ends.

Write an AI-tooling lesson in the [AI knowledge base](https://github.com/erikaskrukauskas/ai-knowledge-base), not here. If one effort produced both, write both and link them.

Leave a result that only makes sense inside one product in that project's notes. See [Practice versus project](05-practice-versus-project.md).
