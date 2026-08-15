# Weather API integration (Open-Meteo)

Fetch and cache weather for the store locations. Cache aggressively — demo cannot depend on live external calls.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T1 Data** owns store metadata including geography. Confirm which datasets have defensible location data (M5 does not; Walmart partial). If store location isn't defensible, weather cannot be joined — Paper 5 becomes a separate experiment.
- Timing: Week 2. Cached snapshot required by Week 8 for demo.

### Definition of Done

- Weather fetched per store, cached to Parquet
- Cache is authoritative for demo (offline-capable)
- Documented what happens if API is down

### Demo

Disable network; pipeline still produces weather-joined events from cache.

### Subtasks

- Open-Meteo client
- Location → weather cache
- Fallback path
