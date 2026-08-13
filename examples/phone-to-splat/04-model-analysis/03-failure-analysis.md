# Failure-mode analysis

For each hard-tier scene that failed or scored poorly, look at what happened. Was it an SfM failure (too few images registered)? A splat failure (rendered views look wrong)? A geometry failure (rendered views look fine but measurements are off)? Group by root cause.

- **Upstream/downstream:** Modeling (03-modeling/03) uses this to decide what per-scene hyperparameter changes to try. Product analysis inherits the failure taxonomy as edge-case tests. Documentation captures lessons.
- **Definition of done:** `notebooks/failure-analysis.ipynb` with 3–5 identified failure classes, each with example scenes, symptoms, and hypotheses.
- **Demo:** Walk through 3 failed reconstructions; explain the diagnosis.
- **Subtasks:**
  - Common failure classes to look for:
    - **Insufficient overlap:** SfM registers few images; sparse cloud is thin. Fix: recapture with slower orbit.
    - **Texture-poor surfaces:** SIFT finds nothing; SfM fails or produces holes. Fix: masking, alternative features, or acknowledge as out-of-scope.
    - **Motion blur:** frames are individually low-quality; feature matching struggles. Fix: capture protocol adjustment.
    - **Reflective/transparent surfaces:** splat rendering may look OK but geometry is wrong. Fix: exclude reflective regions or document as a known limitation.
    - **Scale drift over long orbits:** camera trajectory closes imperfectly; global geometry warps. Fix: shorter loops or explicit loop closure.
  - Distinguish data problems (capture) from tool problems (SfM/splat settings) from fundamental limits (monocular reconstruction of glass).
