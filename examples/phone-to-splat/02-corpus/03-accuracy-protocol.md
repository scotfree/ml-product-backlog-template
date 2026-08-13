# Define the accuracy protocol

This is the hard, interesting card. Given a reconstruction (a point cloud, mesh, or splat) and a ground-truth measurement (dimensions in mm), how do you compute an accuracy score? There's no textbook answer — the team has to design it.

- **Upstream/downstream:** Model Analysis (Card 04-model-analysis/03) implements this protocol into an evaluation script. Product Analysis (Card 05-product-analysis/01) reports numbers using it. Documentation (Card 07-documentation/02) captures the reasoning.
- **Definition of done:** `docs/accuracy-protocol.md` covering the four decisions below, with rationale for each choice. Implemented as `evaluate_reconstruction(reconstruction_path, ground_truth_path) -> AccuracyReport` in the code.
- **Demo:** Walk through one reconstruction being evaluated end-to-end; explain why each decision was made the way it was.
- **Subtasks:**
  - **Feature correspondence:** how do you identify "the cube's edge length" in a point cloud? Manual annotation of a few reference points? Automatic detection? RANSAC-fit primitives (planes, cylinders)?
  - **Scale handling:** given the scale ambiguity in monocular SfM, do you (a) require a known-size reference in every capture, (b) use a global scale-alignment step, or (c) report scale-invariant error only?
  - **Error representation:** absolute (mm) or relative (%)? Per-axis, per-edge, per-face, or aggregate? Mean, worst-case, or distribution?
  - **Pass criteria:** what number means "the reconstruction is trustworthy"? This depends on the intended use — a Rubik's cube reconstruction useful for AR overlay needs different accuracy than one useful for 3D printing a replica.

## Why this card matters

In ag-bot-cv, "correct" is defined by the dataset (labels are given). Here, students have to *design* the definition of correct. That's the higher-order engineering skill: understanding that accuracy metrics are not natural facts, they're choices with tradeoffs. A student who can articulate why they chose worst-case corner error over mean face-flatness deviation understands measurement in a way most graduates don't.
