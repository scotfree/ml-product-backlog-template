# Identify candidate datasets

For each of fruit, pest, and disease, find 2–3 candidate public datasets. Check license against AgCloud's deployment posture (assume permissive-only until told otherwise). Rank by fit and license.

- **Upstream/downstream:** Modeling needs to know what data is available before choosing an architecture. Cloud (Kayvan) needs to know about any license constraints that propagate to AgCloud.
- **Definition of done:** `docs/datasets.md` listing candidates per task with license, size, source URL, and one-line "why this / why not". Winner marked per task.
- **Demo:** Present the shortlist per task; call out any license landmines.
- **Subtasks:**
  - Fruit: LaboroTomato, MinneApple, others. Check whether ripeness labels exist.
  - Pest: IP102 (detection subset), AgriPest, others. Check class balance.
  - Disease: PlantVillage (lab), PlantDoc (field), FieldPlant (field). Note the lab-vs-field distinction — Sprint 5 lab-to-field cross-eval depends on it.
  - Confirm no CC BY-NC or similar that would block AgCloud commercial deployment.
