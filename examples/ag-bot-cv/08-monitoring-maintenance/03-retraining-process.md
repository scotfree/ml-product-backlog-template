# Retraining and update process

When do we retrain? On what data? How do we know the new model is better before shipping? Doc the process even though we won't execute it during the program — it's a hire-relevant artifact for the writeup and it forces students to think past ship day.

- **Upstream/downstream:** Whoever owns the model long-term (post-program). Documentation (Card 07-documentation/02) captures the reasoning.
- **Definition of done:** `docs/retraining.md`: triggers (what would prompt retraining), data sources (where new labeled data comes from), validation (how we compare v_new vs. v_current before rollout), rollback plan.
- **Demo:** Walk through the process; explain the hardest decision (usually: "when is per-class F1 drop significant vs. noise?").
- **Subtasks:**
  - Triggers: per-class F1 drops by X on validation of freshly-collected data; new pest species reported; quarterly refresh.
  - Data: image archive in AgCloud MinIO (from `mc mirror` sync) with retroactive labeling process.
  - Validation: A/B on a held-out real-conditions set; ship only if new model wins on ≥2 of 3 tasks.
  - Rollback: `pip install robogreeno-detection==<prev>` on Pi; supervised by Embedded.
