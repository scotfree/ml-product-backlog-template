# Epic: Pipeline (Phone-to-Splat)

Move a phone video through five stages: frame extraction → SfM (camera poses + sparse point cloud) → Gaussian Splat training → format conversion → viewer/consumer. Interfaces between stages are all file formats — no live services.

Focus of this epic is orchestration: making the whole pipeline runnable end-to-end with stubs first, then swapping in real components. Because SfM and splat training are both slow (minutes to hours), the stub-first discipline matters *more* here than in a fast-inference project — you don't want to wait an hour for COLMAP just to discover your file-handling code has a bug.

## Cards in this epic

1. Design the pipeline interface
2. Build a stub pipeline end-to-end
3. Replace stubs with real components (incremental)
