# Grafana panels for technical view

Kafka lag, service latency/error rates, model inference times, DB health. The "operations dashboard" for the demo.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T7 Platform** provides Prometheus + OpenTelemetry. Depend on their standard metric names.
- **Every service team** must be instrumented per T7's conventions or their panel will be empty.
- Timing: Week 5 initial; Week 8 hardened.

### Definition of Done

- Grafana dashboard covers: Kafka lag, service latency (p50/p95), error rates, DB connections, inference times
- Loads without errors
- Panels populated from real metrics

### Demo

Show the dashboard live during Week 9 demo alongside manager view.

### Subtasks

- Panel definitions
- Metric queries
- Dashboard export
