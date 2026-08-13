# Epic: Corpus (Sat-Flood-Mapping)

Sen1Floods11 — an existing public dataset. Unlike phone-to-splat, students don't build the corpus themselves; unlike ag-bot-cv, geospatial data has a licensing/attribution nuance worth surfacing (many "public" satellite datasets have use restrictions).

The interesting decision in this epic is **how to split** the data. Random splits are meaningless for a global flood mapping model — you want geographic splits (train on some flood events, test on completely different ones) to measure real generalization.

## Cards in this epic

1. Download and understand Sen1Floods11
2. Characterize the corpus
3. Design geographic splits
