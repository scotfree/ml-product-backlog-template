# Package as a CLI + container

Build `flood-mapping` as a pip-installable CLI: `flood-mapping predict --input <tif> --out <dir>`. Also produce a Docker image that bundles the model weights (or downloads them at first run — model weights are ~1.2 GB, worth being deliberate).

- **Upstream/downstream:** Ops consumer runs the CLI or the container. Documentation captures usage.
- **Definition of done:** `pip install flood-mapping` installs the CLI. `flood-mapping --help` shows subcommands. `docker pull <registry>/flood-mapping:<tag>` and `docker run` both work.
- **Demo:** Fresh venv install, then run on a sample tile; show the .tif and .geojson outputs.
- **Subtasks:**
  - `pyproject.toml` with the CLI entry point.
  - Decide on model weight handling: bundle in the wheel (large but simple), download at first run (smaller wheel, needs network), or expect the user to supply (most flexible, most friction).
  - Handle geospatial dependencies (`rasterio`, `geopandas`, `pyproj`) — these are notoriously finicky. Docker is often the cleanest answer for external users.
  - Confirm the wheel/container runs on Linux CPU-only (slower but should work for inference on small tiles).
