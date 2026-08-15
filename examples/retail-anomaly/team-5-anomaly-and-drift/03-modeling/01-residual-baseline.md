# Residual/z-score baseline

Simple detector: forecast (internal simple forecast, not T2's) → residual → z-score threshold. Permanent fallback.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- Explicitly does NOT wait for T2's forecast. Use an internal seasonal-naive forecast for residuals.
- Timing: Week 1-2.

### Definition of Done

- Internal simple forecast
- Residual z-score computation
- Threshold documented

### Demo

Inject anomaly; z-score exceeds threshold; anomaly emitted.

### Subtasks

- Internal forecaster
- Residual computation
- Threshold picker
