# Consume canonical events + store metadata

Peer discovery needs store metadata (location, size, region) plus historical sales.

### Upstream / Downstream contract

Team-internal: whoever ingests events + whoever loads metadata.

### Cross-team contact points

- **T1 Data** must include store metadata in fixture bundle. Confirm which fields are available in M5/Walmart datasets — flag any gaps in Week 1.
- Timing: fixtures Week 1; Kafka Week 3.

### Definition of Done

- Store metadata loaded from fixtures
- Historical sales accessible per store
- Same code path for fixture and Kafka modes

### Demo

Show peer similarity computed from fixture data.

### Subtasks

- Metadata loader
- Historical sales joiner
- Similarity computation
