# MLflow experiment tracking

All training runs logged to MLflow. Config, metrics, artifacts.

### Upstream / Downstream contract

Team-internal: whoever runs experiments uses the shared MLflow.

### Cross-team contact points

- **T7 Platform** may provide MLflow instance in shared Compose; confirm early. If not, T2 runs it locally.
- Timing: Week 2.

### Definition of Done

- MLflow instance running (local or shared)
- Every training script logs config + metrics + artifacts
- Team members can compare runs

### Demo

Compare baseline vs promotion model in MLflow UI.

### Subtasks

- MLflow setup
- Logging in all training scripts
