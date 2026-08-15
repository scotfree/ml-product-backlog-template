# Data quality monitoring

Automated checks running against the live canonical stream. Detect fixture-vs-stream drift, missing fields, out-of-range values, delayed events.

### Upstream / Downstream contract

Team-internal: quality-check suite from Product Analysis reused as monitoring.

### Cross-team contact points

- **T7 Platform** provides Prometheus/OpenTelemetry hooks — coordinate metric names and label conventions early.
- **T8 Product** displays data-quality panel in the technical Grafana view.
- Timing: Week 5 (initial), Week 8 (hardened for demo).

### Definition of Done

- Metrics: event rate, schema-conformance rate, delayed-event count, per-source event ratio
- Alerts documented (thresholds, escalation)
- Grafana panel in the technical view

### Demo

Deliberately publish a malformed event; show the alert firing in Grafana.

### Subtasks

- Metric emission from the producer
- Grafana panel definition
- Alert rules
