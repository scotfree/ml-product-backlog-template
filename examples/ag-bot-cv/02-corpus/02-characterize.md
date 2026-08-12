# Characterize the chosen dataset

For each chosen dataset, characterize class distribution, resolution range, and any known quirks. IP102 in particular has severe long-tail class imbalance that will bite pest-detection metrics later.

- **Upstream/downstream:** Modeling needs to know about imbalance (affects loss choice, augmentation). Model analysis needs to know about tail classes (per-class breakdown matters more than headline mAP).
- **Definition of done:** Notebook per dataset with class-count histogram, resolution stats, sample size, and 3–5 flagged issues. Committed to `notebooks/corpus/`.
- **Demo:** Show the IP102 class histogram (long tail is dramatic) and one surprise from the spot-check.
- **Subtasks:**
  - Class/label distribution per dataset.
  - Image resolution range and aspect ratios.
  - Spot-check ~50 raw examples from each with human eyes — look for mislabels, duplicates, watermarks.
  - Note: PlantVillage is uniformly clean lab shots; PlantDoc/FieldPlant are messy field shots. Flag this loudly for cross-eval planning.
