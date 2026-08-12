# Reproducible evaluation harness

`scripts/evaluate.py --model <path> --task <fruit|pest|disease>` produces the same numbers every time on the locked test set. Outputs a JSON report + a Markdown summary. Runs both locally on the training machine and on the Pi (for deployment-time verification).

- **Upstream/downstream:** Everyone comparing models depends on this. Product analysis (Card 01-realistic-input-tests) may extend it with realistic-input evaluation.
- **Definition of done:** `evaluate.py` runs deterministically (seeded). Same model + same command → identical numbers. Reports committed to `reports/` per model version.
- **Demo:** Run harness on `fruit_yolo11n_v0` and `fruit_yolo11n_v3` side-by-side; show the comparison.
- **Subtasks:**
  - Locked test set enforced via a whitelist check on file hashes.
  - Seeded randomness where relevant (augmentation off at eval time).
  - JSON output for machine-readability; Markdown for humans.
  - Runs on Pi too — same numbers, different latency.
