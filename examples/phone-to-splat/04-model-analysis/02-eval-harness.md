# Reproducible evaluation harness

`evaluate.py --run <run_dir> --scene <scene_id>` produces the same numbers every time. Reads the reconstruction, the ground truth for that scene, and outputs a JSON report + Markdown summary covering all three metric layers.

- **Upstream/downstream:** Everyone comparing runs depends on this. Product analysis extends it with realistic-input evaluation.
- **Definition of done:** Reproducible: same run + same command → identical numbers. Reports committed to `reports/<scene_id>/<run_id>.md` per (scene, run) pair.
- **Demo:** Run harness on two configs of the same scene; show the comparison table.
- **Subtasks:**
  - Locked held-out validation frames per scene (documented, hashed).
  - Deterministic evaluation (seed everything; disable any random sampling in metrics).
  - JSON for machine readability, Markdown for humans.
  - Handle the "reconstruction failed entirely" case gracefully — reports a fail row, doesn't crash.
