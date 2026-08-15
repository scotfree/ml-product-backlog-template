# Mock-first UI shell

Full UI shell built entirely from mocked API responses. Every screen renderable from fixtures alone.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **All producing teams** provide mock payloads by end of Week 1 (their Contract Gate output). T8 builds against those.
- Non-blocking rule: T8 must never wait for a live producer. Missing fields render as "not available."
- Timing: Week 1.

### Definition of Done

- UI shell renders from `fixtures/*.example.json` only
- Every screen documented with which fixtures it uses
- No hardcoded connection to a live backend

### Demo

Clone the repo; `npm start`; UI renders full anomaly list from mocks.

### Subtasks

- Component scaffolding
- Fixture-driven data layer
- Documentation
