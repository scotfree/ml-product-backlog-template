# Epic: Deployment (Ag-Bot-CV)

Package as a `pip`-installable Python wheel with models bundled as package data. Entry point `python -m robogreeno_detection`. Runs as a long-lived process on the Pi 3B; Embedded owns the service supervision (systemd or otherwise). Benchmark all three CPU runtime candidates (NCNN, ONNX Runtime, TFLite+XNNPACK) before locking in.

## Cards in this epic

1. Package the model for use
2. Runnable by someone who isn't you
3. Benchmark in the target environment
