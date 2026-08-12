# Define evaluation metrics

_What number(s) tell you the model works? Justify against the actual goal, not the default from the tutorial._

- **Upstream/downstream:** _Modeling needs to know what to optimize toward. Product analysis inherits these as one input among several._
- **Definition of done:** _One page: what metrics, why them, what values would count as success/failure._
- **Demo:** _Explain the chosen metric in one sentence and why it beats the obvious alternatives._
- **Subtasks:**
  - _Consider what "wrong" looks like: false positives vs. false negatives, tail cases, expensive mistakes._
  - _Sanity-check the metric against a naive baseline — "always predict majority class" should score poorly._
