# CRP Fixtures

## Purpose
Fixtures validate implementations against the specification. They do not define protocol behavior.

## Fixture Layout
- manifest.json
- expected.receipt (committed, immutable)
- meta.json (optional, versioned)

## Generation
Use reference Rust impl. Commit only after local reproducibility.

## Update Policy
New fixtures on spec version bump. No rewriting history. CI SHALL fail on regeneration attempts.

## CI Integration
Fetch official fixtures. Byte-compare. Fail-closed.