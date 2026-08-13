# Package as a CLI

Build `phone-to-splat` as a Python wheel with a CLI entry point (`phone-to-splat run --video X --out Y`). Since COLMAP and gsplat are non-trivial dependencies, ship a `docker` image *alongside* the wheel for users who don't want to fight system dependencies.

- **Upstream/downstream:** External users are the consumers. Compute-heavy backend (Colab/GPU cloud) is a separate concern (Card 03).
- **Definition of done:** `pip install phone-to-splat` installs the CLI. `phone-to-splat --help` shows subcommands. Docker image `phone-to-splat:latest` is buildable from the repo and runs the same CLI. Both work on Linux and macOS (Windows is best-effort).
- **Demo:** Install in a fresh venv; run on a canned tiny video; show the .glb output.
- **Subtasks:**
  - `pyproject.toml` with the CLI entry point.
  - Handle the COLMAP dependency — either bundle a wheel with pycolmap (nice) or document `apt install colmap` prerequisite (simpler).
  - Handle the GPU dependency — CPU-only splat training is slow but works; document GPU requirement clearly with realistic runtime estimates.
  - Docker image: bake all dependencies including COLMAP and a CUDA runtime.
