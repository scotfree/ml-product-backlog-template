# Survey candidates and pick a baseline

Compare small-detector options: YOLO11n, YOLO11s, RF-DETR-base, YOLOX-s. Confirm license posture with the organizer before committing to Ultralytics (AGPL). Baseline is YOLO11n if AGPL is fine, RF-DETR-base if not.

- **Upstream/downstream:** Deployment (Cards 06-deployment/*) needs to know model size and export format. The AGPL decision propagates to AgCloud's license posture (Kayvan).
- **Definition of done:** `docs/model-survey.md` with 4 candidates, params/size/license, and a paragraph justifying the baseline pick. Organizer's AGPL decision recorded.
- **Demo:** Explain top two candidates and why the winner won.
- **Subtasks:**
  - Confirm each candidate has ONNX export path (needed for Sprint 3 Pi deployment).
  - Confirm YOLO11n fine-tunes in reasonable time on the strongest team laptop.
  - Wait for organizer's AGPL confirmation before committing framework choice.
