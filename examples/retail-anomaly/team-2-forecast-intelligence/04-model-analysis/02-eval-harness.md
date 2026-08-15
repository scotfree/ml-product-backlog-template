# Reproducible evaluation harness

`evaluate.py --model <version>` runs on locked test set, produces identical numbers every time.

### Upstream / Downstream contract

Team-internal: whoever owns metrics + harness + test-set management.

### Cross-team contact points

- **T1 Data** provides the test set (part of fixture bundle). Coordinate on split definitions.
- Timing: Week 3.

### Definition of Done

- Locked test set (hash-verified)
- Deterministic evaluation (seeded)
- Reports committed to `reports/<version>.md`

### Demo

Run harness twice on same model; identical numbers. Run on two model versions; comparison table.

### Subtasks

- Test-set locking
- Report generation
