# Iterate — improve one thing per run

One change per run. Priority order: (a) fruit augmentation (cheap wins), (b) YOLO11n → YOLO11s on fruit (see if the bigger model earns its keep on Pi), (c) start on pest, (d) start on disease. Stop when improvements plateau or Sprint 3 ends.

- **Upstream/downstream:** Model analysis (03-error-analysis) informs what to try next. Deployment (03-benchmark) informs whether YOLO11s is even viable on Pi 3B CPU.
- **Definition of done:** `docs/experiments.md` with one line per run: what changed, mAP delta, notes. Best-so-far checkpoint per task promoted to `models/<task>_best.pt`.
- **Demo:** Show the experiment log; call out the best change and one thing that didn't help.
- **Subtasks:**
  - Fruit: baseline → add augmentation → try YOLO11s.
  - Pest: baseline (expect long-tail pain), then decide on mitigation for the tail (focal loss, class-balanced sampling — one per run).
  - Disease: baseline on PlantVillage first, then Sprint 5 cross-eval on PlantDoc/FieldPlant.
