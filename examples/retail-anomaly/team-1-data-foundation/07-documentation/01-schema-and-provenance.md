# Schema and provenance documentation

Living doc that describes the canonical schema, its versioning, source dataset provenance, and any synthetic modifications. Downstream teams read this to understand what they're consuming.

### Upstream / Downstream contract

Team-internal: schema owner keeps it updated; validation owner cross-references it.

### Cross-team contact points

- Every consuming team relies on this doc. When schema changes (even backwards-compatible), the doc must be updated in the same PR that changes the schema. T7's contract-test CI should enforce this.
- Timing: initial by end of Week 1; kept live through Week 6 schema freeze.

### Definition of Done

- `docs/canonical-schema.md`: field definitions, semver policy, changelog
- `docs/data-provenance.md`: source datasets, license notes, synthetic scenario provenance
- Both linked from the top-level project README

### Demo

Point a T2 or T4 team member at the docs during Foundation Gate; they can find any field they need without asking.

### Subtasks

- Schema field doc
- Provenance doc
- CI check for doc-schema sync
