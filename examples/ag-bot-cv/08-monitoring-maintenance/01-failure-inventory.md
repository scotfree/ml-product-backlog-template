# Failure-mode inventory

Enumerate what could go wrong once the pipeline is deployed. Data drift (new pest species, seasonal lighting changes), silent failures (detections all-zero because the camera is dirty), infrastructure (Pi runs out of disk, MinIO sync fails), integration (broker password rotated).

- **Upstream/downstream:** Feeds Card 08-monitoring-maintenance/02 (what metrics to collect) and Card 07-documentation/02 (decisions log).
- **Definition of done:** `docs/failure-modes.md`: table of failure mode, symptom, detection idea, response idea. At least 10 entries.
- **Demo:** Walk through the top three; explain how you'd catch them.
- **Subtasks:**
  - Data drift: new pest species not in IP102, seasonal changes, new crops.
  - Silent failures: all detections empty, all confidence scores identical, MQTT publishes stop.
  - Infra: SD card full, MinIO local bucket full, network partition, Pi thermal throttling.
  - Integration: broker credentials rotated, topic renamed, schema version bumped by Cloud.
