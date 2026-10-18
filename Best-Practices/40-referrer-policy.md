---
title: Referrer policy
tags: [practices, security]
status: tested
updated: 2026-10-17
---

# Referrer policy

A document states how much of its URL may be sent as a referrer. Secrets and capability tokens do not ride along to another site.

W3C Referrer Policy says: "This document describes how an author can set a referrer policy for documents they create, and the impact of such a policy on the Referer HTTP header for outgoing requests and navigations." Checked 2026-10-17 at <https://www.w3.org/TR/referrer-policy/>.

The copy checked on 2026-10-17 is a Candidate Recommendation from 2017, and that copy says later documents may supersede it. Confirm the current specification before relying on a policy token.

## Check

Navigate from a page that holds a token in its URL. The outgoing referrer does not include the token.
