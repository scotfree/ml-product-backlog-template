# README that lets someone reproduce a reconstruction

A newcomer clones the repo, installs the CLI, captures a video following our documented protocol, runs the pipeline, and gets a viewable 3D file with accuracy report — all within an hour.

- **Upstream/downstream:** External contributors, portfolio reviewers, and the hand-off test (Card 05-product-analysis/03) all consume this as source of truth.
- **Definition of done:** Someone outside the team follows the README on a clean machine and reproduces a reconstruction from a corpus scene without asking questions.
- **Demo:** Have that outside person show what they did in 3 minutes.
- **Subtasks:**
  - Install section (pip + Docker paths).
  - Capture protocol summary (link to the full `docs/capture-protocol.md`).
  - One command each: run reconstruction, view result, run accuracy evaluation.
  - Expected outputs at each step so users can tell they're on track.
  - Common errors + fixes.
