# Design the capture protocol and reference-object menu

Decide how videos should be captured to give SfM the best chance of success, and pick a diverse menu of reference objects the team will actually capture. Both parts matter: bad captures produce bad reconstructions regardless of tooling, and a menu that spans easy-to-hard scenes is what makes Model Analysis interesting.

- **Upstream/downstream:** Modeling (03-modeling/02) will run reconstructions on this corpus; the capture protocol determines how often those runs succeed. Model Analysis (04-model-analysis/03) needs a diverse set of scenes to characterize failure modes.
- **Definition of done:** `docs/capture-protocol.md` covering: phone settings (focus lock, exposure lock, resolution, framerate), motion pattern (orbit, arc, coverage, overlap targets), scene setup (lighting, background). Plus `docs/reference-objects.md` listing 8–12 candidate objects across a difficulty spectrum.
- **Demo:** Walk through the capture protocol; show two example captures — one good (steady orbit, high overlap), one bad (fast pan, motion blur).
- **Subtasks:**
  - Phone settings: lock focus and exposure (auto settings cause between-frame drift that SfM handles poorly).
  - Motion: orbit at constant radius with ~50–70% between-frame overlap. Cover top, sides, and (if possible) bottom.
  - Suggested reference objects — pick ~3 per difficulty tier:
    - **Easy (textured, rigid, small):** 3D-printed cube with published STL, patterned coffee mug, textbook, Rubik's cube.
    - **Medium (larger or lower-texture):** a chair, a plant in a pot, a printed calibration board on a stand.
    - **Hard (challenging for SfM):** shiny/reflective objects, glass, uniform-color surfaces, room-scale scenes with a laser-measured floor plan.
  - Consent/privacy: no captures with identifiable people or private spaces unless explicit consent is documented.
