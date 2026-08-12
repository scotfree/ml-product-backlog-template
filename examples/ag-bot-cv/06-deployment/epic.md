# Epic: Deployment (Ag-Bot-CV)

## What this epic covers

Package as a `pip`-installable Python wheel with models bundled as package data. Entry point `python -m robogreeno_detection`. Runs as a long-lived process on the Pi 3B; Embedded owns the service supervision (systemd or otherwise). Benchmark all three CPU runtime candidates (NCNN, ONNX Runtime, TFLite+XNNPACK) before locking in.

## Cards in this epic

1. Package the model for use
2. Runnable by someone who isn't you
3. Benchmark in the target environment

## Success criteria

A wheel Pavan can `pip install` on a clean Pi 3B that runs, publishes, and shuts down cleanly on SIGTERM — with a benchmark table backing an explicit runtime recommendation per task. Demoable as install-to-detection on the Pi in under 15 minutes.
