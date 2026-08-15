# Consume signals from four teams

Main pipeline: subscribe to anomaly.detected (T5 primary trigger); enrich with forecast.completed (T2), peer.completed (T3), context.completed (T4), drift.detected (T5) as available.

### Upstream / Downstream contract

Team-internal: whoever owns the consumer loop + whoever owns evidence-joining logic.

### Cross-team contact points

- **T5 Anomaly** — primary trigger. All others are secondary evidence.
- **T2 Forecast, T3 Graph, T4 Context, T5 Drift** — optional evidence. Every field is optional; missing signals degrade gracefully. This is the key architectural discipline for this card.
- Timing: mocks Week 1; real events for each team as they come online (Weeks 3-4).

### Definition of Done

- Consumer loop subscribes to all five topics (T5 anomaly + 4 evidence)
- Evidence joined by (store, product, time) key with tolerance window
- Missing evidence handled cleanly (empty fields, not errors)

### Demo

Kill T4's producer; T6 still emits explanations, just without context evidence.

### Subtasks

- Kafka consumer for each topic
- Join logic with tolerance window
- Graceful degradation for missing signals
