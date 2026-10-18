---
title: Password storage
tags: [practices, security]
status: tested
updated: 2026-10-17
---

# Password storage

A password is not stored or logged as the password itself. The verifier stores a salted hash from a password hashing scheme, with a cost that can rise over time.

NIST SP 800-63B says: "Passwords SHALL be salted and hashed using a suitable password hashing scheme." Checked 2026-10-17 at <https://pages.nist.gov/800-63-4/sp800-63b.html>.

NIST SP 800-63-4 says verifiers shall store passwords in a form resistant to offline attacks, and the salt and hash are what the verifier keeps. This is not the same rule as keeping secrets out of git. See [Application security](06-application-security.md). Confirm the current SP before choosing a scheme.

## Check

Create an account and inspect the stored verifier. The stored value is not the password, and a second account with the same password does not share the same salt.
