# Build a stub pipeline end-to-end

Every stage returns a fake-but-valid output file: frame extractor returns 10 canned images, SfM stub returns a canned sparse reconstruction, splat trainer stub returns a tiny .ply with 100 hard-coded gaussians, converter produces a valid but ugly .glb. The whole pipeline runs in seconds.

- **Upstream/downstream:** No external teammates blocked. Real file-format contracts get validated end-to-end (viewer opens the output) before any slow real component is wired in.
- **Definition of done:** `python -m phone_to_splat run --video <path> --out <dir>` runs to completion in under 60 seconds. The output opens in the target viewer (however ugly).
- **Demo:** Run the pipeline live; open the output in the viewer; show that even the stub .glb loads.
- **Subtasks:**
  - Canned frame set in `tests/fixtures/frames/`.
  - Stub SfM: hardcoded camera poses + point cloud in COLMAP text format.
  - Stub splat: tiny hand-authored .ply with valid Gaussian attributes.
  - Real converter (splat → glb) — this is short and worth validating early.
