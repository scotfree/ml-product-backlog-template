# Example: Sat-Flood-Mapping (Prithvi + Sen1Floods11)

A filled-in instantiation of the template, adapted for **satellite-based flood mapping** using a pretrained geospatial foundation model. This example demonstrates:

- **Foundation-model fine-tuning workflow** — different from ag-bot-cv's YOLO fine-tuning in that the pretrained model is much larger (300M–600M params) and includes domain-specific pretraining (masked autoencoder on multi-spectral time-series satellite imagery).
- **Multi-spectral data handling** — satellite imagery isn't RGB. Prithvi consumes 6 bands (Blue, Green, Red, Narrow NIR, SWIR1, SWIR2) from Sentinel-2. Students learn that "image" doesn't always mean 3 channels.
- **Geospatial-specific concerns** — coordinate reference systems (CRS), tiling and reprojection, geographic vs. random splits, real-world consequences of prediction errors.
- **Real production monitoring** — flood mapping systems run continuously and are monitored in production, so the Monitoring & Maintenance epic is fully populated (unlike phone-to-splat).

## Differences from the other examples

| | ag-bot-cv | phone-to-splat | sat-flood-mapping |
|---|---|---|---|
| Data modality | RGB images | RGB video | Multi-spectral satellite (6 bands) |
| Model scale | ~2.6M params (YOLO11n) | Reconstruction tools | 300M+ params (Prithvi-EO-2.0) |
| Task | Object detection | 3D reconstruction | Semantic segmentation |
| Deployment | Edge (Pi 3B) | User laptop CLI | Batch server / cloud |
| Iteration on models | Many runs, hyperparameter tuning | Per-scene hyperparameters | Few runs, mostly head/decoder choices |
| All 8 epics used | Yes | 7 (no monitoring) | Yes (monitoring is real) |

## Project context (abridged)

- **Team:** 4-person bootcamp team + team lead.
- **Compute:** GPU strongly recommended for fine-tuning Prithvi (~300M params). Colab Pro or a small cloud GPU (single T4/A10) is sufficient. Inference-only work runs on CPU laptops for very small tiles.
- **Model:** [Prithvi-EO-2.0-300M-TL](https://huggingface.co/ibm-nasa-geospatial/Prithvi-EO-2.0-300M-TL) as the default baseline. A pre-fine-tuned [Prithvi-EO-2.0-300M-TL-Sen1Floods11](https://huggingface.co/ibm-nasa-geospatial/Prithvi-EO-2.0-300M-TL-Sen1Floods11) exists — good for comparison / starting benchmarks.
- **Fine-tuning framework:** [TerraTorch](https://github.com/IBM/terratorch) (IBM, Apache 2.0). The older [hls-foundation-os](https://github.com/NASA-IMPACT/hls-foundation-os) reference is also available if TerraTorch has issues.
- **Corpus:** [Sen1Floods11](https://github.com/cloudtostreet/Sen1Floods11) — 446 hand-labeled 512×512 chips across 14 biomes, 357 ecoregions, 6 continents, 11 flood events (2018–2020).
- **Deliverable:** A CLI (and containerized service) that takes a Sentinel-2 tile and produces a georeferenced flood-extent GeoTIFF + GeoJSON, plus a small monitoring dashboard for continuous operation.

## Key references

Cited inline throughout the epics where relevant.

- **Prithvi-EO-2.0 (primary model reference):** Roy, S., Fraccaro, P., Le, S., et al. (2024). *Prithvi-EO-2.0: A Versatile Multi-Temporal Foundation Model for Earth Observation Applications.* arXiv:2412.02732. [Paper](https://arxiv.org/abs/2412.02732) · [GitHub](https://github.com/NASA-IMPACT/Prithvi-EO-2.0) · [HuggingFace models](https://huggingface.co/ibm-nasa-geospatial)
- **Prithvi-EO-1.0 (original foundation model paper):** Jakubik, J., Roy, S., Phillips, C. E., et al. (2023). *Foundation Models for Generalist Geospatial Artificial Intelligence.* arXiv:2310.18660. [Paper](https://arxiv.org/abs/2310.18660)
- **Sen1Floods11 (corpus paper):** Bonafilia, D., Tellman, B., Anderson, T., & Issenberg, E. (2020). *Sen1Floods11: A Georeferenced Dataset to Train and Test Deep Learning Flood Algorithms for Sentinel-1.* CVPR Workshops. [Paper](https://openaccess.thecvf.com/content_CVPRW_2020/html/w11/Bonafilia_Sen1Floods11_A_Georeferenced_Dataset_to_Train_and_Test_Deep_Learning_CVPRW_2020_paper.html) · [Repo & data](https://github.com/cloudtostreet/Sen1Floods11)
- **TerraTorch (fine-tuning framework):** [GitHub](https://github.com/IBM/terratorch) · Apache 2.0
- **Assessment paper (useful benchmark reference):** Li, W., & Hsu, C.-Y. (2023). *Assessment of a New GeoAI Foundation Model for Flood Inundation Mapping.* arXiv:2309.14500. [Paper](https://arxiv.org/abs/2309.14500)
