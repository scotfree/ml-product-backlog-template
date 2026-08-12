# Design decisions log

A running `docs/decisions.md` capturing why choices were made — especially why we didn't do the obvious other thing. Add an entry any time a decision would take more than 5 minutes to re-derive.

- **Upstream/downstream:** Future maintainers, cross-team reviewers, and the portfolio writeup all consume this.
- **Definition of done:** 10–15 entries by end of program. Each entry: decision, alternatives considered, reasoning, date.
- **Demo:** Read out one entry (e.g., "Why NCNN over ONNX Runtime for pest") and explain the trade-off.
- **Subtasks:**
  - Entry for: YOLO11 vs. RF-DETR (framework + license).
  - Entry for: post-training vs. quantization-aware quantization.
  - Entry for: edge inference vs. cloud inference (why we don't stream frames).
  - Entry for: pull-based pose lookup vs. subscribing to Data A's 50Hz stream.
  - Entry for: Python wheel vs. Docker container as the delivery format.
