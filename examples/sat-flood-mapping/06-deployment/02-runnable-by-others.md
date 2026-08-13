# Runnable by someone who isn't you

External tester installs the CLI or pulls the Docker image, runs it on a tile they supply, gets a georeferenced flood map. Under 45 minutes from `pip install` (or `docker pull`) to a viewable output.

- **Upstream/downstream:** External consumer. Documentation (Card 07-documentation/01) is where fixes land.
- **Definition of done:** The Product Analysis hand-off test (Card 05-product-analysis/03) passes: external person gets a flood map in under 45 minutes, no questions asked.
- **Demo:** External person demos it. Team watches, takes notes.
- **Subtasks:**
  - "Install" section: pip and Docker paths, both.
  - "Quickstart": here's how to acquire a Sentinel-2 tile, here's the one command to run.
  - Common-errors section: model download issues, CRS issues (very common for people new to geospatial data), missing bands, cloudy inputs.
