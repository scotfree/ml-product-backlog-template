# Kafka + Postgres via Docker Compose

The shared runtime. Every team must be able to `docker compose up` and get Kafka + Postgres running locally.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **All 7 other teams** depend on this. First-week deliverable.
- Timing: Contract Gate (Week 1).
- Risk: if late, every team's integration path is blocked. But teams can develop from fixtures — this is only blocking for integration testing.

### Definition of Done

- `docker-compose.yml` starts Kafka (or Redpanda) + Postgres + minimum tooling
- Documented ports, credentials, connection strings
- Any team member can start the stack in <5 minutes with a fresh checkout

### Demo

Fresh clone; `docker compose up`; publish + consume test event.

### Subtasks

- Compose file
- Documentation
- Smoke test
