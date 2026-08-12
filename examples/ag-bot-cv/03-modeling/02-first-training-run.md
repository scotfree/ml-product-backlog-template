# End-to-end training run, even if bad

## Description

Fine-tune YOLO11n on LaboroTomato (fruit). Doesn't need to be good — needs a checkpoint we can hand to Model Analysis and to Deployment. Fruit is the easiest task; get the training-loop plumbing working here before pest or disease.

## Upstream / Downstream contract

- Model analysis (Card 04-model-analysis/02) consumes the checkpoint.
- Deployment (Card 06-deployment/01) consumes it to test the packaging path.

## Definition of Done

Checkpoint saved to `models/fruit_yolo11n_v0.pt`. `configs/fruit_yolo11n_v0.yaml` captures every hyperparameter. `scripts/train.py --config configs/fruit_yolo11n_v0.yaml` reproduces the run.

## Demo

Run inference on one LaboroTomato test image; show the predicted boxes.

## Subtasks

- Use Ultralytics' `model.train()` if AGPL is OK; otherwise adapt RF-DETR's fine-tune script.
- Config-driven, not hardcoded — every hyperparameter in the YAML.
- Version the checkpoint filename (`_v0`, `_v1`, ...) so we never overwrite.

## Estimate

~2 days.
