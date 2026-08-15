# Observability stack (OpenTelemetry, Prometheus)

Prometheus scraping, OpenTelemetry traces, structured logs collected centrally. Every service exposes standard metrics.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T8 Product** builds Grafana panels on top. Coordinate metric names + labels early — renames break dashboards.
- **All service teams** must instrument their services to standard conventions. T7 provides a helper library or template.
- Timing: Week 5.

### Definition of Done

- Prometheus scraping every service
- OpenTelemetry traces flow to a collector
- Standard metric names documented

### Demo

T8's Grafana panel shows real metrics from T2/T5 services.

### Subtasks

- Prometheus setup
- OTel collector
- Metric naming doc
- Helper library
