# Example: Phone-to-Splat (video → 3D file pipeline)

A filled-in instantiation of the template, adapted for a **non-ML** pipeline: phone video in → Structure-from-Motion → Gaussian Splat training → standard 3D file (glb/mesh) out.

This example demonstrates two things the ag-bot-cv example doesn't:

1. **The template works even when "modeling" is barely modeling.** Here the "model" is a choice of reconstruction tools + per-scene hyperparameters. There's no dataset to fine-tune on and no checkpoint to iterate. The modeling epic is thin — that's honest, and the template flexes to accommodate it.
2. **The corpus can be a real engineering deliverable.** Students design a capture protocol, build a corpus of reference objects with **measured ground-truth dimensions**, and then invent an accuracy protocol to compare reconstructions against those measurements. That third step is unusually rich pedagogy: students learn that "accuracy" is defined, not looked up.

## Differences from ag-bot-cv

- **No Monitoring & Maintenance epic.** This is a batch pipeline (upload video → get 3D file), not a running service. Nothing to monitor at runtime. Reliability-flavored concerns migrate into Product Analysis (edge cases: short videos, texture-poor scenes, motion blur). If your team has good reason to add Monitoring back, use the template's 8th epic as a starting point.
- **Modeling is lightweight.** Three cards instead of four, and they're shorter.
- **Corpus and Model Analysis are the meaty epics.** This is where the real engineering happens.
- **Deployment is CLI + viewer, not edge device.** No packaging for constrained hardware.

## Project context (abridged)

- **Team:** 4-person bootcamp team + team lead.
- **Compute:** Student laptops. A GPU laptop or Colab is helpful for Gaussian Splat training but not strictly required (small scenes work CPU-only, slowly).
- **Tools (default recommendations):** COLMAP for SfM, `gsplat` (or `nerfstudio`) for splat training, SuperSplat or standard glTF viewers for consumption. Alternatives discussed per epic.
- **Corpus:** Student-generated. Reference objects with known dimensions. Includes 3D-printed parts, everyday measurable objects, and room-scale scenes.
- **Deliverable:** A CLI tool that takes a phone video and produces (a) a .glb (or splat) file, (b) an accuracy report against the object's ground-truth measurements.

## Key references

Cited throughout the epics where relevant.

- **COLMAP / SfM:** Schönberger, J. L., & Frahm, J.-M. (2016). *Structure-from-Motion Revisited.* CVPR. [Paper](https://openaccess.thecvf.com/content_cvpr_2016/html/Schonberger_Structure-From-Motion_Revisited_CVPR_2016_paper.html) · [Code](https://github.com/colmap/colmap)
- **COLMAP MVS:** Schönberger, J. L., Zheng, E., Pollefeys, M., & Frahm, J.-M. (2016). *Pixelwise View Selection for Unstructured Multi-View Stereo.* ECCV.
- **3D Gaussian Splatting:** Kerbl, B., Kopanas, G., Leimkühler, T., & Drettakis, G. (2023). *3D Gaussian Splatting for Real-Time Radiance Field Rendering.* SIGGRAPH. [Paper](https://arxiv.org/abs/2308.04079) · [Project page](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/)
- **Survey (helpful overview of the whole 3D-from-images landscape):** Dalal, A., Hagen, D., Robbersmyr, K. G., & Knausgård, K. M. (2024). *Gaussian Splatting: 3D Reconstruction and Novel View Synthesis, a Review.* IEEE Access. [Paper](https://arxiv.org/abs/2405.03417)
- **Splat → mesh (for downstream use):** Guédon, A., & Lepetit, V. (2024). *SuGaR: Surface-Aligned Gaussian Splatting for Efficient 3D Mesh Reconstruction and High-Quality Mesh Rendering.* CVPR.
