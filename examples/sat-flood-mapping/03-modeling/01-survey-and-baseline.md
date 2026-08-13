# Survey candidates and pick a baseline

Choose which Prithvi variant to use and which fine-tuning framework. Also decide whether to compete with or start from the pre-fine-tuned Sen1Floods11 checkpoint.

- **Upstream/downstream:** Deployment (Card 06-deployment/01) needs to know the model size (300M vs. 600M — meaningful memory/latency difference at inference). Analysis (Model Analysis Card 01) needs to know what baseline you're comparing against.
- **Definition of done:** `docs/model-survey.md` with 2–3 candidates, sizes, licenses, and a paragraph justifying the pick.
- **Demo:** Explain the choice; specifically say whether you're starting from the pre-fine-tuned Sen1Floods11 checkpoint (faster iteration, harder to improve) or from the raw Prithvi-EO-2.0-300M-TL (harder start, more room to explore).
- **Subtasks:**
  - **Model candidates:**
    - **Prithvi-EO-2.0-300M-TL** (Apache 2.0) — the default. TL = "temporal + location" variant, best for downstream fine-tuning per the paper.
    - **Prithvi-EO-2.0-600M-TL** (Apache 2.0) — 2× the params, marginally better, 2× the memory/compute. Only if you have the GPU budget.
    - **Prithvi-EO-2.0-300M-TL-Sen1Floods11** (Apache 2.0) — the pre-fine-tuned checkpoint. Use as: (a) baseline to reproduce, (b) starting point for further tuning, or (c) benchmark to beat.
  - **Fine-tuning framework:**
    - **[TerraTorch](https://github.com/IBM/terratorch)** (Apache 2.0) — IBM's newer framework, well-integrated with Prithvi. Default recommendation.
    - **[hls-foundation-os](https://github.com/NASA-IMPACT/hls-foundation-os)** (Apache 2.0) — the older reference, uses MMSegmentation. Fallback if TerraTorch has friction on your setup.
  - Confirm the choice runs a smoke test on the team's GPU before committing.
