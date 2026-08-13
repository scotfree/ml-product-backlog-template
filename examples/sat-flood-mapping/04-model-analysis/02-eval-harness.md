# Reproducible evaluation harness

`evaluate.py --model <path> --split test` produces the same numbers every time. Outputs a JSON report + Markdown summary. Runs on the locked test set (geographic holdouts from Corpus Card 03).

- **Upstream/downstream:** Everyone comparing models depends on this. Product Analysis extends it to realistic-input tests.
- **Definition of done:** Reproducible: same model + same command → identical numbers. Reports committed to `reports/<model_version>.md`.
- **Demo:** Run harness on the pre-fine-tuned baseline and on your latest run; show the comparison table.
- **Subtasks:**
  - Locked test set enforced via a hash whitelist.
  - Deterministic evaluation (seed everything; augmentation off).
  - JSON output for machine readability, Markdown for humans.
  - Include per-region rows in the output, not just aggregates.
  - Compare against the published Sen1Floods11 baseline numbers from the [Prithvi-EO-2.0 paper](https://arxiv.org/abs/2412.02732), §4.
