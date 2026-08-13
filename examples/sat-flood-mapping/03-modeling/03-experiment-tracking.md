# Add experiment tracking

Wire up W&B (free tier) or MLflow for every run. Foundation-model fine-tuning is expensive enough that you *cannot* afford to forget what settings you used last time.

- **Upstream/downstream:** Everyone comparing runs depends on this. Modeling Card 04 (iterate) is essentially unusable without it.
- **Definition of done:** All students' runs appear in a shared tracking project. Every run logs: config, per-epoch metrics (IoU, F1, loss), sample predictions on a held-out chip, checkpoint reference, git commit hash.
- **Demo:** Show two runs side-by-side in the tracking UI; explain what changed.
- **Subtasks:**
  - Shared tracking project; all students added.
  - TerraTorch has W&B logging built-in — enable it in the config.
  - Log sample predictions as images so you can eyeball what's happening without downloading checkpoints.
  - Track GPU-hours per run (this becomes a real budget metric).
