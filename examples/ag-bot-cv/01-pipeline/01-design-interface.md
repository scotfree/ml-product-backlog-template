# Design the pipeline interface

Sketch the five stages (capture → IQA gate → detector → pose enrichment → MQTT publish) and the type each hands to the next. Confirm the external contracts with Embedded (frame pull API), Data A (freshest-pose API), and Cloud (MQTT topic + message schema).

- **Upstream/downstream:** Embedded (Pavan) provides `cv2.VideoCapture(0).read()` returning `(ok, frame_ndarray, frame_stamp_ms)`. Data A (Ingyu) provides synchronous `get_freshest_pose()` returning `(pose_dict, pose_stamp_ms)`. Cloud (Kayvan) accepts JSON on `robogreeno/detections/<robot_id>/<task>` at QoS 1.
- **Definition of done:** A one-page `docs/pipeline.md` with a diagram of the five stages, the type signature at each boundary, and links to the confirmed external contracts (Pavan / Ingyu / Kayvan replies).
- **Demo:** Walk the team through the diagram in 2 minutes; specifically point out where a stub can sit at each stage.
- **Subtasks:**
  - Confirm frame format with Embedded (ndarray shape, dtype, color order).
  - Confirm pose schema with Data A (fields, coordinate frame, units, stamp format).
  - Confirm MQTT topic hierarchy, QoS, and message JSON schema with Cloud.
  - Mark every boundary as "stubbable" so Card 2 can proceed independently.
