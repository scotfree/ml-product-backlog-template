# Ranking sanity tests

Rank a curated set of anomalies (some obviously high-priority, some low). Confirm the priority formula produces the right ordering.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- Use T1's synthetic scenarios as test cases. High-severity scenarios should rank above low-severity.
- Timing: Week 5-6.

### Definition of Done

- Test suite with curated scenarios
- Expected orderings encoded
- Suite passes

### Demo

Show ranking on a mixed set; explain why the ordering makes sense.

### Subtasks

- Curate test cases
- Encode expected orderings
- Ranking test harness
