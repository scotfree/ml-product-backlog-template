# Retraining and update process

When do we retrain? On what data? How do we validate a new model is better before rollout? Document the process even if you don't execute it during the program — it's interview-visible and forces thinking past ship day.

- **Upstream/downstream:** Whoever owns the model post-program. Documentation captures the reasoning.
- **Definition of done:** `docs/retraining.md`: triggers, data sources, validation, rollout, rollback.
- **Demo:** Walk through the process; explain the hardest decision.
- **Subtasks:**
  - **Triggers:** per-region IoU drops on fresh labeled data; sensor drift detected (Card 02); annual refresh; new flood event with expert labels available.
  - **Data sources:** post-hoc humanitarian labels (e.g., HOT OSM Team maps flooded areas after events — can become training labels); new expert-labeled events (Sen1Floods11 was 11 events; more exist now).
  - **Validation:** hold out most-recent events; require new model to beat current model on those before rollout.
  - **Rollout:** A/B on a subset of tiles first (route 10% of production traffic to the new model, compare distributions).
  - **Rollback:** version model weights; keep last-known-good deployable in one command.
