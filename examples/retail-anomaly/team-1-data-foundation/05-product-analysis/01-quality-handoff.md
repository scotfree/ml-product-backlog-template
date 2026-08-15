# Data quality handoff

Automated checks that a fixture bundle or Kafka stream is usable before publishing it. Downstream teams shouldn't discover schema drift by breaking their own tests.

### Upstream / Downstream contract

Team-internal: validation is written against the canonical schema; each dataset adapter runs the validation before emitting.

### Cross-team contact points

- **All downstream teams** benefit from these checks running before releases. Publish quality reports alongside each fixture bundle version.
- Coordinate with **T7 Platform** on schema-registry validation as the runtime equivalent.
- Timing: Week 3 for fixtures; Week 5 for Kafka path.

### Definition of Done

- Pandera or Great Expectations suite covers schema, types, ranges, missing-field rules
- CI blocks fixture publication if suite fails
- Quality report emitted per bundle version, published to shared location

### Demo

Deliberately break a fixture; show CI catching it; fix; show it passing.

### Subtasks

- Quality rule authoring
- CI integration
- Report format and publication
