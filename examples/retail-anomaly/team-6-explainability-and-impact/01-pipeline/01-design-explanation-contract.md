# Design explanation.completed and impact.completed contracts

Two payloads. explanation.completed: root cause summary, evidence pointers, confidence. impact.completed: severity, priority_score, business_impact_estimate.

### Upstream / Downstream contract

Team-internal.

### Cross-team contact points

- **T8 Product** is the primary consumer for both payloads (renders in manager UI). Get their input on what fields the UI actually renders — don't over-design.
- **T7 Platform** registers schemas.
- Timing: Contract Gate Week 1.

### Definition of Done

- Both schemas in repo
- Mock payloads
- T8 sign-off

### Demo

Walk T8 through mock payloads.

### Subtasks

- Draft schemas
- Mock payloads
- T8 review
