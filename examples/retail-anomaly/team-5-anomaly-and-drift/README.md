# Team 5 — Anomaly & Drift

Direct anomaly scoring + temporary-vs-persistent drift classification. Papers 6 (Xiaoyang, dual LSTM-AE) and 3 (DriftGuard, hierarchical concept drift) core.

## Applicable epics

Pipeline, Modeling, Model Analysis, Product Analysis, Deployment, Monitoring. Documentation skipped for brevity — team lead can add later.

## Cross-team role

Consumes from T1 (canonical events + synthetic scenarios). Publishes to T6 and T8 (anomaly.detected, drift.detected). Explicitly does NOT wait for T2/T3/T4 outputs — fusion is enhancement, not dependency.
