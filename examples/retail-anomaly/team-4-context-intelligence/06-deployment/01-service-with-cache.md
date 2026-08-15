# Context service with weather cache

Service consumes canonical events, joins cached weather, publishes context.completed.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T7 Platform** provides service template.
- Timing: Week 3-4.

### Definition of Done

- Service runs via Compose
- Weather cache accessible in container
- Health endpoint

### Demo

Cold start; context.completed appears for a canonical event.

### Subtasks

- Wrap into service
- Cache mount
- Dockerfile
