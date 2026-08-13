# Define metrics for each layer

Three layers, three metric families:

- **SfM layer:** reprojection error (per-pixel, aggregate mean/median), number of images registered vs. total, sparse point cloud density.
- **Splat layer:** PSNR and SSIM on held-out views (train/val split of the input frames).
- **Geometric accuracy:** implements the accuracy protocol from Corpus card 03. Real numbers in millimeters vs. ground truth.

- **Upstream/downstream:** Modeling (03-modeling/03) uses these to decide what to iterate on. Product analysis inherits the geometric-accuracy metric as a system-level success criterion.
- **Definition of done:** `docs/metrics.md`: what metrics per layer, why, what thresholds count as pass/fail per difficulty tier from the corpus.
- **Demo:** Explain in one sentence why all three layers matter (each catches problems the others miss — good PSNR with bad geometry is possible, and vice versa).
- **Subtasks:**
  - SfM: define acceptable reprojection error (typically < 1 px median for well-captured scenes).
  - Splat: hold out ~10% of frames as validation views; report PSNR and SSIM.
  - Geometric: implement the accuracy protocol from Corpus 03. Establish tier-specific pass thresholds.
  - Sanity-check against a naive baseline: "reconstruction = mean point cloud from all input images" should score badly on all metrics.
