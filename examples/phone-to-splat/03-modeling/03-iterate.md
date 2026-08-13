# Iterate per-scene hyperparameters

Unlike a classifier project, you don't iterate on a single model — you iterate on *per-scene* hyperparameters because different scenes need different treatment. A texture-poor object may need more input frames; a large scene may need lower densification thresholds; a shiny object may need masking of specular regions.

- **Upstream/downstream:** Model Analysis feeds back which scenes are failing and how. Corpus card 03 (accuracy protocol) tells you if a change actually helped or just looked prettier.
- **Definition of done:** `docs/experiments.md` with one line per (scene × config) run: what changed, what happened to accuracy score, notes.
- **Demo:** Show two runs of the same scene with different settings; contrast visually and by accuracy score.
- **Subtasks:**
  - Common levers: frame extraction rate, SfM feature type (SIFT vs. others), splat training iterations, densification interval, learning rate schedule.
  - **One change per run.** Multiple simultaneous changes make it impossible to attribute improvements.
  - Stop when: accuracy meets the pass criteria for the scene tier, OR further iteration isn't earning its runtime cost.
