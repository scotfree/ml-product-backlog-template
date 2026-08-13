# End-to-end tests on new inputs

Have a team member capture ~5 new scenes from outside the training corpus — different objects, different rooms, different lighting. Run the full pipeline end-to-end. Report per-scene: did it complete? Did it produce a viewable file? Did the accuracy protocol run and produce a number?

- **Upstream/downstream:** Deployment consumes this as go/no-go signal. Feeds back to Corpus (any systematic capture-protocol misses?) and Modeling (any consistent tuning gaps?).
- **Definition of done:** `tests/realistic/` with the new captures and expected outcomes (may just be "should produce a viewable file with accuracy report") — not per-scene ground truth (that's the whole point of testing on new inputs). `pytest tests/realistic/` runs the pipeline and reports success/failure.
- **Demo:** Run the suite; walk through one clear pass and one clear failure.
- **Subtasks:**
  - New captures deliberately different from corpus (different objects, environments).
  - Include at least one scene from each difficulty tier (some easy wins, some honest failures).
  - System-level success ≠ perfect geometry — closer to "did the pipeline produce artifacts a downstream user could use?"
