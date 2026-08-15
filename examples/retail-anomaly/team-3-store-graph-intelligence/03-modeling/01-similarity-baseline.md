# Store similarity baseline

Simple similarity/nearest-peer method (correlation on historical sales, or feature-vector cosine). Permanent demo fallback.

### Upstream / Downstream contract

Team-internal: baseline owner + eval owner.

### Cross-team contact points

None directly.

### Definition of Done

- Similarity function implemented
- Peer sets computed for all stores
- Sanity check: known-similar stores (same region, same format) appear as peers

### Demo

Show peer set for one store; explain why those are peers.

### Subtasks

- Similarity function
- Peer set generation
- Visual sanity check
