# Reproducible evaluation harness

_One command that takes a model and produces the same numbers every time._

- **Upstream/downstream:** _Everyone comparing models depends on this. Product analysis may extend it._
- **Definition of done:** _`evaluate.py --model X` produces a report; running it twice gives identical numbers._
- **Demo:** _Run the harness on two models and show the comparison._
- **Subtasks:**
  - _Locked test set._
  - _Seeded randomness where relevant._
