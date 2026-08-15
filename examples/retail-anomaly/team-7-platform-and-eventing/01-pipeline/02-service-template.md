# Reusable service template

Copy-pasteable FastAPI service with Kafka producer/consumer, health endpoints, structured logging, test suite. Every research team uses this as a starting point.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T2, T3, T4, T5, T6** all base their services on this template.
- Non-blocking rule: template is **copy-pasteable, not imported**. Teams shouldn't depend on a live version of the template evolving during development.
- Timing: Week 1 (basic), Week 2 (with contract tests).

### Definition of Done

- Template repo (or template subdirectory) with a working example service
- Documented setup instructions
- Includes: producer, consumer, health endpoint, logging, test scaffolding

### Demo

Copy the template; rename it; run it; publish an event.

### Subtasks

- Template scaffolding
- Documentation
- Example test
