# Package the anomaly + drift services

Two services (or one with two producers). Compose-ready.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T7 Platform** provides template.
- Timing: Week 3-4.

### Definition of Done

- `docker compose up anomaly drift`
- Health endpoints
- Model loading at startup

### Demo

Cold start; scenarios flow through and produce events.

### Subtasks

- Wrap models
- Dockerfiles
- Compose entries
