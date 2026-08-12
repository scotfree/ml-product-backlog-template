# Integration and edge-case tests

_What happens when input is empty, malformed, huge, or unexpected? What happens when a downstream service is slow or down?_

- **Upstream/downstream:** _Deployment needs to know the failure modes. Documentation captures them._
- **Definition of done:** _A short list of edge cases with expected behavior, and tests confirming the system does what's expected (or fails cleanly)._
- **Demo:** _Trigger 2–3 edge cases live; show the system either handling them or failing gracefully._
- **Subtasks:**
  - _Empty input, malformed input, unusually large input._
  - _Failure of a dependency (broken model file, missing config, no network)._
  - _Concurrent or repeated calls, if that's relevant to the deployment target._
