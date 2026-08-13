# Logging and metrics in production

Structured JSON logs (per-tile). Aggregate metrics (daily): tiles processed, flood pixels predicted per tile, prediction confidence distribution, error/warning counts. Silent-failure detection: flag if flood-pixel-count stays at 0 across many tiles (probably a model regression).

- **Upstream/downstream:** Ops team monitors these. Documentation captures the log format.
- **Definition of done:** System emits structured JSON logs on stdout. Aggregate metrics exposed via Prometheus-compatible endpoint or written to a shared time-series store. A dashboard shows daily tile counts and prediction stats.
- **Demo:** Show the dashboard; explain what a healthy day looks like vs. what an anomaly looks like.
- **Subtasks:**
  - Log format: JSON, one line per tile, includes tile_id, CRS, prediction stats.
  - Aggregate metrics: tiles/day, avg flood fraction, silent-failure counter.
  - Confidence distribution: track how the histogram of model confidences shifts over time — a sharp shift indicates domain drift.
  - Simple alerts: "no tiles processed in last 6h", "flood-pixel-count = 0 for 100 consecutive tiles".
