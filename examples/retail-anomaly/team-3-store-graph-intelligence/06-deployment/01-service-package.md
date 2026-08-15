# Package the graph service

FastAPI service (T7 template) + optional Neo4j backend. Runnable in Compose.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T7 Platform** provides service template and Compose. If Neo4j chosen, T7 provides it in Compose.
- Timing: Week 3-4.

### Definition of Done

- `docker compose up graph` works
- Health endpoint
- Neo4j (if used) migrations reproducible

### Demo

Cold start the service; peer request returns peers.

### Subtasks

- Wrap model
- Dockerfile
- Neo4j migrations (if applicable)
