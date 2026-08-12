# End-to-end tests on realistic inputs

## Description

Assemble a set of "realistic" inputs that are *not* from LaboroTomato / IP102 / PlantVillage — instead: webcam captures of tomatoes on desks, iPhone shots of houseplants, blurry motion frames simulating a walking hexapod. Run the full pipeline; report where it succeeds and fails.

## Upstream / Downstream contract

- Deployment (all cards) consumes results as a go/no-go signal.
- Feeds back to Modeling if a domain gap becomes obvious.

## Definition of Done

`tests/realistic/` directory with ~30 curated real-world inputs and expected outcomes. `pytest tests/realistic/` runs the pipeline on each and produces a pass/fail report.

## Demo

Run the suite; walk through one clear pass (obvious ripe tomato) and one clear failure (bad lighting misclassified).

## Subtasks

- Team captures ~30 images with phones/webcams — deliberately not from training data.
- Label them with "expected" outcomes (may just be "should detect a tomato here", not full boxes).
- System-level success ≠ pixel-perfect model accuracy — closer to "did the MQTT publish look right?"

## Estimate

~2 days, plus a shared evening of everyone taking photos.
