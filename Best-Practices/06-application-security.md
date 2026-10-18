---
title: Application security
tags: [practices, security, architecture]
status: verified
updated: 2026-10-17
---

# Application security

Treat input as untrusted, decide access at an explicit boundary, and keep secrets out of git.

## Input handling

Validate at the trust boundary where data enters the application: a request, a message, a file, or a user field. State what is accepted, what is rejected, and what the caller observes on rejection.

- Check type, length, range, and allowed values before the value is used in a query, a path, a command, or a response.
- Encode output for the context that will interpret it. Validation on the way in does not make every later context safe.
- Do not rely on a client, a hidden field, or a disabled control as the only check. Those are convenience for an honest caller.

The specification names the rejection behavior. The check covers both an accepted value and a rejected one. See [Specify behavior and done](02-specify-behavior-and-done.md).

## Authentication and authorization

Authentication answers who the caller is. Authorization answers what that caller may do. Keep the two decisions separate.

- Perform authorization on the server side of the trust boundary, on every operation that reads or changes protected state.
- Authorize the specific action and the specific resource. A successful login is not permission for every operation.
- Fail closed: a missing identity, a missing permission, or an uncertain decision denies the operation and returns the error the contract defines.
- Do not scatter the same permission rule across the UI and the API with no single owner. The UI may hide an action. The boundary that owns the data must still enforce it.

## Secrets

Do not commit secrets. That includes API keys, tokens, passwords, connection strings, and private certificates.

- Load them from the project's secret manager or from a local file ignored by git.
- `.gitignore` ignores `.env` and `.env.*` as a backstop. The rule is still: do not add those files.
- A sample file may list the variable names with placeholder values. It must not contain a live secret.
- A lesson may name the variable and the approved place it is loaded from. It must not contain the secret value so the next session can "just work."

## What this page does not decide

It does not choose a token format, a framework filter, or a cloud product. Compare those options in the project when the behavior above is already specified, and confirm the current product docs before relying on a feature. See [Official-Documentation/README.md](../Official-Documentation/README.md).
