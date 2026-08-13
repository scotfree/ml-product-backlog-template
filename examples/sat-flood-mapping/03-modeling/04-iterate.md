# Iterate — improve one thing per run

Change one variable at a time. Priority order for this project: (a) loss function tweaks (Dice vs. weighted CE vs. focal), (b) decoder architecture, (c) unfreezing the top layers of the backbone, (d) parameter-efficient fine-tuning (LoRA-style adaptations to the frozen backbone).

- **Upstream/downstream:** Model Analysis (Card 04-model-analysis/03) tells you what to try next. Deployment (Card 06-deployment/03) tells you whether the improvement earns its inference cost.
- **Definition of done:** `docs/experiments.md` with one line per run: what changed, IoU delta, notes. Best-so-far checkpoint promoted to `models/flood_best.ckpt`.
- **Demo:** Show the experiment log; call out the best change and one thing that didn't help.
- **Subtasks:**
  - Loss iterations: weighted CE with different weights, Dice, focal, combos.
  - Decoder: TerraTorch supports several (UperNet, FCN, others per the [survey](https://arxiv.org/abs/2412.02732)) — try 2–3.
  - Backbone unfreezing: unfreeze the last N transformer blocks; compare training cost vs. IoU gain.
  - **Stretch:** parameter-efficient methods — see [PEFT for Geospatial FMs](https://arxiv.org/abs/2504.17397) as a reference direction. Only if the team has bandwidth after the basics.
  - Stop when improvements plateau or the sprint ends.
