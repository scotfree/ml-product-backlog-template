# Epic: Deployment (Sat-Flood-Mapping)

Package as a CLI + Docker container. Consumer: an ops team (or automated system) that receives a Sentinel-2 tile and needs a georeferenced flood map back within a target latency (minutes, not seconds — flood mapping is batch, not real-time).

Different flavor from ag-bot-cv (no edge device) and from phone-to-splat (no per-run heavy training). The distinctive concern here is **model size**: Prithvi-300M is ~1.2 GB on disk. That's fine for a server but not trivial for cold-start latency.

## Cards in this epic

1. Package as a CLI + container
2. Runnable by someone who isn't you
3. Benchmark on realistic hardware
