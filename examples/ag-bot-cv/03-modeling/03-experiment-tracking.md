# Add experiment tracking

Wire up W&B (free tier) for every training run. Config, metrics, sample predictions, and final checkpoint all logged. Team lead sets up a shared W&B project so all 4 students can see each other's runs.

- **Upstream/downstream:** Anyone else on the team running experiments needs to find and compare runs.
- **Definition of done:** All 4 students' training runs appear in the shared W&B project. Every run has config, train/val metrics per epoch, and a link back to the git commit.
- **Demo:** Show two runs side-by-side in W&B; explain the delta.
- **Subtasks:**
  - Shared W&B project set up; all students added.
  - `wandb.init()` and `wandb.log()` calls in `scripts/train.py`.
  - `wandb.config` populated from the training YAML automatically.
  - Log 5–10 sample predictions per epoch for visual sanity-check.
