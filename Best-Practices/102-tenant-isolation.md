---
title: Tenant isolation
tags: [practices, security, architecture]
status: candidate
updated: 2026-10-17
---

# Tenant isolation

A fact belongs to a tenant. A caller authenticated for one tenant does not read or write another tenant's fact, even with a guessed identifier.

No current official page was opened for this rule. Confirm a primary source before treating it as tested.

Authorization names the tenant and the resource. See [Application security](06-application-security.md).

## Check

Authenticate as tenant A and request tenant B's identifier. The call is refused and the body does not contain B's data.
