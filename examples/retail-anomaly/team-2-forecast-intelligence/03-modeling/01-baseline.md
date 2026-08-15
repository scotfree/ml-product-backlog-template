# Naive/seasonal baseline

Simple baseline (seasonal naive or per-store average) that everything else compares against. Permanent demo fallback.

### Upstream / Downstream contract

Team-internal: baseline owner writes the model; evaluation owner defines the metric to beat.

### Cross-team contact points

None directly. The baseline's *outputs* still fit the `forecast.completed` schema (see Pipeline card 01).

### Definition of Done

- Baseline model implementation
- Reproducible run script (`scripts/train_baseline.py`)
- MLflow run logged

### Demo

Show baseline forecast on a held-out slice; compare to actuals visually.

### Subtasks

- Seasonal naive implementation
- Per-store average as alternative baseline
- MLflow logging
