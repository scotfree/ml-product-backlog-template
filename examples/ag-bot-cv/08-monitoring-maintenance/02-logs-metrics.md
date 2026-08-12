# Logging and metrics in production

## Description

Structured JSON logs to stdout (captured by whatever supervisor Embedded runs). Periodic aggregate stats published via MQTT every 60s: frame counts, skip rates by reason, detection counts by task, latency histogram. Also serves as the liveness heartbeat.

## Upstream / Downstream contract

- Cloud (Kayvan) consumes the MQTT stats for the AgCloud dashboard.
- Embedded consumes stdout logs via journald or equivalent.
- Documentation captures the log format.

## Definition of Done

Pipeline emits JSON logs on stdout with fields (timestamp, level, event, task, robot_id, extra). MQTT stats message published every 60s on `robogreeno/stats/<robot_id>`. Kayvan confirms the stats fit his dashboard needs.

## Demo

Run pipeline for 5 minutes; show `mosquitto_sub` receiving stats messages; grep logs to trace a specific frame end-to-end.

## Subtasks

- Log format: JSON, one line per event, `python-json-logger` or similar.
- Stats aggregation: rolling 60s window, counts + latency percentiles.
- Coordinate stats schema with Kayvan (see 08-monitoring-maintenance email thread).
- Skip reasons enumerated (blur, dark, out-of-focus, motion, pose-stale).

## Estimate

~2 days, gated on Kayvan confirming the stats schema.
