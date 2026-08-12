# Integration and edge-case tests

## Description

What happens when: camera returns nothing, IQA gate rejects every frame, MQTT broker is unreachable, pose lookup times out, model checkpoint file is corrupted? Pipeline should degrade gracefully — never crash silently, always log clearly.

## Upstream / Downstream contract

- Deployment (Cards 06-deployment/02, 06-deployment/03) needs to know the failure modes.
- Documentation (Card 08-monitoring-maintenance/01) inherits this as the failure-mode inventory.

## Definition of Done

`tests/edge_cases/` covers each named case. Pipeline either handles gracefully or fails with a clear log message and non-zero exit. No silent hangs, no crashes without context.

## Demo

Kill the local `mosquitto` broker mid-run; show the pipeline logging the disconnect and either retrying or exiting cleanly.

## Subtasks

- Camera: `cap.read()` returns `(False, None)`.
- IQA: 100 consecutive rejects (real if lens is capped).
- MQTT: broker unreachable at startup; disconnected mid-run.
- Pose: Data A's API returns stale (>500ms old) data or times out.
- Model: corrupted `.pt` file.

## Estimate

~2 days.
