# Define evaluation metrics

Headline: IoU and F1 for the flood class (class 0 is dominant — mean-IoU is misleading here). Also report false-positive rate and false-negative rate separately — they have different real-world costs. Break down by held-out region/event to show geographic generalization honestly.

- **Upstream/downstream:** Modeling uses these to decide what to iterate. Product Analysis inherits them as system-level success criteria.
- **Definition of done:** `docs/metrics.md`: metrics, why them, thresholds for "good enough". Include per-region breakdown template.
- **Demo:** Explain in one sentence why per-class IoU beats mean-IoU here (mean-IoU is dominated by the "no water" class; a model predicting "no water" everywhere would score ~95%).
- **Subtasks:**
  - **Flood-class IoU** (per-pixel intersection over union for class 1).
  - **Flood-class F1** (harmonic mean of precision and recall on flood pixels).
  - **False-negative rate** — missed flood pixels. **Highest-cost error for disaster response.** Emphasize.
  - **False-positive rate** — spurious flood predictions. Real cost: response resources wasted, credibility damaged.
  - **Per-region breakdown** — one row per held-out event/region. Reveals whether the model generalizes or just memorizes.
  - **Comparison to pre-fine-tuned baseline** — Prithvi-EO-2.0-300M-TL-Sen1Floods11 numbers are published; you should meet or beat them.
  - Sanity-check: "predict no-water everywhere" should score close-to-zero on flood F1 despite high overall accuracy.
