# Epic: Modeling (Ag-Bot-CV)

## What this epic covers

YOLO11n as baseline, with RF-DETR (Apache) as the fallback if the AGPL question comes back "not acceptable". Fine-tuning only — no from-scratch. Fruit model first (easiest), then pest, then disease across the sprints.

## Cards in this epic

1. Survey candidates and pick a baseline
2. End-to-end training run, even if bad
3. Add experiment tracking
4. Iterate — improve one thing per run

## Success criteria

A `models/<task>_best.pt` for fruit, pest, and disease, each beating its baseline and each traceable to a W&B run and a config in git. The license question is settled and recorded. Demoable as two runs side-by-side in W&B with the delta explained.
