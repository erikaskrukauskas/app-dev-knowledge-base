---
title: Compare before choosing
tags: [practices, architecture, api, state]
status: verified
updated: 2026-10-17
---

# Compare before choosing

Name the real options before choosing an architecture, a public API, or an application state model. Then implement one.

## When a comparison is required

Compare when more than one design could satisfy the stated behavior and the choice will be expensive to reverse:

- Architecture: how responsibilities are split across modules or processes, and which boundary owns each rule.
- Public API: the operations, the payload shape, the errors, and what a later caller may rely on.
- State model: which facts are stored, which are derived, who may write them, and how a reader sees a consistent result.

A local rename, a private helper, or a bug fix with one obvious edit does not need a written comparison.

## What to write down

For each option, record:

- The behavior it satisfies, using the words from [Specify behavior and done](02-specify-behavior-and-done.md).
- What it makes easy and what it makes hard for the next change.
- The contract it exposes and the contract it hides.
- The check that would show this option is wrong.

Reject an option that cannot meet the named check. Do not keep it in the comparison to look thorough.

## Then implement one

Pick one option and build that option. Record the rejected options in the project decision or, when the comparison is reusable, in a lesson. Do not implement two architectures in the same change and leave the caller to discover which one is live.

## What does not belong in the comparison

- A framework, language, or host platform treated as the architecture. Those are implementation choices. Confirm current behavior in [Official-Documentation/README.md](../Official-Documentation/README.md) when the choice depends on one.
- A project-only constraint, such as an environment name or an existing vendor account, written up here as if every application had it. See [Practice versus project](05-practice-versus-project.md).
