# ML Product Backlog Template

A reusable structure for scoping ML pipeline projects. Not a curriculum, not a lab — a shape for the work, adaptable to any domain (CV, SfM, tabular, NLP, optimization).

## What's here

- **`CARD_TEMPLATE.md`** — what a good issue looks like.
- **`TEAM_LEAD_NOTES.md`** — how to adapt this for your team; the scaffolding dial.
- **`templates/markdown/`** — the reusable backlog, one directory per epic, one file per card.
- **`templates/github-templates/`** — the same content as GitHub issue templates you can drop into `.github/ISSUE_TEMPLATE/`.
- **`examples/ag-bot-cv/`** — a fully filled-in example: agricultural computer vision on a hexapod robot (from the Robo-Greeno project). Same directory shape as `templates/markdown/`, but every card is adapted to that specific project.

## How to use

1. Read `CARD_TEMPLATE.md` so the shape of a good card is clear.
2. Read `TEAM_LEAD_NOTES.md` and decide where on the scaffolding dial your team should start.
3. Copy `templates/markdown/` (or the GitHub-templates version) into your project repo.
4. Adapt each card to your domain, deleting the prompt language as you fill it in. Use `examples/ag-bot-cv/` as a reference for what "adapted" looks like.
5. Create GitHub Issues (or your team's equivalent) from the adapted cards. Team can refine further in planning.

## The eight epics

1. **Pipeline** — data flow, code architecture, interfaces
2. **Corpus** — the actual dataset(s) you'll work with
3. **Modeling** — architecture selection and training runs
4. **Model analysis** — is the model itself any good?
5. **Product analysis** — does the end-to-end system do the job?
6. **Deployment** — packaging, serving, running somewhere real
7. **Documentation** — what future-you and others need to know
8. **Monitoring & Maintenance** — how you'll know it's still working

Not every project needs all eight in equal measure. Adapt.
