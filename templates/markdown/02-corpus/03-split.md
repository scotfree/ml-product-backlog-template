# Split train / validation / test with a rationale

## Description

_A split you can defend. Document why._

## Upstream / Downstream contract

- _Analysis will use the test set; training will use the others._
- _Anyone touching data needs to respect the split._

## Definition of Done

_Split is deterministic (seeded), documented, and enforced in code so nobody accidentally trains on test._

## Demo

_Show the split logic and the guardrails preventing test-set contamination._

## Subtasks

- _Decide split ratios and any stratification._
- _Add a "fast loop" sub-sample for quick iteration._

## Estimate

_Rough size — minutes, hours, or days. If it's more than a few days, break it up._
