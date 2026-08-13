# Design decisions log

`docs/decisions.md` capturing why choices were made. Especially why we didn't do the obvious other thing.

- **Upstream/downstream:** Future maintainers, cross-team reviewers, the portfolio writeup.
- **Definition of done:** 8–15 entries by end of program. Each: decision, alternatives considered, reasoning, date.
- **Demo:** Read one entry aloud; explain the trade-off.
- **Subtasks:**
  - Suggested entries specific to this project:
    - Why Prithvi-EO-2.0 over other geospatial foundation models (SatMAE, Scale-MAE, DOFA, etc.).
    - Why 300M over 600M (or vice versa).
    - Why TerraTorch over hls-foundation-os.
    - Why event-based splits (per-region generalization matters).
    - Why we froze the backbone (or didn't).
    - Why our loss function (Dice / weighted CE / focal — whichever the team chose).
    - Whether we're comparing against or building on the pre-fine-tuned Sen1Floods11 checkpoint.
