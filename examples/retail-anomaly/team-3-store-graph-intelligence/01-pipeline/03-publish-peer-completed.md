# Publish peer.completed to Kafka

Service produces peer sets and deviation metrics per (store, product, time) task.

### Upstream / Downstream contract

Team-internal: modeling owner + serving owner.

### Cross-team contact points

- **T7 Platform** provides producer template.
- **T6 Explain** and **T8 Product** switch from mocks to real events at Foundation Gate.
- Timing: Week 3 Foundation Gate.

### Definition of Done

- Producer publishes peer.completed on canonical event trigger
- Idempotent (T7's pattern)
- Contract test in CI

### Demo

Live event flows: T1 publishes canonical → T3 publishes peer → T6 consumes.

### Subtasks

- Kafka producer via template
- Trigger logic (per canonical event or batch)
