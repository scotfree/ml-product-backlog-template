# Integration and edge-case tests

What happens with: a tile that's mostly clouds? A tile of ocean (all water but no flood)? A snow-covered tile? A tile with missing bands? A corrupt input GeoTIFF? A tile with an unusual CRS? Pipeline should degrade gracefully — never silently produce garbage, always report clearly.

- **Upstream/downstream:** Deployment needs to know the failure modes. Documentation (Card 08-monitoring-maintenance/01) inherits this as the failure-mode inventory.
- **Definition of done:** `tests/edge_cases/` covers each named case. Pipeline handles gracefully (produces output + warning) or fails with a clear log message. No silent failures.
- **Demo:** Trigger 2–3 edge cases live; show either graceful handling or clear failure.
- **Subtasks:**
  - Mostly-cloud tile (should return "insufficient valid pixels" warning).
  - Ocean tile (all water — model should predict permanent water or refuse, not flood).
  - Snow-covered tile (SWIR similar to water — real risk of false positives).
  - Salt flat / dry lake bed (from error analysis in Model Analysis Card 03).
  - Missing bands (only 3 or 4 of the required 6 available).
  - Corrupt or unreadable GeoTIFF.
  - Unusual CRS (something other than WGS84 or a common UTM zone).
