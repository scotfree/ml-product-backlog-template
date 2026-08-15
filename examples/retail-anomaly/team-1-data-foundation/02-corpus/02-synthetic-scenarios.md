# Synthetic scenario catalog

Deterministic, labeled scenarios that inject anomalies: sudden drops, missing promo uplift, peer divergence, weather contradiction, gradual drift. Used by T5 for evaluation and T8 for demo.

### Upstream / Downstream contract

Team-internal: whoever owns the synthetic generator + whoever owns the scenario catalog documentation.

### Cross-team contact points

- **T5 Anomaly** needs these scenarios to compute Precision/Recall/F1 on their detectors. Confirm the anomaly types they need to distinguish before finalizing the catalog (Week 2 sync).
- **T6 Explain** and **T8 Product** need scenarios for demo cases — a "drop despite favorable weather" makes a compelling manager-view demo.
- Timing: initial catalog Week 3 (Foundation Gate); expanded Week 4.
- Risk: if late, T5 falls back to injecting locally — usable but not shared, and demo scenarios weaken.

### Definition of Done

- `synthetic/scenarios/` directory with one config file per scenario type
- Each scenario deterministic (seeded); replay produces identical events
- Scenario labels documented (which events are anomalies, what type)
- T5 confirms scenarios cover their evaluation needs

### Demo

Run one scenario end-to-end; show the injected anomaly appearing in the event stream with a labeled ground-truth marker.

### Subtasks

- Scenario DSL / config format
- Injection logic for each scenario type
- Ground-truth labels emitted alongside events
- Documentation and examples
