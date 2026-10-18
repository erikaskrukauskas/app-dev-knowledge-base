---
title: Credential guessing
tags: [practices, security]
status: tested
updated: 2026-10-17
---

# Credential guessing

Online attempts to guess a password, a code, or a recovery secret are throttled. The application does not offer an unlimited number of tries.

NIST SP 800-63B says: "The verification of saved recovery codes SHALL be subject to the throttling requirements in Sec. 3.2.2." Checked 2026-10-17 at <https://pages.nist.gov/800-63-4/sp800-63b.html>.

NIST requires throttling for saved recovery codes and says centrally stored passwords are hashed because offline guessing is fast. Confirm the current throttling limits in SP 800-63B before copying a number into a project. See [Rate limits](25-rate-limits.md) for ordinary traffic.

## Check

Submit many wrong secrets. Further attempts are refused before the secret space is exhausted, and a correct secret is not locked out forever without a stated recovery.
