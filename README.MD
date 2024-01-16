# Lane Detection Algorithm for Self-Driving Cars

## Overview

This repository implements a Lane Detection Algorithm for Self-Driving Cars, combining the power of YOLOv8 for object detection and TwinLiteNet for lane detection.

## Features

- **Object Detection:** Utilizes YOLOv8 for accurate and real-time object detection.
- **Lane Detection:** Integrates TwinLiteNet for lane detection in various driving scenarios.

## Dependencies

- [YOLOv8](https://docs.ultralytics.com/)
- [TwinLiteNet](https://github.com/chequanghuy/TwinLiteNet)
- OpenCV
- Python 3.X

## Installation & Usage

1. Download the IPYNB file.

2. Connect it to your Google Drive:

```bash
from google.colab import drive
drive.mount('/content/drive')
```

3. Edit dataset file path in Yolo Object Detection and Lane Detection
```bash
//Yolo Object Detection
videos_directory = "/content/drive/path/to/your/datasets"

//Lane Detection
path = (f"/content/drive/path/to/your/datasets/runs/detect/all_predictions/predict/{video_file}")
path = (f"/content/drive/path/to/your/datasets/runs/detect/all_predictions/predict{counter}/{video_file}")
out = cv2.VideoWriter(f"/content/drive/path/to/output/directory/{video_file}",cv2.VideoWriter_fourcc('M','J','P','G'), 30, (frame_width,frame_height))

//It is imperative only to modify "/path/to/your/datasets/" and "/path/to/output/directory/"
```

4. Runtime -> Run all.

## Acknowledgments

- [YOLOv8](https://docs.ultralytics.com/)
- [TwinLiteNet](https://github.com/chequanghuy/TwinLiteNet)
- OpenCV
- Python 3.X

## Issues
- The current version only works with specific road layouts, where the separator of a 2-way road should be yellow. Otherwise, the model will detect roads in the opposite way as drivable roads.

Feel free to raise issues or contribute to the project by creating pull requests.
