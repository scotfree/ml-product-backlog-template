# GNN vs baseline decision point

Implement STGNN/GNN per Paper 2 and compare against the similarity baseline. Decide by Week 6 which ships.

### Upstream / Downstream contract

Team-internal: whoever builds the GNN + whoever manages the comparison.

### Cross-team contact points

- **T7 Platform** may provide Neo4j if graph DB is chosen path. Confirm early.
- Timing: Week 4-6. Decision by Integration Gate (Week 6).

### Definition of Done

- GNN implementation with published metrics
- Head-to-head comparison against baseline
- Documented decision: which method ships, why

### Demo

Metric comparison table + qualitative peer-set differences.

### Subtasks

- PyTorch Geometric setup
- Graph construction
- Training loop
- Comparison harness
