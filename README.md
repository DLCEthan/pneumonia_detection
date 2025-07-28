# Pneumonia Detection from Chest X-rays (RSNA Challenge)

This project aims to detect pneumonia in chest X-ray images using a two-stage deep learning pipeline combining classification and object detection. It follows the evaluation methodology of the RSNA Pneumonia Detection Challenge and demonstrates strong performance in identifying and localizing pneumonia-affected regions.
# Project Overview

The pipeline is designed to:

Classify chest X-rays as Normal or Pneumonia.

Detect and localize pneumonia regions using bounding boxes for enhanced clinical interpretability.

Our goal is to provide an assistive tool that can aid radiologists by flagging suspicious cases and visualizing potentially affected regions.
# Model Architecture

Stage 1 – Classification:
An ensemble of convolutional neural networks (e.g., EfficientNet, ResNet) determines whether the image shows signs of pneumonia.

Stage 2 – Detection:
If pneumonia is detected, a RetinaNet model localizes the pneumonia regions via bounding boxes.
## Results

- Accuracy: 88%

- Recall: 81%

- mAP (test set): 0.21464

        This would rank 24th out of ~340 participants in the original Challenge leaderboard.

## Dataset

RSNA Pneumonia Detection Challenge Dataset

~26,000 chest X-ray images

## Evaluation

- Multi-threshold mean Average Precision (mAP) computed using IoU thresholds from 0.4 to 0.75

## Tech Stack

Python, PyTorch

torchvision,


Google Colab

## Clinical Relevance

This project provides a proof-of-concept for automated pneumonia screening in radiographs. While not a diagnostic tool, it can assist physicians by highlighting high-risk cases and drawing attention to suspicious lung regions.
## Limitations

    Trained on a publicly available dataset with potential labeling inconsistencies

    Not validated on external or clinical datasets

## Note

Due to privacy constraints, the original RSNA test set lacks annotations. Our final evaluation was performed on a held-out internal test set simulating the official challenge conditions.
## License

This project is intended for educational and research use only.
