---
title: Best practices index
tags: [practices, index, architecture]
status: verified
updated: 2026-10-17
---

# Best practices

These pages are the stable application-development rules. Lessons in `Lessons-Learned/` are evidence from real work. When a lesson holds beyond the original project, fold the reusable part into a page here and link the lesson to that page.

| Guide | Use it when |
| --- | --- |
| [Consult before a design choice](01-consult-before-design.md) | About to choose architecture, a contract, state, or a security boundary |
| [Specify behavior and done](02-specify-behavior-and-done.md) | Writing the change an application must make |
| [Compare before choosing](03-compare-before-choosing.md) | Choosing an architecture, a public API, or a state model |
| [Verify, then record](04-verify-and-record.md) | Deciding the work is done, or saving a lesson |
| [Practice versus project](05-practice-versus-project.md) | Deciding whether a decision belongs in this repo |
| [Application security](06-application-security.md) | Handling input, access, or secrets |
| [Write findable pages](07-write-findable-pages.md) | Adding a page a later search should find |
| [Accessibility](08-accessibility.md) | Naming what a person must be able to perceive, operate, and understand |
| [Error contracts](09-error-contracts.md) | Telling a caller what failed and whether state changed |
| [Idempotent operations](10-idempotent-operations.md) | Deciding whether a retry applies a command twice |
| [Conditional updates](11-conditional-updates.md) | Stopping a stale write from overwriting a newer one |
| [API compatibility](12-api-compatibility.md) | Changing a public API without breaking an existing caller |
| [Date and time contracts](13-date-and-time.md) | Carrying an instant or a civil date |
| [Stable identifiers](14-stable-identifiers.md) | Giving a caller an identity that survives rename and reorder |
| [Internationalization](15-internationalization.md) | Keeping user-facing text in the reader's language |
| [Paging collections](16-paging-collections.md) | Reading a collection without an unbounded list |
| [Response caching](17-response-caching.md) | Saying which responses may be reused, and by whom |
| [Deprecating a contract](18-deprecating-a-contract.md) | Warning callers before an old behavior stops |
| [Safe operations](19-safe-operations.md) | Keeping a read from changing stored state |
| [Creation results](20-creation-results.md) | Returning the identity of a resource a command just created |
| [Accepted work](21-accepted-work.md) | Accepting a command whose effect is not finished yet |
| [Redirect contracts](22-redirect-contracts.md) | Sending a caller to another URI |
| [Content negotiation](23-content-negotiation.md) | Choosing one representation of the same resource |
| [Partial responses](24-partial-responses.md) | Returning only a byte range of a representation |
| [Rate limits](25-rate-limits.md) | Telling a caller they sent too many requests |
| [Oversized requests](26-oversized-requests.md) | Rejecting a request that exceeds a published size |
| [Media types](27-media-types.md) | Naming the format of a representation |
| [Null and absent](28-null-and-absent.md) | Distinguishing a missing member from an explicit null |
| [Duplicate member names](29-duplicate-member-names.md) | Rejecting an object that repeats a member name |
| [URI identity](30-uri-identity.md) | Treating a URI as the identity of a resource |
| [Language tags](31-language-tags.md) | Labeling the language of an information object |
| [Unicode normalization](32-unicode-normalization.md) | Comparing text after one normalization form |
| [Text segmentation](33-text-segmentation.md) | Counting and cutting text on user-perceived characters |
| [Password storage](34-password-storage.md) | Storing a password so a stolen database is not the password |
| [Currency codes](35-currency-codes.md) | Naming money with an international currency code |
| [Country codes](36-country-codes.md) | Identifying a country with a standard code |
| [Time zones](37-time-zones.md) | Naming a place's local-time rules |
| [Caller-supplied URLs](38-caller-supplied-urls.md) | Fetching a URL a caller provided |
| [Config versus code](39-config-versus-code.md) | Keeping deploy-specific values out of code |
| [Referrer policy](40-referrer-policy.md) | Limiting what a navigation sends as a referrer |
| [Cache vary](41-cache-vary.md) | Telling a cache which request fields select the representation |
| [Sensitive response storage](42-sensitive-response-storage.md) | Stopping caches from storing a sensitive response |
| [Derived representations](43-derived-representations.md) | Keeping one stored fact and treating other views as derived |
| [Read your writes](44-read-your-writes.md) | Letting the writer observe the state just written |
| [Single writer](45-single-writer.md) | Giving each stored fact one writer |
| [Credential guessing](46-credential-guessing.md) | Throttling repeated attempts to guess a secret |
| [Recovery codes](47-recovery-codes.md) | Storing backup codes as hashes and invalidating them once used |
| [Step-up authentication](48-step-up.md) | Asking for a stronger check before a sensitive action |
| [Address formats](49-address-formats.md) | Accepting addresses that do not match one country's layout |
| [Action links](50-action-links.md) | Advertising what a caller can do next with link relations |
| [Idempotency window](51-idempotency-window.md) | Remembering a completed command long enough for a retry |
| [Exactly-once claims](52-exactly-once-claims.md) | Describing delivery as at least once plus an idempotent effect |
| [Side effects after commit](53-side-effects-after-commit.md) | Sending an external effect only after the state write is durable |
| [Stored event contracts](54-stored-event-contracts.md) | Treating a stored event as a contract for later consumers |
| [Expand then contract](55-expand-then-contract.md) | Changing stored shape in an order readers can survive |
| [Identifier reuse](56-identifier-reuse.md) | Not issuing a retired identifier to a new fact |
| [Minor units](57-minor-units.md) | Storing money in the currency's minor unit |
| [Redirect targets](58-redirect-targets.md) | Allowing only known redirect destinations |
| [Logging credentials](59-logging-credentials.md) | Keeping credentials out of logs |
| [Published descriptions](60-published-descriptions.md) | Checking behavior against a published API description |
| [Batch item results](61-batch-item-results.md) | Reporting success and failure per item in a batch |
| [Body size limits](62-request-size-for-bodies.md) | Rejecting a body over the published maximum |
| [Audit actor](63-audit-actor.md) | Recording who performed a privileged change |
| [Field errors](64-problem-details-per-field.md) | Pointing a validation error at the field that failed |
| [Sort order](65-sort-order.md) | Choosing an explicit order for a collection |
| [Filter contracts](66-filter-contracts.md) | Saying which filters a collection accepts |
| [Sort tie breaks](67-sort-tie-breaks.md) | Making equal sort keys deterministic |
| [Field selection](68-field-selection.md) | Letting a caller ask for a subset of fields |
| [Unknown values](69-unknown-values.md) | Deciding what a reader does with a value it does not know |
| [Case sensitivity](70-case-sensitivity.md) | Stating whether letter case changes identity |
| [Correlation identifiers](71-correlation-ids.md) | Carrying one identifier across a call and its logs |
| [Clock skew](72-clock-skew.md) | Allowing a bounded difference between clocks |
| [Backfill](73-backfill.md) | Filling a new fact on old records before readers require it |
| [Soft delete](74-soft-delete.md) | Hiding a fact without reusing its identifier |
| [Personal data deletion](75-personal-data-deletion.md) | Removing a person's data on a valid request |
| [Personal data export](76-personal-data-export.md) | Giving a person a copy of the data held about them |
| [Impersonation](77-impersonation.md) | Acting as another user without hiding the real actor |
| [Session end](78-session-end.md) | Making logout invalidate the server-side session |
| [Account enumeration](79-account-enumeration.md) | Not revealing whether an account exists |
| [Upload bounds](80-upload-bounds.md) | Limiting what an upload may contain |
| [Percentages](81-percentages.md) | Stating the base a percentage is of |
| [Rounding mode](82-rounding-mode.md) | Naming how a value is rounded |
| [Draft versus committed](83-draft-versus-committed.md) | Keeping an uncommitted draft out of the committed fact |
| [Pessimistic locking](84-pessimistic-locking.md) | Holding a lock so others cannot write until release |
| [Cancellation](85-cancellation.md) | Stopping accepted work that has not finished |
| [Unsaved changes](86-unsaved-changes.md) | Warning before discarding a person's unsaved edits |
| [Preserve form input](87-preserve-form-input.md) | Keeping what the person typed when validation fails |
| [Destructive confirmation](88-destructive-confirmation.md) | Confirming an action that removes or sends something irreversible |
| [Empty states](89-empty-states.md) | Showing what an empty collection means |
| [Loading states](90-loading-states.md) | Showing that a result is not ready yet |
| [Module boundaries](91-module-boundaries.md) | Keeping a module from reaching into another module's store |
| [Dependency direction](92-dependency-direction.md) | Pointing dependencies toward more stable contracts |
| [Feature flags](93-feature-flags.md) | Turning unfinished behavior off by default |
| [Documented defaults](94-documented-defaults.md) | Making a default part of the contract |
| [Monotonic reads](95-monotonic-reads.md) | Not showing an older value after a newer one |
| [Bounded staleness](96-bounded-staleness.md) | Stating how old a read may be |
| [Concurrent sessions](97-concurrent-sessions.md) | Saying whether one person may have multiple sessions |
| [Offline queue](98-offline-queue.md) | Replaying commands made while disconnected |
| [Timeout budgets](99-timeout-budgets.md) | Giving each outbound call a deadline |
| [Backpressure](100-backpressure.md) | Slowing producers when consumers are behind |
| [Read-only mode](101-read-only-mode.md) | Rejecting writes during a declared read-only period |
| [Tenant isolation](102-tenant-isolation.md) | Keeping one tenant from reading another tenant's facts |
| [Retention period](103-retention-period.md) | Deleting data after a stated retention period |
| [Consent records](104-consent-records.md) | Recording the consent a person gave |
| [Token audience](105-token-audience.md) | Accepting a token only for its intended audience |
| [Revocation](106-revocation.md) | Making a revoked credential fail before its expiry |
| [Maker checker](107-maker-checker.md) | Requiring a second person to approve a sensitive write |
| [Conflict copy](108-conflict-copy.md) | Keeping both sides when an automatic merge is unsafe |
| [Notification versus state](109-notification-versus-state.md) | Treating a notification as a hint to read state |
| [Duplicate delivery](110-duplicate-delivery.md) | Handling the same message more than once |
| [Poison messages](111-poison-messages.md) | Parking a message that fails every attempt |
| [Ignore unknown fields](112-ignore-unknown-fields.md) | Letting readers skip fields they do not know |
| [Command versus query](113-command-versus-query.md) | Separating a command that changes state from a query that does not |
| [Quota versus rate](114-quota-versus-rate.md) | Separating a count of resources from a rate of calls |
| [Receipt immutability](115-receipt-immutability.md) | Not rewriting a record that was issued as a receipt |
| [Sequence gaps](116-sequence-gaps.md) | Detecting a missing number in an ordered stream |
| [Default deny](117-default-deny.md) | Refusing an action that no rule explicitly allows |
| [Permission cache](118-permission-cache.md) | Bounding how long a cached permission may be reused |
