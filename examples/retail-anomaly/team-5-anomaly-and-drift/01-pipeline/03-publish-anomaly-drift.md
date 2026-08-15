# Publish anomaly.detected and drift.detected

Two producers. Both are triggered by canonical event flow; anomaly per-event, drift on a window.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T7 Platform** producer templates for both.
- **T6 Explain** and **T8 Product** switch from mocks at Foundation Gate.
- Timing: Week 3.

### Definition of Done

- Both producers idempotent
- Contract tests pass
- Publishing rate documented (drift is windowed, not per-event)

### Demo

Live scenario replay: anomalies flow to T6, drift to T8.

### Subtasks

- Anomaly producer
- Drift producer
- Windowing logic for drift
