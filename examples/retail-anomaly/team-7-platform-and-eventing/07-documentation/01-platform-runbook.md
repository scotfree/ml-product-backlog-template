# Platform runbook

Operational doc: how to start the stack, how to restart a broken service, how to check Kafka lag, what to do when the DLQ fills up.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **All teams** consult this when things break. Referenced during Week 9 demo operations.
- Timing: continuously updated; hardened Week 8.

### Definition of Done

- `docs/runbook.md` covers startup, recovery, common failure modes
- Every failure documented in the failure-mode inventory has a recovery step here

### Demo

During Demo-Readiness, deliberately break something; recover using only the runbook.

### Subtasks

- Author runbook
- Test it (deliberately break, follow steps)
