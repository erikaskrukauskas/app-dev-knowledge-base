---
title: Logging credentials
tags: [practices, security]
status: tested
updated: 2026-10-17
---

# Logging credentials

Logs, traces, and error reports do not contain passwords, tokens, session ids, or raw authorization material.

The Twelve-Factor App says: "A litmus test for whether an app has all config correctly factored out of the code is whether the codebase could be made open source at any moment, without compromising any credentials." Checked 2026-10-17 at <https://12factor.net/config>.

The twelve-factor litmus test is about credentials leaving the code. The same test applies to a log line that would be unsafe to publish. See [Password storage](34-password-storage.md) and [Application security](06-application-security.md).

## Check

Authenticate and trigger an error. The recorded diagnostic does not contain the credential.
