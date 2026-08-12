# End-to-end training run, even if bad

_A model trained on your data. Doesn't need to be good — needs to exist._

- **Upstream/downstream:** _Analysis needs a model to evaluate. Deployment needs a model to package._
- **Definition of done:** _A saved checkpoint from a run on your real data, plus the exact command that produced it._
- **Demo:** _Run inference on one example using the trained model._
- **Subtasks:**
  - _Config file or script capturing all hyperparameters._
  - _Checkpoint saved to a known location, versioned._
