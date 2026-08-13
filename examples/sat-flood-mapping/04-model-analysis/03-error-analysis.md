# Error analysis

For the best model, pull the worst-predicted chips and look at them. Group by root cause. Common causes in flood mapping include: cloud contamination, permanent water misclassified as flood, sediment/muddy water confused with land, salt flats, snow, urban water features.

- **Upstream/downstream:** Modeling (Card 03-modeling/04) consumes this to decide what to iterate. Product Analysis (Card 05-product-analysis/02) inherits the failure taxonomy as edge-case tests. Documentation captures lessons.
- **Definition of done:** `notebooks/error-analysis.ipynb` with 3–5 identified failure classes, each with example chips and hypotheses.
- **Demo:** Walk through 3 chips the model gets wrong; explain the diagnosis.
- **Subtasks:**
  - Pull worst-scoring chips (by flood-class IoU) from the test set.
  - Group by geography (do failures cluster in one region?), by biome (does the model struggle in specific ecosystems?), by cloud fraction, by flood extent size.
  - Common failure modes to look for:
    - **Cloud confusion:** partial clouds mislabeled as flood or missing flood.
    - **Permanent water confusion:** rivers/lakes classified as flood.
    - **Sediment-heavy water:** turbid floodwater looks spectrally like land.
    - **Salt flats and dry lake beds:** high SWIR reflectance can look water-like.
    - **Urban water:** street-level flooding is small, hard to detect at 10m resolution.
  - Distinguish data problems (label noise) from model problems (fundamental limits) from tunable-with-more-data problems.
