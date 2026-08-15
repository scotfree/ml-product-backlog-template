# SHAP quality checks

Where feature-based explanations use SHAP (from T2's model exports), ensure they're stable and consistent across similar cases.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T2 Forecast** must expose SHAP-computable interface for their model. Coordinate on what's feasible with their chosen model.
- Timing: Week 4-5.

### Definition of Done

- SHAP explanations for at least T2's model
- Stability check: similar cases produce similar explanations
- Documented limitations

### Demo

Two similar anomalies; show similar explanations.

### Subtasks

- SHAP integration with T2's model
- Stability tests
