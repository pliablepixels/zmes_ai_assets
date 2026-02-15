These are model/weights for the ZMES ML Ecosystem. The install script of ES uses these links during install

## Converting .pt to .onnx

Requires the `ultralytics` package (`pip install ultralytics`). Then use the `yolo` CLI:

```bash
yolo export model=path/to/model.pt format=onnx
```

For example:

```bash
yolo export model=models/ultralytics/yolo26n.pt format=onnx
```

This will produce a `.onnx` file alongside the original `.pt` file.

If the `.pt` file doesn't exist locally, the `yolo` CLI will automatically download it from Ultralytics before exporting. For example:

```bash
yolo export model=yolo11x.pt format=onnx
```

This will download `yolo11x.pt` and then export it to `.onnx` in one step.
