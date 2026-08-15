# Switch to live backend

Config switch that swaps mock data for T7's backend API. Same components; different data source.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T7 Platform** provides backend API. Depend on their Week 3 initial and Week 5 full versions.
- If backend is late, UI stays on mocks. Non-blocking.
- Timing: Week 3 (initial), Week 5 (full).

### Definition of Done

- Env-based switch: `REACT_APP_BACKEND=mock|live`
- Live mode queries T7's API
- No component changes required

### Demo

Toggle env var; UI switches from mock to live seamlessly.

### Subtasks

- Data layer abstraction
- Env config
- Integration testing
