# Split train / validation / test with a rationale

_A split you can defend. Document why._

- **Upstream/downstream:** _Analysis will use the test set; training will use the others. Anyone touching data needs to respect the split._
- **Definition of done:** _Split is deterministic (seeded), documented, and enforced in code so nobody accidentally trains on test._
- **Demo:** _Show the split logic and the guardrails preventing test-set contamination._
- **Subtasks:**
  - _Decide split ratios and any stratification._
  - _Add a "fast loop" sub-sample for quick iteration._
