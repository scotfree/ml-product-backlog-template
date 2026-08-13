# Replace stubs with real components (incremental)

Swap one stub at a time. Order: (1) real cloud masking (usually simple: Sentinel-2 L2A includes a scene classification band), (2) real preprocessing (reprojection, resampling, normalization), (3) real inference (Prithvi via TerraTorch — the biggest swap).

- **Upstream/downstream:** Each swap depends on the corresponding Corpus (02) and Modeling (03) cards being done.
- **Definition of done:** Real component passes the same interface tests as the stub. `pytest tests/` still green after each swap.
- **Demo:** For each swap, show the pipeline running with the new real stage; compare output raster/vector against the stub.
- **Subtasks:**
  - One card per stub-to-real swap.
  - Cloud masking: use Sentinel-2 SCL band or `s2cloudless`.
  - Preprocessing: reprojection with `rasterio.warp`, per-band normalization matching Prithvi's pretraining stats.
  - Inference: TerraTorch model loading + tiled prediction (Prithvi expects 224×224 patches by default).
