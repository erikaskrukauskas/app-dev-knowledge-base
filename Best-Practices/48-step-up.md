---
title: Step-up authentication
tags: [practices, security]
status: tested
updated: 2026-10-17
---

# Step-up authentication

A sensitive action can require a fresh or stronger authentication even when the caller already has a session. The session alone is not permission for every action.

NIST SP 800-63B says: "authentication from an unexpected geolocation or IP address block (e.g., a cloud service) might prompt the use of additional risk-based controls." Checked 2026-10-17 at <https://pages.nist.gov/800-63-4/sp800-63b.html>.

NIST allows risk signals to prompt additional controls. They do not replace the authorization decision. See [Application security](06-application-security.md). Confirm the current authenticator levels before requiring a particular factor.

## Check

Call a sensitive action with a normal session and without the extra check. It is refused. The same action with the extra check succeeds when the caller is authorized.
