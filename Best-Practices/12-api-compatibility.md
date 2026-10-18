---
title: API compatibility
tags: [practices, api, contracts]
status: tested
updated: 2026-10-17
---

# API compatibility

Declare the public API, and treat a change that breaks an existing caller as a different version.

Semantic Versioning says: "Software using Semantic Versioning MUST declare a public API." Checked 2026-10-17 at <https://semver.org/>. It also says to increment the major version when you make incompatible API changes, and the minor version when you add functionality in a backward-compatible manner.

## What is incompatible

Incompatible means an existing caller, using the contract you already published, no longer works. Removing a field, changing the meaning of an accepted value, or rejecting a value you used to accept is incompatible. Adding a field that old callers can ignore is compatible.

Once a version has been released, do not change that release in place. SemVer says the contents of a released version must not be modified. Ship the correction as a new version.

Name the public API in the specification. See [Specify behavior and done](02-specify-behavior-and-done.md). A removal that callers must prepare for is [deprecation](18-deprecating-a-contract.md), not a silent edit.

## Check

Run the previous caller, or a fixture of its requests, against the new version. A compatible change still passes. An incompatible change is only offered where the old caller can stay on the previous version.
