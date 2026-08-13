# Characterize the corpus

Class imbalance, cloud fraction, geographic distribution, band statistics. Foundation-model fine-tuning needs to know what the data actually looks like — surprises here become bugs later.

- **Upstream/downstream:** Modeling needs to know class imbalance (drives loss choice). Model Analysis needs to know geographic distribution (drives the per-region breakdown).
- **Definition of done:** Notebook in `notebooks/corpus/` with class distribution, cloud fraction distribution, per-biome / per-continent chip counts, per-band mean/std (needed for normalization matching Prithvi's pretraining).
- **Demo:** Show the class imbalance chart (flood pixels are ~5% of total — this matters). Show the geographic distribution map (11 events, 6 continents — but heavily concentrated in a few regions).
- **Subtasks:**
  - Pixel-level class distribution: expect severe imbalance (mostly no-water, small flood fraction).
  - Cloud fraction: some chips are almost entirely cloud — decide handling.
  - Geographic distribution: map the 11 events across the 6 continents. Note which biomes are over- and under-represented.
  - Per-band statistics: compute mean/std across the corpus for normalization (Prithvi has published its pretraining stats — you can either match those or recompute; document the choice).
  - Spot-check: look at ~20 chips with your own eyes. Note anything odd (mislabeled edges, sensor artifacts, permanent water misclassified as flood).
