# Publish canonical events to Kafka

Real Kafka producer for `sales.canonical.ready`. Consumed by the four research teams once they're ready to integrate.

### Upstream / Downstream contract

Team-internal: dataset ingestion → validation → serialization → publish. The ingestion pipeline can run in "batch" (fixtures) or "stream" (Kafka) mode from the same code path.

### Cross-team contact points

- **T7 Platform** provides Kafka + service template + producer conventions. Depend on T7's Week 2 deliverable (versioned schemas + contract tests).
- **T2, T3, T4, T5** consume `sales.canonical.ready`. Each has their own timeline; T1's producer must be stable before Foundation Gate (Week 3).
- Timing: Week 3 Foundation Gate.
- Risk: if this slips, research teams remain on fixtures — recoverable but delays end-to-end integration.

### Definition of Done

- `sales.canonical.ready` published to Kafka with schema-registry-validated payload
- Idempotency guarantee documented (T7 requirement)
- Contract test in shared CI passes
- Consumer example in `examples/consume_canonical.py` (Python) that any team can copy

### Demo

Run the producer against the shared Kafka; show a T5 team member's consumer receiving events in real time.

### Subtasks

- Wire the ingestion pipeline into T7's producer template
- Register schema with T7's registry
- Contract test coverage
