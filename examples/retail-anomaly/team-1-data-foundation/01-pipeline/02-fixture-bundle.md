# Publish the fixture bundle

A versioned bundle of Parquet/JSON fixtures that every team pulls from the repo. Non-blocking rule: every team must be able to develop from fixtures alone, even if Kafka is down.

### Upstream / Downstream contract

Team-internal: whoever owns dataset ingestion writes the bundle-generation script; whoever owns validation ensures fixtures pass all checks.

### Cross-team contact points

- **All 7 other teams** consume this bundle. Update path: `fixtures/canonical/v{N}/` in the shared repo. Semver bump for any breaking change.
- Timing: initial bundle by end of Week 1 (small M5 slice, ~100 events). Main bundle by end of Week 2 (representative sample across regions/products).
- Risk: if fixtures are late or unstable, every research team is delayed.

### Definition of Done

- `fixtures/canonical/v0.1/` contains: Parquet event files, sample JSON, schema.json, README explaining structure
- Versioning strategy documented; changelog entry per version bump
- CI check verifies fixture validity against schema

### Demo

Show a downstream team member (e.g., T5) loading the fixture bundle in their notebook without any Kafka running.

### Subtasks

- Bundle generation script
- Schema validation in CI
- Publish to a shared, versioned path
