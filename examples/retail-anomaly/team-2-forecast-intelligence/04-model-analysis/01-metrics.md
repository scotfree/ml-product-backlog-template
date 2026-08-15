# Define evaluation metrics

MAE/RMSE headline; MAPE for interpretation; interval coverage/width for uncertainty; error slices by promotion, store, product.

### Upstream / Downstream contract

Team-internal: metrics owner + modeling owner + eval-harness owner align.

### Cross-team contact points

- Coordinate with **T5 Anomaly** on whether they'll use forecast residuals (optional per spec). If yes, expose residual computation cleanly.
- Timing: metrics doc by Week 2; eval harness Week 3.

### Definition of Done

- `docs/metrics.md`: what, why, thresholds
- Includes slice breakdowns (promotion, store, product)
- Baseline naive-forecast reference values documented

### Demo

Show metrics table for baseline vs Paper-1 model.

### Subtasks

- Metric definitions
- Slicing utilities
- Baseline reference computation
