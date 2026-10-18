---
title: Recovery codes
tags: [practices, security]
status: tested
updated: 2026-10-17
---

# Recovery codes

A recovery code is stored as a one-way hash, shown to the person once, and rejected after it has been used.

NIST SP 800-63B says: "Saved recovery codes SHALL be stored in the subscriber account in hashed form using an approved one-way function" Checked 2026-10-17 at <https://pages.nist.gov/800-63-4/sp800-63b.html>.

NIST also says the verifier shall invalidate that code after use and issue a new one. Do not store the code next to the password hash in reversible form.

## Check

Use a recovery code once. A second use fails, and the stored value is not the code itself.
