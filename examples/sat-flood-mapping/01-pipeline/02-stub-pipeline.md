# Build a stub pipeline end-to-end

Every stage returns fake-but-CRS-valid data: a canned 512×512 Sentinel-2-shaped GeoTIFF (6 bands, real CRS metadata), a stub cloud mask that passes everything, a stub inference that returns random probabilities, real post-processing, real vector export.

- **Upstream/downstream:** No external dependencies blocked. Vector output can be loaded in QGIS or `geopandas` to validate the CRS handling.
- **Definition of done:** `python -m flood_mapping run --input <tif> --out <dir>` runs to completion in seconds. The output GeoJSON opens in QGIS with correct georeferencing.
- **Demo:** Run the pipeline on the canned input; load output in QGIS; show the stub flood polygons in the right geographic location.
- **Subtasks:**
  - Canned Sentinel-2-shaped GeoTIFF in `tests/fixtures/`.
  - Stub cloud mask, stub inference (returns valid-shape probabilities).
  - Real post-processing (threshold, connected components, `shapely` polygonization).
  - Real GeoTIFF/GeoJSON export via `rasterio` / `geopandas` — validates the CRS handling end-to-end.
