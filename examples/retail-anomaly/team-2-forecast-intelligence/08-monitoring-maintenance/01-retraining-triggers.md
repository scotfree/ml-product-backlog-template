# Retraining triggers

Document when the forecast model should be retrained: rolling window recency, MAE degradation threshold, seasonal boundary.

### Upstream / Downstream contract

Team-internal: modeling owner defines triggers; MLOps owner (if any) implements.

### Cross-team contact points

- **T5 Anomaly** may signal drift.detected — decide whether that triggers retraining automatically or requires human review.
- Timing: Week 7-8 (stretch).

### Definition of Done

- `docs/retraining.md` defines triggers and process
- At least one trigger tested end-to-end (even if manual)

### Demo

Simulate MAE degradation; retraining trigger fires; new model trained.

### Subtasks

- Trigger definitions
- Retraining script
