# Failure-mode inventory

Enumerate what could go wrong in production. Sensor changes, domain shift, silent failures (all-zero predictions), infrastructure failures, and the special case of failing during an active flood event when the system matters most.

- **Upstream/downstream:** Feeds Card 08-monitoring-maintenance/02 (metrics to collect) and Card 07-documentation/02 (decisions log).
- **Definition of done:** `docs/failure-modes.md`: table of failure mode, symptom, detection, response. At least 10 entries.
- **Demo:** Walk through the top three; explain detection.
- **Subtasks:**
  - **Sensor drift:** Sentinel-2 radiometry drifts over years; model calibrated on 2018–2020 data may under- or over-predict in later years.
  - **Domain shift:** climate change and land-use change alter flood patterns. Regions not in Sen1Floods11 may generalize poorly.
  - **Silent failures:** model returns all-zero (no flood detected anywhere) or all-one (everything is flood) — much worse than a clear error.
  - **Catastrophic timing failures:** system down during a real flood event — worst-case outcome.
  - **Infrastructure:** GPU OOM on a large tile, storage full, network partition to the tile source.
  - **Sen1Floods11 label limits:** the training data doesn't include every flood type (e.g., snowmelt floods are under-represented). Document as a known limit.
