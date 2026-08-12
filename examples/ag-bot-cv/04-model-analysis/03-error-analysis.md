# Error analysis

For each task's best model, pull the worst 20 predictions and look at them. Group by failure mode. Feed conclusions back into Modeling (which augmentation? which dataset addition?) and Documentation (decisions log).

- **Upstream/downstream:** Modeling (04-iterate) consumes conclusions as input for the next iteration. Documentation (02-decisions-log) captures why choices were made.
- **Definition of done:** `notebooks/error-analysis/<task>.ipynb` with 3–5 identified failure modes per task, each with example images and a hypothesis.
- **Demo:** Walk through 3 pest misclassifications; explain what's happening (usually: rare class, occlusion, or lab-vs-field domain shift).
- **Subtasks:**
  - Pull worst-scoring examples per task.
  - Group by patterns (class, size, lighting, background).
  - Distinguish "data problem" (mislabels, class imbalance) from "modeling problem" (needs bigger model, better augmentation).
  - Cross-reference with dataset spot-check notes from Card 02-corpus/02.
