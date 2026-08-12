# Build a stub pipeline end-to-end

Every stage returns fake-but-plausibly-shaped data: a stub camera returns a canned test image, a stub IQA gate always passes, a stub detector returns a fixed detection, a stub pose lookup returns a hardcoded pose, and the MQTT publisher is real (against a local `mosquitto` broker in Docker).

- **Upstream/downstream:** No external teammates blocked. Real MQTT publisher validates the message-schema contract with Cloud before their broker is ready.
- **Definition of done:** `python -m robogreeno_detection` runs a full loop against a local `mosquitto` broker and publishes valid JSON messages matching the agreed schema. `mosquitto_sub` from another terminal receives them.
- **Demo:** Start `mosquitto` in Docker, run the pipeline, show subscribed messages appearing in a second terminal.
- **Subtasks:**
  - Canned test frame in `tests/fixtures/`.
  - Stub for each of: capture, IQA gate, detector, pose lookup.
  - Real MQTT publisher using `paho-mqtt`, schema-validated with `jsonschema`.
  - `docker-compose.yml` for local `mosquitto`.
