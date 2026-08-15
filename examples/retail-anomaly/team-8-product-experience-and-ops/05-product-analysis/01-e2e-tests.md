# End-to-end tests (Playwright)

Automated browser tests that walk critical journeys: view anomaly list, drill to store, drill to product, open anomaly detail.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- Tests run against T7's backend in CI. Coordinate with T7 on a test-mode backend or seed data.
- Timing: Week 5 (initial), Week 8 (comprehensive).

### Definition of Done

- Playwright suite covers 3+ critical journeys
- Runs in CI on every PR
- Screenshots on failure

### Demo

Run the suite; walk through a passing run and one deliberately-failing case.

### Subtasks

- Playwright setup
- Journey tests
- CI integration
