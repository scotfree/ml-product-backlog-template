# Package the model for use

## Description

Build `robogreeno-detection` as a Python wheel. Models bundled as package data via `pyproject.toml` `[tool.setuptools.package-data]`. Entry point is `python -m robogreeno_detection` — a long-lived process that logs to stdout, handles SIGTERM, and reads config from a YAML file.

## Upstream / Downstream contract

- Embedded (Pavan) consumes the wheel and decides how to supervise it on the Pi (systemd is his call, not ours).
- Cloud consumes the resulting MQTT stream.

## Definition of Done

`pip install dist/robogreeno_detection-*.whl` on a clean Python 3.11 env installs code + models. `python -m robogreeno_detection --config configs/pi.yaml` runs the pipeline. `SIGTERM` triggers graceful shutdown (drain + disconnect + exit 0).

## Demo

Install the wheel in a fresh venv on a laptop; run it against local `mosquitto`; kill with SIGTERM; show clean shutdown in logs.

## Subtasks

- `pyproject.toml` with `robogreeno_detection` package + `models/` as package data.
- `robogreeno_detection/__main__.py` with SIGTERM handler and structured stdout logging.
- YAML config schema: MQTT broker URL, topic prefix, model paths, robot_id.
- Confirm wheel size is acceptable (< 100 MB, PyPI hard limit — expect 20–50 MB with 3 quantized models).

## Estimate

~2 days.
