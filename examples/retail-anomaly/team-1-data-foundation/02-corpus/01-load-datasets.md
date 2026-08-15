# Load M5 and other main datasets

Reproducibly ingest M5 (primary), then Walmart and dunnhumby as secondary. Each dataset gets an adapter that emits canonical events.

### Upstream / Downstream contract

Team-internal: adapter authors work in parallel per dataset. Each adapter must produce identical canonical event shape regardless of source.

### Cross-team contact points

- Not directly cross-team, but the datasets chosen affect what fields are populated for **T2 Forecast** (promotion signals in M5) and **T4 Context** (weather joinability, which M5 lacks — flag this to T4 early).
- If T4 wants weather-joined data, only M5-EU or Walmart with defensible geographic mapping will support it.

### Definition of Done

- M5 loads end-to-end into canonical schema; deterministic (seeded)
- Two additional dataset adapters exist (Walmart, dunnhumby) with the same interface
- Each adapter has a unit test verifying schema conformance
- Documentation of which context fields each source populates

### Demo

Load 100 events from each dataset; show they conform to the same schema.

### Subtasks

- M5 adapter (primary)
- Walmart 45-store adapter
- dunnhumby Breakfast-at-the-Frat adapter
- Adapter interface / abstract base class
