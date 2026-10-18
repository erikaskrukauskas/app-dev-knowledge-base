---
title: Date and time contracts
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# Date and time contracts

A timestamp that means a moment is not a bare local clock time. Say whether the contract carries an instant or a civil date.

RFC 3339 says: "This document defines a date and time format for use in Internet protocols that is a profile of the ISO 8601 standard for representation of dates and times using the Gregorian calendar." Checked 2026-10-17 at <https://www.rfc-editor.org/rfc/rfc3339>.

## Instants

An instant includes the date, the time, and a numeric offset from UTC, or `Z` for UTC. Do not invent a second string shape for the same fact. Confirm the current profile before relying on a separator or a fraction of a second.

Store and compare instants on one timeline. Convert to a local zone only when a person reads the value. Two offsets that name the same instant compare equal.

## Civil dates

A calendar date with no time is not midnight UTC unless the contract says so. Day, month, and year order is a presentation choice. See [Internationalization](15-internationalization.md).

## Check

Write an instant from one offset and read it from another. The instant is unchanged. A date-only field round-trips as a date, not as a shifted instant.
