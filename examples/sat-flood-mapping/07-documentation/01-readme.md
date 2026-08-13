# README that lets someone reproduce a run

A newcomer clones the repo, installs the tooling, downloads Sen1Floods11, and reproduces a fine-tuning run — all within an hour of readable instructions.

- **Upstream/downstream:** Future contributors, portfolio reviewers, and the hand-off test all consume this.
- **Definition of done:** Someone outside the team follows the README on a clean machine and reproduces a training run + inference on a test chip, without asking questions.
- **Demo:** Have that person show what they did.
- **Subtasks:**
  - Setup: Python version, GPU requirements, geospatial dependencies.
  - Data prep: download Sen1Floods11.
  - Train: one command via TerraTorch.
  - Evaluate: one command that produces a report.
  - Inference on a new tile: one command that produces a GeoTIFF + GeoJSON.
  - Common errors and fixes.
