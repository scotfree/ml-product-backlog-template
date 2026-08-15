# Threshold drift monitoring

Detection thresholds may need adjustment over time as data changes. Log threshold, actual anomaly rate, and predicted-vs-actual FP rate.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T8 Product** may display FP-rate trend in the technical view.
- Timing: Week 7-8 (stretch).

### Definition of Done

- Metrics emitted for thresholds and rates
- Documented recalibration process

### Demo

Show FP rate creeping up over time in Grafana; recalibrate; rate drops.

### Subtasks

- Metric emission
- Recalibration script
