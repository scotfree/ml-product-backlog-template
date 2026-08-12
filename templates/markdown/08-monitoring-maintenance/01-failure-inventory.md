# Failure-mode inventory

_What could go wrong? How would you notice?_

- **Upstream/downstream:** _Whoever runs this in production needs to know what to watch for. Documentation captures it._
- **Definition of done:** _A short list: failure mode, symptom, detection idea, response idea._
- **Demo:** _Walk through the top three; explain how you'd catch them._
- **Subtasks:**
  - _Data drift (inputs look different from training)._
  - _Silent failures (model runs but produces garbage)._
  - _Infrastructure failures (crashes, timeouts, storage)._
