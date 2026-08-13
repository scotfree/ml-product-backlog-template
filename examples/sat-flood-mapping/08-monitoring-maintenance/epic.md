# Epic: Monitoring & Maintenance (Sat-Flood-Mapping)

Unlike phone-to-splat, this is a real running system. Flood mapping deployed in production processes Sentinel-2 tiles continuously (or on-demand during events). Real production concerns: sensor drift (Sentinel-2 sensor characteristics change over years), domain shift (climate change → new flood patterns), catastrophic failures during active flood events (the worst possible time for the system to be broken).

## Cards in this epic

1. Failure-mode inventory
2. Logging and metrics in production
3. Retraining and update process
