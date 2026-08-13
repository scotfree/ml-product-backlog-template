# Capture, measure, and share the corpus

Actually build the corpus. Each team member captures at least 3 scenes across the difficulty tiers, measures ground-truth dimensions (with a ruler, caliper, laser measure, or from a 3D-printed part's published STL), and uploads to shared storage with metadata.

- **Upstream/downstream:** Modeling and Model Analysis both depend on this being real, labeled data. Share the corpus across the whole team so any team member's reconstruction can be evaluated against any other's ground truth.
- **Definition of done:** ≥12 scenes uploaded to shared storage (Google Drive, S3, or repo LFS — team's choice). Each scene has: the video file, a metadata JSON (phone model, settings, capture date, room lighting, camera path description), and a ground-truth JSON (measured dimensions, tolerance, measurement method).
- **Demo:** Walk the team through 3 scenes at different difficulty tiers; show the metadata schema; show the ground-truth measurements.
- **Subtasks:**
  - Agree on a metadata schema and a ground-truth JSON schema (Card 03 will need this).
  - Each team member: capture ≥3 scenes.
  - Ground truth: dimensions in millimeters, with the measurement method and tolerance recorded. For 3D-printed parts, cite the source STL.
  - **Include a known-size reference in the frame.** Monocular SfM has scale ambiguity — without a reference, absolute measurements are impossible. A ruler or coin visible in the video solves this.
