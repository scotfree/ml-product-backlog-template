# Define evaluation metrics

Headline: mAP@0.5 and mAP@0.5:0.95 (COCO-style). But per-class F1 matters more for pest (long-tail IP102 classes). For ripeness (fruit), a confusion matrix across ripeness stages is what a greenhouse operator actually cares about.

- **Upstream/downstream:** Modeling (Card 04-iterate) uses these to decide what to try next. Product analysis inherits these as one input among several.
- **Definition of done:** `docs/metrics.md`: what metrics per task, why them, what values would count as success/failure. Per-task thresholds recorded (e.g., "pest is useful if per-class F1 > 0.4 on top 10 classes").
- **Demo:** Explain in one sentence why per-class F1 beats headline mAP for pest.
- **Subtasks:**
  - Fruit: mAP + ripeness confusion matrix.
  - Pest: mAP overall + per-class F1 on top-K most-common classes + coverage on tail.
  - Disease: mAP + per-condition F1 + cross-domain gap metric (Sprint 5).
  - Sanity-check each against a naive baseline (e.g., "predict most-common class only").
