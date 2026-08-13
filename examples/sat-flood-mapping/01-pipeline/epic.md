# Epic: Pipeline (Sat-Flood-Mapping)

Move a Sentinel-2 tile through: acquisition (download or file-in) → tile preparation (band selection, cloud masking, normalization, reprojection to a canonical CRS) → foundation model inference → post-processing (probability threshold, connected components, small-region removal, vectorization) → georeferenced outputs (GeoTIFF for raster, GeoJSON for vector).

Every stage has a well-defined file-based interface. Geospatial data has an important extra constraint over other CV pipelines: **the CRS (coordinate reference system) must be tracked and preserved through the whole pipeline**, or georeferenced outputs won't align with the real world.

## Cards in this epic

1. Design the pipeline interface (with CRS handling)
2. Build a stub pipeline end-to-end
3. Replace stubs with real components (incremental)
