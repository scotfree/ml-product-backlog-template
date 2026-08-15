# Design the peer.completed contract

Schema for peer output: peer_ids list, expected value from peers, per-peer weights (optional), deviation metric.

### Upstream / Downstream contract

Team-internal: modeling owner + serving owner co-design.

### Cross-team contact points

- **T6 Explain** consumes peer.completed as explanation evidence — "your sales are below peer stores." Confirm required fields: peer_ids, expected, deviation.
- **T8 Product** renders peer comparison. Ask what UI needs.
- **T7 Platform** registers the schema.
- Timing: Contract Gate (Week 1). Mock payload for T6 and T8 by Friday.

### Definition of Done

- Schema in shared repo
- Mock payload in `fixtures/peer_completed.example.json`
- T6/T8 sign-off

### Demo

Walk T6/T8 through the mock payload.

### Subtasks

- Draft schema
- Mock payload
- Downstream review
