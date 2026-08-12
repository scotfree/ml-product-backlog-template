# Epic: Monitoring & Maintenance (Ag-Bot-CV)

## What this epic covers

Once the pipeline is running on the Pi in a greenhouse, how will we know it's still doing the right thing? Local structured logs, periodic aggregate stats via MQTT (heartbeat + skip rates), and a plan for retraining when the data drifts.

## Cards in this epic

1. Failure-mode inventory
2. Logging and metrics in production
3. Retraining and update process

## Success criteria

At least 10 documented failure modes, each with a detection idea backed by a log field or MQTT stat that actually exists, plus a written retraining process with triggers and a rollback plan. Demoable by tracing one frame end-to-end through the logs.
