# Design geographic splits

**The most important corpus decision in this project.** Random splits are misleading for global flood mapping: if you train on chips from a flood event in India and test on other chips from the *same* event, your model looks great but hasn't actually learned to generalize to new regions or events. Geographic (event-based or region-based) splits give you a truthful measure of real-world performance.

- **Upstream/downstream:** Model Analysis's headline number depends entirely on how this split is defined. Product Analysis's realistic-input tests inherit this thinking.
- **Definition of done:** `docs/splits.md` explains the split policy with rationale. `flood_mapping/data/splits.py` implements it deterministically. Test-set access gated so nobody accidentally trains on it.
- **Demo:** Show the geographic distribution of train vs. test on a map. Explain why an event-based split is more honest than a random split.
- **Subtasks:**
  - **Option A (event-based):** hold out entire flood events (e.g., train on 8 events, val on 1, test on 2). Strongest generalization signal; the paper's official split does this.
  - **Option B (region-based):** hold out entire regions (e.g., train on Africa+Asia, test on Americas). Even harder generalization test.
  - **Option C (random within events):** easier metrics but misleading — use only for sanity checks, not headline reporting.
  - **Recommendation:** default to Sen1Floods11's official event-based splits (they exist in the repo). Document why. Reserve Option C for internal debugging only.
  - Add a "reveal" guard in code that raises if training accidentally touches test chips.
