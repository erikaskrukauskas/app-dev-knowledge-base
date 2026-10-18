---
title: Config versus code
tags: [practices, architecture]
status: tested
updated: 2026-10-17
---

# Config versus code

Values that change between deploys live outside the code. Code does not contain credentials, hostnames, or other per-deploy handles.

The Twelve-Factor App says: "Config varies substantially across deploys, code does not." Checked 2026-10-17 at <https://12factor.net/config>.

The twelve-factor config page says a codebase should be openable without compromising credentials. Environment-specific names still stay in the project, not in this library. See [Practice versus project](05-practice-versus-project.md) and [Application security](06-application-security.md).

## Check

Search the source for a live credential or a deploy hostname. The only hits are placeholders.
