# Epic: Modeling (Phone-to-Splat)

**Note on scope:** in this domain, "the model" is your choice of reconstruction pipeline (SfM tool + splat trainer + hyperparameters). There's no training dataset, no checkpoint to fine-tune, no iteration loop like a classifier project. This epic is deliberately thinner than in ML-heavy projects — three short cards instead of four. The template flexes to accommodate that; not every epic gets equal weight in every domain.

The real engineering weight in this project lives in Corpus (student-built ground truth) and Model Analysis (measurement against that ground truth). Modeling is mostly "pick tools, run them, tune per-scene."

## Cards in this epic

1. Survey tools and pick defaults
2. Run reconstruction end-to-end on one scene
3. Iterate per-scene hyperparameters
