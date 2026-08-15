# Consume canonical events + synthetic scenarios

Time-series consumer. Handles both real canonical events and T1's synthetic scenario replay.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T1 Data** provides canonical events + synthetic scenarios. Confirm scenario labels are attached to events (or emitted as sidecar events).
- Timing: Week 1 (fixtures + local injection); Week 2 (T1's synthetic replay); Week 3 (Kafka).

### Definition of Done

- Time-series consumer for canonical events
- Scenario labels usable for evaluation
- Works from fixtures + Kafka + T1's replay

### Demo

Replay one T1 scenario; anomaly detected with correct label.

### Subtasks

- Kafka consumer template (T7)
- Fixture reader
- Scenario label handling
