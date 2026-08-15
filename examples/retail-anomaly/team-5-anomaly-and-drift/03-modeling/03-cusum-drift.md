# CUSUM/statistical drift detection

DriftGuard-inspired: monitor forecast error over time; CUSUM detects persistent shifts.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- Uses internal forecast residuals (same as anomaly baseline). No T2 dependency.
- Timing: Week 3-4.

### Definition of Done

- CUSUM implementation
- Threshold tuned
- Persistence flag output

### Demo

Show a scenario where a short spike doesn't trigger drift, but a sustained shift does.

### Subtasks

- CUSUM implementation
- Persistence logic
- Sanity tests
