# Survey tools and pick defaults

Pick an SfM tool and a splat trainer. COLMAP is the standard SfM choice; several splat trainers exist with different licenses and features.

- **Upstream/downstream:** Pipeline (01-pipeline/03) consumes these choices when swapping stubs for real components. Deployment (06-deployment/01) inherits any packaging constraints.
- **Definition of done:** `docs/tools.md` with 2–3 SfM candidates and 2–3 splat trainer candidates, license and pros/cons for each, and the chosen defaults with justification.
- **Demo:** Explain the pick and the top runner-up in one minute each.
- **Subtasks:**
  - **SfM candidates:**
    - **COLMAP** (BSD-3-Clause) — the standard. Well-documented, robust, cited by almost every 3D-from-images paper. Default recommendation. Ref: Schönberger & Frahm, *Structure-from-Motion Revisited*, CVPR 2016.
    - **GLOMAP** (BSD-3-Clause) — newer global SfM from the same COLMAP team, often faster on large collections. Worth trying if COLMAP is slow.
    - **OpenMVG** (MPL2) — older alternative, less active development. Only if COLMAP won't install.
  - **Splat trainer candidates:**
    - **gsplat** (Apache 2.0) — clean, well-maintained library used by nerfstudio and many others. Default recommendation.
    - **nerfstudio** (Apache 2.0) — full framework, includes gsplat plus alternatives (NeRF, etc.) and a viewer. Slightly heavier; good if the team wants the extra tooling.
    - **Original 3DGS reference code** (Kerbl et al.) — **INRIA research license, non-commercial**. Do NOT use if there's any chance the deliverable is commercial. Cite the paper regardless of what code you use. Ref: Kerbl et al., SIGGRAPH 2023 ([arxiv](https://arxiv.org/abs/2308.04079)).
  - Confirm both defaults install and run a smoke test on the team's laptops before committing.
