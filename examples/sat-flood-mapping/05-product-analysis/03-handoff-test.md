# Hand-off test — someone else runs it

Someone outside the team (a mentor, a student from another team, a friend familiar with GIS) installs the CLI on their machine, downloads a Sentinel-2 tile of an event they pick, runs the pipeline, and gets a georeferenced flood map. Under 45 minutes end-to-end using only the README.

- **Upstream/downstream:** Deployment (Card 06-deployment/02) is the target consumer. Documentation (Card 07-documentation/01) is where fixes land.
- **Definition of done:** External person goes from install to viewable flood map in QGIS under 45 minutes with no questions asked. Every stumble filed as a GitHub issue.
- **Demo:** External tester demos it; team watches and takes notes.
- **Subtasks:**
  - Schedule 60 minutes with the tester.
  - Provide clear instructions on how to acquire a Sentinel-2 tile (this is the hardest step for someone new to geospatial workflows).
  - Watch without helping; take notes on every hesitation.
  - Fix every stumble before demo day.
