# Epic: Model analysis (Phone-to-Splat)

"Is the reconstruction any good?" — with real ground truth, this is answerable in absolute terms (millimeters of error), not just "vibes." Three complementary lenses: SfM-level metrics (was the camera pose estimation any good?), splat-level metrics (does the rendered view match held-out real views?), and geometric accuracy (does the reconstruction match the ground truth?).

The third one — geometric accuracy — is the star of this project. It's what most 3D-reconstruction educational projects skip.

## Cards in this epic

1. Define metrics for each layer
2. Reproducible evaluation harness
3. Failure-mode analysis
