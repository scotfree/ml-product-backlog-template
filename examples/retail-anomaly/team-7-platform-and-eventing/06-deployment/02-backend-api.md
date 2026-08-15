# Backend query API for the dashboard

REST API that T8 queries for anomaly lists, drill-downs, historical data.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T8 Product** is the primary consumer. Coordinate on endpoints, pagination, filter semantics.
- **T6 Explain** writes to Postgres; API reads from Postgres to serve T8.
- Timing: Week 3 (initial); Week 5 (full).

### Definition of Done

- OpenAPI spec published
- Reference endpoints implemented (anomalies list, single-anomaly detail, filters)
- T8 successfully queries it

### Demo

T8 runs a Playwright test that hits the real API.

### Subtasks

- Endpoint design
- Implementation
- OpenAPI docs
