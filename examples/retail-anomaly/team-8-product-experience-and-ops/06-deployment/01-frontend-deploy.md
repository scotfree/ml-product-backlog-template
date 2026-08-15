# Frontend deployment

Build + deploy the React app. Dockerized; runs in the same Compose stack as everything else.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T7 Platform** provides Compose stack. T8's service joins it.
- Timing: Week 3-4.

### Definition of Done

- Dockerized production build
- Compose entry
- Environment variable wiring for backend URL

### Demo

`docker compose up ui`; UI accessible on documented port.

### Subtasks

- Dockerfile
- Compose entry
- Build optimization
