# Design anomaly.detected and drift.detected contracts

Two schemas. anomaly.detected: score, type, evidence pointers, model version. drift.detected: score, persistent flag, hierarchy level (product/store/region).

### Upstream / Downstream contract

Team-internal: whoever owns anomaly + whoever owns drift co-design so evidence fields overlap where useful.

### Cross-team contact points

- **T6 Explain** is the primary consumer for anomaly.detected. Confirm anomaly type taxonomy and evidence field format with them.
- **T8 Product** renders both; drift.detected has a distinct UI treatment for persistence.
- **T7 Platform** registers both schemas.
- Timing: Contract Gate Week 1.

### Definition of Done

- Both schemas in repo
- Mock payloads for both
- T6/T8 sign-off

### Demo

Walk T6/T8 through mocks.

### Subtasks

- Draft schemas
- Mock payloads
- Downstream review
