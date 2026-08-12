# Logging and metrics in production

## Description

_Log enough to debug later without logging so much you drown in noise._

## Upstream / Downstream contract

_Anyone diagnosing a future problem depends on these logs._

## Definition of Done

_Deployed system emits structured logs and a small set of metrics; a teammate can query them._

## Demo

_Trigger a synthetic problem; show how the logs surface it._

## Subtasks

- _Decide log format and destination._
- _Decide a minimal metric set (throughput, error rate, latency, whatever fits)._

## Estimate

_Rough size — minutes, hours, or days. If it's more than a few days, break it up._
