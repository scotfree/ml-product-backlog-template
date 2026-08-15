# Design the forecast.completed contract

Schema for the forecast event: expected value, prediction interval, model version, feature snapshot.

### Upstream / Downstream contract

Team-internal: feature owner + modeling owner co-design the schema so it captures what the model actually produces.

### Cross-team contact points

- **T6 Explain** consumes `forecast.completed` as evidence for explanations. Confirm they get: expected, lower, upper, model_version. Include feature importances if available.
- **T8 Product** renders expected-vs-actual and interval widths. Confirm the UI needs.
- **T7 Platform** registers the schema.
- Timing: Contract Gate (Week 1). Mock payload published for T6 and T8 by Friday.

### Definition of Done

- Schema JSON in shared repo
- Mock payload in `fixtures/forecast_completed.example.json`
- T6 and T8 sign-off on required fields

### Demo

Walk T6 and T8 through the mock payload; confirm they can build UI components against it.

### Subtasks

- Draft schema
- Mock payload
- Downstream review
