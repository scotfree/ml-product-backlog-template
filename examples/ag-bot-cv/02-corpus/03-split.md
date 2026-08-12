# Split train / validation / test with a rationale

## Description

Deterministic seeded splits per dataset. For disease specifically, we need a split that supports Sprint 5's lab-to-field cross-eval: train on PlantVillage, test on PlantDoc/FieldPlant.

## Upstream / Downstream contract

- Model analysis (Card 04-model-analysis/02-eval-harness) depends on a locked test set.
- Modeling (Card 03-modeling/02) will fast-loop on a subsample.

## Definition of Done

Split logic in `robogreeno_detection/data/splits.py`, seeded. Test-set access gated behind a "reveal" flag in the eval harness. Documented in `docs/datasets.md`.

## Demo

Show the split code and the assertion in training code that raises if test data leaks in.

## Subtasks

- Fruit/pest: standard 70/15/15 stratified by class.
- Disease: two parallel splits — (a) standard within-dataset, (b) cross-dataset (train on PlantVillage, val within PlantVillage, test on PlantDoc + FieldPlant).
- Fast-loop sub-sample: 200 images per task for smoke-test iteration.

## Estimate

~1 day.
