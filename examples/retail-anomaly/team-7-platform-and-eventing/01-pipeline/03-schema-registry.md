# Schema registry + contract tests

Each producing team registers their event schema; contract tests in CI verify producer output conforms.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T1, T2, T3, T4, T5, T6** all register schemas. Producer team owns their schema; T7 provides the validation harness.
- Timing: Week 2 (registry + tests); Week 3 (all core producers registered).

### Definition of Done

- Schema registry available (Confluent-style, or a lightweight repo-based equivalent)
- Contract test template that a producer team can adopt in <30 min
- CI blocks merges that break schema conformance

### Demo

Deliberately publish a malformed event; contract test fails.

### Subtasks

- Registry setup
- Contract test template
- CI integration
