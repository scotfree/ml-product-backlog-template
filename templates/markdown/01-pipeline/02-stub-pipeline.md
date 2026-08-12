# Build a stub pipeline end-to-end

_Every stage returns fake but plausibly-shaped data. The whole thing runs._

- **Upstream/downstream:** _Which teammate's real code will replace which stubs, and when?_
- **Definition of done:** _`run.py` (or equivalent) produces plausible output from a canned input, with all stages exercised._
- **Demo:** _Run the pipeline live from an input file to a printed/saved output._
- **Subtasks:**
  - _Fake input generator._
  - _Stub for each stage that returns the right shape._
  - _One command that runs the whole thing._
