# Team 6 — Explainability & Impact

Turn technical model signals into understandable evidence and business priority. Consumer of many teams' outputs — aggregation-heavy.

## Applicable epics

Pipeline, Model Analysis (light — SHAP quality checks), Product Analysis, Deployment, Documentation. Skips Corpus, Modeling (no ML model of their own beyond rules/SHAP), Monitoring (light, skipped for brevity).

## Cross-team role

Consumes from T5 (anomaly.detected, drift.detected — primary trigger), T2 (forecast), T3 (peer), T4 (context) — the latter three as optional evidence. Publishes to T7 (persistence) and T8 (UI). Business impact inputs (price/margin) from T1.
