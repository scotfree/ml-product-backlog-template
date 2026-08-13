# Benchmark and document compute requirements

Measure runtime and memory for each pipeline stage on realistic hardware: a laptop CPU, a laptop GPU, a cloud GPU (Colab or RunPod). Publish a table so users can plan.

- **Upstream/downstream:** Documentation consumes the numbers directly. Product analysis has already validated correctness; this is about setting expectations for users.
- **Definition of done:** `docs/performance.md` with a table: (scene tier × hardware × stage) → (runtime, peak memory). Explicit recommendation: "For an easy-tier scene, expect X minutes on a laptop CPU; Y minutes on a mid-range GPU; Z minutes on Colab."
- **Demo:** Present the table; call out the surprising number (usually: how much slower CPU-only splat training is than GPU).
- **Subtasks:**
  - Pick 3 scenes representing the difficulty tiers.
  - Measure on each hardware target the team has access to.
  - Report includes what didn't work (some paths may OOM or crash — document those too).
  - Include a "when to use Colab" recommendation (usually: hard-tier scenes on a CPU-only laptop is not worth the wait).
