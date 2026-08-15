# Consume sales.canonical.ready

Feature pipeline that runs against T1's fixture bundle (Week 1) or live Kafka (Week 3+).

### Upstream / Downstream contract

Team-internal: feature owner reads events; modeling owner reads features.

### Cross-team contact points

- **T1 Data** provides fixture bundle (Week 1) and Kafka stream (Week 3+). Confirm exact fields needed: at minimum store_id, product_id, timestamp, actual_sales, price, promotion, holiday.
- **T7 Platform** provides consumer template for the Kafka switch-over.
- Timing: fixtures Week 1; Kafka Week 3 (Foundation Gate).

### Definition of Done

- Feature pipeline runs from fixture bundle end-to-end
- Same code path works with Kafka source (config switch)
- Feature schema stable

### Demo

Show features generated from a fixture; then swap to Kafka source; identical output.

### Subtasks

- Fixture reader
- Kafka consumer (via T7 template)
- Feature engineering (lag, rolling, calendar, promotion)
