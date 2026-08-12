# Benchmark in the target environment

## Description

Measure inference latency, memory, and end-to-end frame-to-publish time on Pi 3B CPU. Compare three runtimes: NCNN (expected fastest on ARM CPU), ONNX Runtime, TFLite+XNNPACK. Also compare INT8-quantized vs. FP32 models. Recommend a runtime for production.

## Upstream / Downstream contract

- Model analysis and documentation both consume the numbers.
- Feedback loop to Modeling: if nothing hits latency budget, we may need a smaller model.

## Definition of Done

`reports/pi-benchmarks.md`: table of (task × runtime × precision) with latency (p50, p95), peak memory, and any failures. Explicit recommendation: "Use runtime X for task Y."

## Demo

Show the benchmark table on the Pi live; point out the surprising result (usually NCNN winning on latency, ONNX Runtime winning on portability).

## Subtasks

- Export each best model to ONNX, then convert to NCNN and TFLite.
- Post-training INT8 quantization with 100–200 calibration images per task.
- Benchmark script does warm-up runs then N=100 measured runs.
- Report includes what didn't work (some export paths may fail — that's a finding, log it).

## Estimate

~3 days — the export/convert matrix is where the time goes.
