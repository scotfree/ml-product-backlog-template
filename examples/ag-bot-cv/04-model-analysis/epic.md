# Epic: Model analysis (Ag-Bot-CV)

## What this epic covers

Whether each detector actually learned. mAP@0.5 and mAP@0.5:0.95 as headline metrics, but per-class breakdown matters more than headline for pest (long-tail). Sprint 5 lab-to-field cross-eval on disease is the big analysis milestone.

## Cards in this epic

1. Define evaluation metrics
2. Reproducible evaluation harness
3. Error analysis

## Success criteria

Anyone on the team can run `scripts/evaluate.py` and get identical, comparable numbers for any checkpoint, on laptop or Pi. Each task has named failure modes with example images. Demoable as two model versions compared live, plus three pest errors explained.
