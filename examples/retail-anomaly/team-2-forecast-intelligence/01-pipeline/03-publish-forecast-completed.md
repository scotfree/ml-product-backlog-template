# Publish forecast.completed to Kafka

The service reads features/canonical events, runs the current model, publishes forecasts.

### Upstream / Downstream contract

Team-internal: modeling owner + serving owner coordinate on inference loop and model loading.

### Cross-team contact points

- **T7 Platform** provides Kafka producer and schema-registry validation.
- **T6 Explain** and **T8 Product** were using mock payloads until this ships — Foundation Gate switches them to real events.
- Timing: Week 3 Foundation Gate.
- Risk: if late, T6/T8 stay on mocks; low integration risk since schema was agreed Week 1.

### Definition of Done

- Service consumes canonical events and publishes forecast.completed
- Idempotent producer (T7's pattern)
- Contract test in CI passes

### Demo

Point the service at a running Kafka; T6's consumer receives forecasts.

### Subtasks

- Service wraps model + T7 template
- Idempotency guarantee
- CI contract test
