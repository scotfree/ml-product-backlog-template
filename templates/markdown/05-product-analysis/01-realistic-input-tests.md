# End-to-end tests on realistic inputs

_Run the whole pipeline on inputs that look like what it'll see in the wild — not the curated test set._

- **Upstream/downstream:** _Deployment consumes the results as a go/no-go signal. Model analysis may have flagged model-level issues; this catches system-level ones._
- **Definition of done:** _A repeatable test that runs the full pipeline on a set of "realistic" inputs (messy, ambiguous, out-of-distribution) and reports where it succeeds and fails._
- **Demo:** _Run the test suite; walk through one clear pass and one clear failure._
- **Subtasks:**
  - _Assemble a small set of realistic inputs — not from the training or test data._
  - _Decide what "success" looks like at the system level, not just the model level._
