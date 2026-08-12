# Example: Ag-Bot-CV (Robo-Greeno Data Team B)

A filled-in instantiation of the template, adapted for agricultural computer vision on a hexapod robot ("Robo-Greeno"). Data Team B owns detection: fruit (tomato ripeness), pest identification (IP102 classes), and disease (leaf conditions).

This is a **reference** for what "adapted to a domain" looks like. Every card in `templates/markdown/` has been rewritten with real specifics — real datasets, real teammates, real deployment targets, real interfaces.

## Project context (abridged)

- **Team:** 4-person Data B, working under mentor Scot. Coordinating with three other teams: Embedded (Pavan, hexapod control + camera), Cloud (Kayvan, AgCloud + MQTT broker), Data A / Robotics (Ingyu, pose + IMU).
- **Deployment target:** Raspberry Pi 3B, CPU-only (no AI accelerator this phase).
- **Camera:** Pi Camera v2 via RPi camera module, pull model (`cv2.VideoCapture(0).read()`).
- **Comms out:** MQTT publish of detection JSON to a remote broker (Kayvan). QoS 1. Cold-path image archival via local MinIO → `mc mirror` to AgCloud MinIO.
- **Detection scope:** fruit → pest → disease (in order of ascending difficulty). Pest is highest priority for the greenhouse operator; fruit is the easiest first target.
- **Framework:** PyTorch training, ONNX export, runtime candidate benchmark across NCNN, ONNX Runtime, and TFLite+XNNPACK.
