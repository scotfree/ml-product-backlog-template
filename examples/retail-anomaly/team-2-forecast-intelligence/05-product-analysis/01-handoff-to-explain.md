# Handoff test — T6 consumes real forecasts

T6 has been developing on mock forecasts. First real integration test: their explanation service consumes T2's real events.

### Upstream / Downstream contract

Team-internal: whoever owns the service ensures schema matches spec.

### Cross-team contact points

- **T6 Explain** is the counterparty. Schedule a paired session in Week 4 to run the pipeline end-to-end: T2 publishes → T6 consumes → T6 produces explanation using T2's fields.
- Any field T6 needs that isn't in the schema is a bug in T2's Pipeline card 01.
- Timing: Week 4 (after Foundation Gate).

### Definition of Done

- Paired session completed; T6 successfully consumes real forecasts
- Any field mismatches logged as issues and fixed
- T6 confirms the schema meets their needs

### Demo

T6 team member runs their consumer against T2's live producer; explanation is generated.

### Subtasks

- Schedule the session
- Prepare a live test scenario
- Fix any issues surfaced
