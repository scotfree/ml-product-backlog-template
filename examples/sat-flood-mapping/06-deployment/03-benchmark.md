# Benchmark on realistic hardware

Measure per-tile latency and memory: CPU laptop, laptop GPU, cloud GPU (T4/A10), CPU-only server. Include cold-start latency (loading the ~1.2 GB model into memory) — for batch systems that spin up on demand, cold-start is often the dominant cost.

- **Upstream/downstream:** Documentation consumes the numbers. Ops consumer plans capacity from them.
- **Definition of done:** `docs/performance.md`: table of (hardware × warm/cold) → (latency, memory) for a standard 512×512 tile. Recommendation for target deployment sizing.
- **Demo:** Present the table; call out the surprising number (typically: cold start is 5–10x the per-tile inference cost).
- **Subtasks:**
  - Standard test tile (a fixed one from Sen1Floods11 test set).
  - Warm-up runs first, then N=20 measured runs on each hardware target.
  - Include cold-start numbers separately.
  - Report per-tile RAM peak and per-tile GPU memory peak.
  - Compare 300M vs 600M if both are viable options.
