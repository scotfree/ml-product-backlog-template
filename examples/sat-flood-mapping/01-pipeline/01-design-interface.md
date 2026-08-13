# Design the pipeline interface (with CRS handling)

Sketch the stages and the type each hands to the next. The extra decision here vs. non-geospatial pipelines: which stages preserve the CRS, which stages resample to a canonical CRS, and how metadata flows alongside the raster data.

- **Upstream/downstream:** Consumer is a downstream system that will overlay flood extents on maps or ingest them into a GIS. That system needs the outputs georeferenced correctly.
- **Definition of done:** `docs/pipeline.md` with a diagram, file format at each boundary (COG for rasters, GeoJSON for vectors), CRS handling policy documented (e.g., "preserve source CRS through inference; reproject to EPSG:4326 only at export").
- **Demo:** Walk the team through the diagram in 2 minutes; specifically point out where the CRS is tracked and where reprojection happens.
- **Subtasks:**
  - Decide directory layout: `runs/<event_id>/raw/`, `runs/<event_id>/prepped/`, `runs/<event_id>/predictions/`, `runs/<event_id>/vector/`.
  - Confirm input format: Sentinel-2 L1C or L2A? (L2A is atmospherically corrected — usually what Prithvi wants.) Which bands, in what order?
  - Confirm output CRS convention (EPSG:4326 for portability; native UTM for local accuracy).
  - Flag which stages need `rasterio` / `geopandas` vs. plain numpy.
  - Cite the source data assumption: 6 bands (Blue, Green, Red, Narrow NIR, SWIR1, SWIR2) per Prithvi's pretraining — see [Prithvi-EO-2.0 paper](https://arxiv.org/abs/2412.02732), §3.
