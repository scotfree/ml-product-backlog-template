# Logging and metrics in production

_Log enough to debug later without logging so much you drown in noise._

- **Upstream/downstream:** _Anyone diagnosing a future problem depends on these logs._
- **Definition of done:** _Deployed system emits structured logs and a small set of metrics; a teammate can query them._
- **Demo:** _Trigger a synthetic problem; show how the logs surface it._
- **Subtasks:**
  - _Decide log format and destination._
  - _Decide a minimal metric set (throughput, error rate, latency, whatever fits)._
