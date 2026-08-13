# Design the pipeline interface

Sketch the five stages and the file each hands to the next: video file → extracted frame directory → COLMAP database + sparse reconstruction → trained splat (.ply) → converted 3D file (.glb or mesh .obj) → viewer.

- **Upstream/downstream:** The consumer is a viewer (Blender, SuperSplat, or a web viewer) that reads the final .glb / .splat. Confirm the target viewer's format expectations before locking the pipeline output.
- **Definition of done:** `docs/pipeline.md` with a diagram, file format at each boundary, and a note on which stages are slow (so students plan around them).
- **Demo:** Walk the team through the diagram in 2 minutes; point out which boundaries are file-based (all of them) and where each stage will store intermediate outputs.
- **Subtasks:**
  - Decide directory layout: `runs/<scene_id>/frames/`, `runs/<scene_id>/sparse/`, `runs/<scene_id>/splat/`, `runs/<scene_id>/output/`.
  - Decide intermediate file formats (COLMAP text format vs. binary; splat .ply vs. custom).
  - Decide final output format(s) based on the viewer(s) you're targeting.
  - Flag which stages are cacheable — SfM is slow but deterministic, so re-running only if inputs change.
