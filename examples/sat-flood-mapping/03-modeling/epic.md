# Epic: Modeling (Sat-Flood-Mapping)

Fine-tune Prithvi-EO-2.0 for flood segmentation. Different from ag-bot-cv's YOLO fine-tuning in two ways:

1. **The pretrained model is huge** (300M–600M params) and domain-specific (pretrained on 4.2M global HLS samples via MAE — see [Roy et al., 2024](https://arxiv.org/abs/2412.02732)). Full fine-tuning is expensive; parameter-efficient methods (freezing the backbone, LoRA-style adaptations) are relevant.
2. **A pre-fine-tuned baseline already exists** ([Prithvi-EO-2.0-300M-TL-Sen1Floods11 on HuggingFace](https://huggingface.co/ibm-nasa-geospatial/Prithvi-EO-2.0-300M-TL-Sen1Floods11)). The team's job isn't necessarily to beat it — it's to reproduce it, understand what makes it work, and try to improve it in a specific direction (e.g., generalization to unseen regions).

## Cards in this epic

1. Survey candidates and pick a baseline
2. First fine-tuning run end-to-end
3. Add experiment tracking
4. Iterate — improve one thing per run
