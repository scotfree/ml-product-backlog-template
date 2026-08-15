# Design the canonical schema

Define the store-product-time schema every other team will consume. First-week Contract Gate output — this schema determines the shape of `sales.canonical.ready` and every downstream event.

### Upstream / Downstream contract

Team-internal: whoever owns dataset adapters (M5, Walmart, dunnhumby) needs the schema to know what to map into. Whoever owns validation writes checks against it.

### Cross-team contact points

- **T2 Forecast, T3 Graph, T4 Context, T5 Anomaly** all consume `sales.canonical.ready`. Confirm required fields with each before finalizing: T2 needs promotion/price/calendar; T3 needs store metadata (location, region, size); T4 needs store geography for weather joins; T5 needs clean time series with regular grain.
- **T7 Platform** needs the schema to register in the schema registry (Week 2).
- **T8 Product** needs to know which fields will render in the UI.
- Timing: schema v0.1 draft by Wednesday of Week 1; finalized by Friday. Team 1 co-owns the Contract Gate with T7.

### Definition of Done

- `docs/canonical-schema.md` published in the shared repo with field-by-field definitions
- One-page diagram showing schema versioning strategy (semver, backwards-compatibility rules)
- Sample event JSON matching the schema in `fixtures/sample_event.json`
- Sign-off from at least one representative on each downstream team (Teams 2, 3, 4, 5)

### Demo

Walk the cohort through the schema in the Contract Gate meeting; show the sample event; take questions from each downstream team lead.

### Subtasks

- Draft the schema based on M5 dataset structure + fields requested by downstream teams
- Circulate for review; collect gaps
- Publish v0.1 as fixture + schema doc
