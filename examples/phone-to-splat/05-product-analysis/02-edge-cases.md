# Integration and edge-case tests

What happens with: a very short video (10 frames)? A video with the phone held still (no parallax)? A corrupt input file? A texture-poor object? An object the size of a room? A scene captured indoors under fluorescent flicker? The pipeline should degrade gracefully — never crash silently, always report clearly.

- **Upstream/downstream:** Deployment (Cards 06-deployment/02, 06-deployment/03) needs to know the failure modes. Documentation captures them.
- **Definition of done:** `tests/edge_cases/` covers each named case. Pipeline either handles gracefully (produces output + warning) or fails with a clear log message and non-zero exit. No silent hangs.
- **Demo:** Trigger 2–3 edge cases live; show either graceful handling or clear failure.
- **Subtasks:**
  - Insufficient input: very short video, still camera, occluded object.
  - Corrupt input: broken video file, unsupported codec, empty file.
  - Scale mismatch: object too small (< 100 px) or too large (fills frame).
  - Environmental: fluorescent flicker (rolling shutter interaction), moving subject mid-capture, changing lighting.
  - Reference the failure-mode analysis from 04-model-analysis/03 — many of those become edge-case tests here.
