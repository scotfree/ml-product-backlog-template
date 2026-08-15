# Package the explanation service

FastAPI service that runs the aggregation loop. Compose-ready.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T7 Platform** provides template and persistence (Postgres for explanation storage).
- Timing: Week 3-4.

### Definition of Done

- Service runs in Compose
- Persistence to Postgres works
- Producers emit to T7-provided topics

### Demo

Full flow: T5 anomaly → T6 explanation stored → T8 dashboard shows it.

### Subtasks

- Service wrapper
- Postgres schema + migration (T7 coord)
- Dockerfile
