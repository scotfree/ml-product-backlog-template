# Context contradiction score

When actuals contradict what context would predict (hot day + low sales despite normally weather-sensitive product), emit a high contradiction score.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T6 Explain** uses this as strong evidence for the manager view. Confirm the scoring range and what "high" means with them.
- Timing: Week 4-5.

### Definition of Done

- Contradiction score defined
- Scoring on held-out data shows meaningful separation between contradicting/non-contradicting cases
- Documented in `docs/contradiction-score.md`

### Demo

Two examples: one strong contradiction, one no contradiction. Show the scores.

### Subtasks

- Score formula
- Sanity check on labeled examples
