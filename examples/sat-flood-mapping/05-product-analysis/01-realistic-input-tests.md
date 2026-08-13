# End-to-end tests on real recent floods

Pick 3–5 flood events from *after* Sen1Floods11's date range (post-2020) with well-documented public news coverage. Download the corresponding Sentinel-2 tiles from Copernicus Open Access Hub. Run the full pipeline; compare predictions to news reports and other flood mapping sources (Dartmouth Flood Observatory, humanitarian OpenStreetMap).

- **Upstream/downstream:** Deployment consumes results as go/no-go signal. Feeds back to Modeling if a systematic gap becomes obvious (e.g., "our model always misses urban flooding").
- **Definition of done:** `tests/realistic/` with the 3–5 recent events, source Sentinel-2 tiles, and a report per event (predicted flood extent, comparison to news/humanitarian data).
- **Demo:** Show one clear success (e.g., correctly identifying flooding from a well-documented event) and one honest failure or partial-miss.
- **Subtasks:**
  - Pick events with high public visibility (major news coverage → easy sanity check).
  - Download Sentinel-2 L2A tiles via `sentinelsat` or the Copernicus Data Space browser.
  - Compare qualitatively (visual overlay on a basemap) and quantitatively where reference data exists (Dartmouth Flood Observatory hand-drawn boundaries).
  - "Success" here is systemic, not pixel-perfect — did the pipeline produce a georeferenced flood polygon that a first responder could use?
