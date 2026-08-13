# First fine-tuning run end-to-end

Get one fine-tuning run to complete, however bad the result. Uses TerraTorch config-driven training on Sen1Floods11's official event-based split.

- **Upstream/downstream:** Model Analysis (Card 04-model-analysis/02) consumes the resulting checkpoint. Deployment (Card 06-deployment/01) consumes it to test the packaging path.
- **Definition of done:** Checkpoint saved to `models/flood_prithvi_v0.ckpt`. `configs/flood_prithvi_v0.yaml` captures the full training config. `terratorch fit -c configs/flood_prithvi_v0.yaml` reproduces the run.
- **Demo:** Run inference on a held-out flood chip using the trained model; show the predicted flood mask alongside the ground truth.
- **Subtasks:**
  - Use TerraTorch's config-driven interface — no hardcoded hyperparameters.
  - Freeze the Prithvi backbone; only train the decoder/head. (Full backbone fine-tuning is a Card 04 iteration.)
  - Loss: weighted cross-entropy or Dice loss — class imbalance is severe. Start with the loss the [Prithvi-EO-2.0 paper](https://arxiv.org/abs/2412.02732) reports for Sen1Floods11.
  - Version the checkpoint filename (`_v0`, `_v1`) — never overwrite.
  - Log wall-clock time; foundation-model fine-tuning is not fast.
