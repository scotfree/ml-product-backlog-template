# README that lets someone reproduce a run

A newcomer clones `robogreeno-detection`, sets up a Python env, downloads LaboroTomato, and reproduces the fruit YOLO11n training run in under an hour. Same README covers install on a Pi and running inference against a broker.

- **Upstream/downstream:** Any future contributor and any portfolio reviewer. Also the hand-off test (Card 05-product-analysis/03) uses it as source of truth.
- **Definition of done:** Someone outside the team (test with a student from another team — Data A or Cloud) follows the README on a clean laptop and reproduces a training run without asking questions.
- **Demo:** Have that outside student show what they did in 3 minutes.
- **Subtasks:**
  - Setup: Python version, dependencies, dataset download commands.
  - One command each for: data prep, train fruit model, evaluate, run inference on a sample image.
  - Separate "Run on Pi" section for deployment.
  - Expected outputs at each step (so people can tell they're on track).
