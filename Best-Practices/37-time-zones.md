---
title: Time zones
tags: [practices, contracts]
status: tested
updated: 2026-10-17
---

# Time zones

A local time is interpreted with a time zone identifier from the IANA time zone database, not with a fixed offset stored as if the rules never change.

IANA Time Zone Database says: "The Time Zone Database (often called tz or zoneinfo) contains code and data that represent the history of local time for many representative locations worldwide." Checked 2026-10-17 at <https://www.iana.org/time-zones>.

An instant still uses [Date and time contracts](13-date-and-time.md). The zone id is how a future local time is resolved. The database is updated when governments change offsets. Confirm the current tz release before relying on a zone's rules. The 2026e release was dated 2026-09-29.

## Check

Schedule a local time in a zone that has a daylight-saving change and resolve it to an instant. The instant matches the zone rules, not a stale fixed offset.
