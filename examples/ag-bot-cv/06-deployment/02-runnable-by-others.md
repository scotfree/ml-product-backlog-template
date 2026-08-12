# Runnable by someone who isn't you

## Description

Pavan installs the wheel on a fresh Pi image and runs the pipeline against the real broker within 15 minutes, using only the README. This validates the whole delivery chain (packaging + docs + config) before we hand it off for real.

## Upstream / Downstream contract

- Embedded (Pavan) is the tester and target consumer.
- Documentation (Card 07-documentation/01) is where the fixes land.

## Definition of Done

Pavan follows the README on a clean Pi; goes from `pip install` to a live detection appearing on the broker in under 15 minutes; no questions asked to Data B.

## Demo

Pavan demos it. We watch.

## Subtasks

- README section: "Install on Raspberry Pi 3B" — exact `pip` command, exact config snippet.
- Verify wheel installs on ARM without needing to build wheels from source (pre-built ARM wheels for dependencies).
- Include a `configs/pi.yaml` template that only needs broker URL filled in.
- Fix whatever Pavan stumbles on before the hand-off (Card 05-product-analysis/03).

## Estimate

~1 day, mostly chasing ARM wheel availability.
