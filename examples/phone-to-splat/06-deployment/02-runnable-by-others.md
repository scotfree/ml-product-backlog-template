# Runnable by someone who isn't you

An external tester installs the CLI on their laptop and runs it on a video they capture themselves. Under 30 minutes from `pip install` to a working .glb + accuracy report, using only the README.

- **Upstream/downstream:** External consumers. Documentation (Card 07-documentation/01) is where fixes land.
- **Definition of done:** The Product Analysis hand-off test (Card 05-product-analysis/03) passes: an outside person goes from install to viewable output in under 30 minutes, no questions asked.
- **Demo:** External tester demos it; team watches and takes notes.
- **Subtasks:**
  - "Install" section of the README: exact commands for pip install and for the Docker path.
  - "Quickstart" section: capture a video following our protocol, run one command, view the result.
  - Common-errors section: what to do when COLMAP fails, when GPU is missing, when the video is too short.
