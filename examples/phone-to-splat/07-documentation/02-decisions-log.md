# Design decisions log

Running `docs/decisions.md` capturing why choices were made — especially why we didn't do the obvious other thing.

- **Upstream/downstream:** Future maintainers, cross-team reviewers, and the portfolio writeup all consume this.
- **Definition of done:** 8–15 entries by end of program. Each: decision, alternatives considered, reasoning, date.
- **Demo:** Read out one entry; explain the trade-off.
- **Subtasks:**
  - Suggested entries specific to this project:
    - Why COLMAP over GLOMAP or OpenMVG.
    - Why gsplat over the original 3DGS reference code (license!).
    - Why we chose the accuracy protocol we did (see Corpus card 03 rationale).
    - Why we require an in-frame scale reference vs. post-hoc alignment.
    - Why the CLI is the primary deployment target vs. a web service.
    - Why we split evaluation into three metric layers.
