# Agent Discovery

Agent discovery answers one question:

> What durable roles materially improve this project's correctness or efficiency beyond the generic agent family?

It is not an inventory of technologies.

## Evidence order

Project-analyzer should inspect, where present:

1. project instructions and README;
2. architecture/security/decision records;
3. handoff and design documents;
4. source boundaries with concentrated business/domain logic;
5. tests, especially regression, permission, performance, and integration tests;
6. build/deployment configuration;
7. issue/task history only when it clarifies recurring work.

## Discovery dimensions

Assess:
- technical stack,
- architecture boundaries,
- domain/business rules,
- security/authority boundaries,
- performance or operational contracts,
- UI/accessibility contracts,
- external specifications,
- human-owned decisions,
- recurring review needs.

## Specialist threshold

Create/recommend a durable specialist only when all are substantially true:
- the capability is distinct from generic implementation/review;
- the need is recurring;
- mistakes are meaningfully costly or difficult to detect;
- dedicated context or expertise improves outcomes.

Prefer one-off delegation when the need is rare.

Do not split by technology mechanically. For example, Django + SQLite + Docker does not imply three specialists if one application engineer can safely own all three.

## Domain specialists

A domain specialist is warranted when code correctness depends heavily on interpreting business rules, regulations, contracts, scientific rules, game rules, financial logic, operational doctrine, or another non-trivial domain source.

A domain specialist must distinguish:
- documented rule,
- implementation assumption,
- unresolved interpretation,
- human-owned decision.

Unresolved interpretations are escalated; they are not invented.
