# Hand-off test — someone else runs it

## Description

Pavan (Embedded) runs the pipeline on a fresh Pi image using only the README, on a real detection task, with the real MQTT broker. He shouldn't have to ask Data B any questions. Anywhere he stumbles is a bug in the docs or the packaging.

## Upstream / Downstream contract

- Deployment (Card 06-deployment/02) is the target consumer for this test.
- Documentation (Card 07-documentation/01) is where the fixes land.

## Definition of Done

Pavan runs `pip install robogreeno-detection && python -m robogreeno_detection --config configs/pi.yaml` on a clean Pi and gets a detection published to the real MQTT broker within 15 minutes. Every stumble filed as a GitHub issue.

## Demo

Have Pavan demo it on the Pi in the shared lab — not the team lead.

## Subtasks

- Schedule 30 minutes with Pavan for the test.
- Watch without helping; take notes.
- File one issue per stumble; fix before demo.

## Estimate

Hours for the test itself; ~1 day for the fixes it surfaces.
