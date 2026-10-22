# Gloved vs. Ungloved Hand Detection

A YOLOv8 computer-vision project that detects whether a visible hand is gloved or ungloved.

## Classes

- `gloved_hand`
- `ungloved_hand`

## Model and dataset

- Framework: Ultralytics YOLOv8
- Model family: YOLOv8n
- Input size: 640 × 640
- Dataset source: [Roboflow Universe](https://universe.roboflow.com/glove-uylxg/glove-q7czq/dataset/1)

The repository includes training artifacts, a notebook, dataset directories, and submission outputs. Inspect the notebook and model folder for the exact experiment configuration.

## Run inference

Install the project dependencies and provide a trained weights file and image directory to the inference workflow:

```bash
pip install ultralytics opencv-python numpy matplotlib
```

Use the trained weights under `glove_model3/weights/` when running the notebook or inference script available in the repository.

## Limitations

Performance depends on camera angle, occlusion, glove appearance, and the training distribution. Treat this as an educational detection project, not a safety certification system.
