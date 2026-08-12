# Epic: Pipeline (Ag-Bot-CV)

The Data B detection pipeline on the Pi: camera capture → image-quality gate → detector inference → MQTT publish. Interfaces to Embedded (upstream, camera), Data A (mid-stream, pose lookup), and Cloud (downstream, MQTT + MinIO).

## Cards in this epic

1. Design the pipeline interface
2. Build a stub pipeline end-to-end
3. Replace stubs with real components (incremental)
