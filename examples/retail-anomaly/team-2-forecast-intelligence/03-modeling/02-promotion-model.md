# Promotion-aware model (Paper 1)

LightGBM/XGBoost model with promotion-life-cycle features per Paper 1 (Hewage et al.). Beats baseline on promotion periods.

### Upstream / Downstream contract

Team-internal: feature owner adds promotion-life-cycle features; modeling owner trains + evaluates.

### Cross-team contact points

None directly for the model itself.

### Definition of Done

- Promotion-life-cycle features implemented (pre-promo, promo, post-promo)
- Model trained and evaluated against baseline on held-out promotion periods
- MLflow run logged with config

### Demo

Show error slice by promotion type — model should beat baseline meaningfully on promo periods.

### Subtasks

- Promotion-lifecycle feature engineering
- Training loop with sensible defaults
- Baseline comparison in a notebook
