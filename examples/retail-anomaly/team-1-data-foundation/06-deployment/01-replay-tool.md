# Deterministic replay tool

A CLI that takes a fixture bundle or scenario config and replays events into Kafka at controlled speed. Used by T5/T8 for demos and by every team for local testing.

### Upstream / Downstream contract

Team-internal: consumes the fixture bundle + synthetic scenarios; produces to whichever Kafka the user points at.

### Cross-team contact points

- **T8 Product** depends on this for the Week 9 demo — the seeded scenario runs through here.
- **T5 Anomaly** uses it for evaluation reproducibility.
- **T7 Platform** provides the Kafka target; replay tool uses T7's producer conventions.
- Timing: Week 4; hardened by Week 8.

### Definition of Done

- `replay --scenario X --speed 10x` works end-to-end
- Deterministic: same seed + same scenario → identical event sequence
- Speed control (real-time, 10x, as-fast-as-possible)
- Documentation for T5 and T8 users

### Demo

Replay one anomaly scenario at 10x speed; T8's dashboard shows the anomaly appearing.

### Subtasks

- CLI framework
- Scenario loader
- Rate control
