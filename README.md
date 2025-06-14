# YOLOv8 Object Detection on COCO128

## Overview

This project demonstrates object detection using YOLOv8, trained and evaluated on the COCO128 dataset. The objective is to quickly build and test a practical object detection model for a hackathon setting.

---

## Why YOLOv8?

YOLOv8 is a recent object detection model that can identify and locate multiple objects in an image. It is suitable for tasks where you need to both classify and localize objects rather than just assigning a single label to an image. Compared to simple CNNs or models designed for datasets like MNIST (which only classify a single digit per image), YOLOv8 is designed for more complex, real-world scenes.

---

## What is COCO?

COCO (Common Objects in Context) is a widely-used dataset for computer vision. It contains real-world images with multiple labeled objects per image and is a standard benchmark for object detection models.

We use the smaller COCO128 version for faster training and demonstration.

---

## Project Structure

- `yolov8_coco128_training.py` — Training, evaluation, and inference script.
- `requirements.txt` — Dependencies.
- `runs/` — Output directory for results.
- `docs/` — (Optional) Reports and analysis.

---

## Getting Started

1. **Install Dependencies**

    ```bash
    pip install ultralytics
    ```

2. **Train and Evaluate**

    ```bash
    python yolov8_coco128_training.py
    ```

    The script will:
    - Download COCO128 if needed
    - Train YOLOv8 for 10 epochs
    - Evaluate the model
    - Run inference on sample images
    - Save results under `runs/`

---

## Model Architecture

YOLOv8 uses a convolutional neural network backbone with detection heads for object localization and classification. It is designed to balance speed and accuracy for object detection tasks.

---

## Evaluation Results

After training for 10 epochs on COCO128, typical results are as follows (actual values may vary):

| Metric        | Value (example) |
|---------------|----------------|
| mAP@0.5       | 0.691           |
| mAP@0.5:0.95  | 0.5264           |
| Precision     | 0.683           |
| Recall        | 0.623           |

- **IoU (Intersection over Union):** Reflected in mAP scores.
- **Confusion Matrix:** Saved in the output directory.

*Metrics like SSIM, PSNR, and MSE are generally used for image quality, not standard for object detection, so they are not reported here.*

---

## Optimization Techniques

  - Used the lightweight YOLOv8n for speed.
  - Trained for fewer epochs (10) for quick turnaround.
  - Applied confidence threshold of 0.25 for detection.
  - Exported ONNX model for future deployment.
---

## Results

Detection outputs and evaluation metrics are saved in the `runs/` directory for review.

---

## Team & Hackathon Details

- **Hackathon:** [Object Detection with YOLOv8 on COCO128 Dataset]
- **Member:** [Noel Dominic]
- **Submission Date:** [09-06-2025]

---



---

## Acknowledgments

- [Ultralytics YOLO](https://github.com/ultralytics/ultralytics)
- [COCO Dataset](https://cocodataset.org/)
