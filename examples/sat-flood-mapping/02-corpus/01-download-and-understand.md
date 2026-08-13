# Download and understand Sen1Floods11

Get the dataset, understand its structure, verify licensing and attribution requirements.

- **Upstream/downstream:** Modeling needs to know band ordering, image dimensions, label semantics. Deployment inherits any licensing constraints that propagate to a deployed system.
- **Definition of done:** Dataset downloaded to shared storage. `docs/dataset.md` covers: source, license/attribution requirements, band ordering, label semantics (0=no water, 1=water/flood, -1=no-data/clouds), file structure, metadata schema.
- **Demo:** Load 3 sample chips (a flood, a permanent-water body, a mostly-cloud scene); show the labels overlaid.
- **Subtasks:**
  - Download from `gs://sen1floods11/` via `gsutil`, or HuggingFace mirror (`harshinde/sen1floods11`).
  - Verify chip count: 446 hand-labeled Sentinel-2 chips (plus ~4,385 weakly-labeled — decide whether to use).
  - **Attribution**: cite Bonafilia et al., 2020 in project README and any published outputs. See [dataset paper](https://openaccess.thecvf.com/content_CVPRW_2020/html/w11/Bonafilia_Sen1Floods11_A_Georeferenced_Dataset_to_Train_and_Test_Deep_Learning_CVPRW_2020_paper.html).
  - **License nuance**: no formal OSS license posted on the Sen1Floods11 repo. Cloud to Street (now Floodbase) is a Public Benefit Corporation; the dataset is freely available for research/humanitarian use. **If the deployed system is commercial, contact Floodbase directly first.** This is a real licensing situation students should learn to handle.
  - Sentinel-2 imagery itself is Copernicus/ESA — open access under [Copernicus Sentinel Data License](https://scihub.copernicus.eu/twiki/pub/SciHubWebPortal/TermsConditions/Sentinel_Data_Terms_and_Conditions.pdf), free with attribution.
