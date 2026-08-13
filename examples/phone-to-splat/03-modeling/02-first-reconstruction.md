# Run reconstruction end-to-end on one scene

Pick one scene from the corpus (an easy-tier one — 3D-printed cube or textured mug). Run COLMAP → splat training → convert → view. Doesn't need to be a great reconstruction; needs to exist and open in the viewer.

- **Upstream/downstream:** Model Analysis (04-model-analysis/02) consumes the output as a first input to the evaluation harness. Pipeline (01-pipeline/03) has this as its real-component target.
- **Definition of done:** For one scene, a saved reconstruction (splat .ply + converted .glb), plus the exact commands that produced it, checked into `runs/<scene_id>/README.md`.
- **Demo:** Load the reconstruction in the viewer; rotate it; show it looks recognizably like the reference object.
- **Subtasks:**
  - Config file capturing: COLMAP feature-extractor settings, splat trainer iteration count, densification thresholds, learning rates.
  - Version the run directory (`runs/rubiks_v0/`, `runs/rubiks_v1/`) — never overwrite.
  - Record timing at each stage (SfM took X min, splat training took Y min) — students underestimate this without data.
