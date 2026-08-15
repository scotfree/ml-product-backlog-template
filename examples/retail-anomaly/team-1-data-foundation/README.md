# Team 1 — Data Foundation

Trustworthy, reproducible retail data and realistic test scenarios so every other team can build and evaluate independently from Week 1.

## Applicable epics

Team 1 owns the data foundation, so several ML-team epics don't apply:

- **Pipeline** ✓ — canonical data pipeline (ingest → validate → publish)
- **Corpus** ✓ — dataset adapters and synthetic scenario generation
- **Modeling** ✗ (no ML model)
- **Model Analysis** ✗ (no model)
- **Product Analysis** ✓ — data quality and handoff to consuming teams
- **Deployment** ✓ — replay tool, Kafka producer, fixtures
- **Documentation** ✓ — schema docs, provenance, run instructions
- **Monitoring & Maintenance** ✓ — data quality monitoring, drift alerts

## Cross-team role

Data Foundation is upstream of every research team (2, 3, 4, 5) via `sales.canonical.ready`, and provides shared fixtures + synthetic scenarios to essentially the entire cohort. See `cross-team-contact-points.xlsx` — Team 1 appears as owner in 5 rows and as dependency in another ~10.
