# Retry / idempotency / DLQ strategy

Documented pattern for how producers/consumers handle failures. Poison messages go to DLQ, not to logs.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **All producing teams** must follow the idempotency pattern. Include in the service template (Pipeline card 02).
- **All consuming teams** must handle retries per the pattern.
- Timing: Week 4 (docs + pattern), Week 5 (DLQ topics per producer).

### Definition of Done

- `docs/retries-dlq.md` explains pattern
- Service template implements it
- DLQ topics exist per producer
- Documented recovery from DLQ

### Demo

Publish a poison message; observe it land in DLQ; document how to reprocess.

### Subtasks

- Pattern doc
- Template integration
- DLQ setup
