# Replace stubs with real components (incremental)

Swap one stub at a time. Order: (1) real frame extractor (easy, fast), (2) real converter (short, mostly done in the stub phase), (3) real COLMAP (slow but well-documented), (4) real splat trainer (slowest, most memory-hungry).

- **Upstream/downstream:** Each swap has its own risk. COLMAP failures typically mean the input video didn't have enough overlap (this is a Corpus-epic concern). Splat training failures typically mean SfM output was bad (upstream problem).
- **Definition of done:** Real component passes the same interface tests as the stub it replaced. `pytest tests/` still green after each swap. A single "known-good" test scene runs end-to-end in real time.
- **Demo:** For each swap, show pipeline running with the new real stage. For SfM, show the actual camera pose overlay. For splat, show a rendered frame.
- **Subtasks:**
  - One card per stub-to-real swap.
  - Frame extractor: `ffmpeg` wrapper with target frame count and dedup logic.
  - COLMAP: use `pycolmap` bindings or subprocess `colmap` CLI (both fine).
  - Splat: use `gsplat` (Apache) or `nerfstudio` (Apache) — see Modeling epic for the tool selection.
