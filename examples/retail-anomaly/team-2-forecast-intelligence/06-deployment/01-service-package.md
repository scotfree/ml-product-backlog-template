# Package the forecast service

FastAPI service (T7 template) that loads the current model and publishes forecasts. Runnable via Docker Compose.

### Upstream / Downstream contract

Team-internal: modeling owner + serving owner.

### Cross-team contact points

- **T7 Platform** provides the service template and Docker Compose integration point.
- Timing: Week 3-4.

### Definition of Done

- Service runs via `docker compose up forecast`
- Health endpoint (T7 convention)
- Graceful startup (model loading) and shutdown (SIGTERM)

### Demo

Cold-start the service in Compose; publish a canonical event; observe forecast.completed appear on Kafka.

### Subtasks

- Wrap model in service
- Health endpoint
- Dockerfile
