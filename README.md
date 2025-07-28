# CO2.2-Final-Project-RF-DETR-for-Object-Detection

# RF-DETR for Person Detection

This project implements **RF-DETR (Receptive Field Enhanced Detection Transformer)** for person detection tasks using the [People Detection dataset](https://universe.roboflow.com/prism-zhxxq/people-4wxxx) from Roboflow. The implementation, experimentation, and results are consolidated in a single Jupyter notebook: `project.ipynb`.

## Overview

RF-DETR is an improvement of DETR (DEtection TRansformer), designed to handle small objects and complex scenes better by using **Receptive Field Enhancement (RFE)** modules. This project demonstrates:

- Deployment and training of RF-DETR on a custom dataset.
- Performance evaluation using mAP, precision, recall.
- Visualization of predictions and training behavior.
- Analysis of training stability and generalization.

## Files

- `project.ipynb`: Main notebook containing data preprocessing, model training, evaluation, visualizations, and discussion.
- Dataset: [People Detection by Roboflow](https://universe.roboflow.com/prism-zhxxq/people-4wxxx) (in COCO JSON format).
- Pretrained weights and evaluation outputs (optional): available via GitHub repo.

## Setup Instructions

1. **Clone this repository**:
   ```bash
   git clone https://github.com/BenitoUy/CO2.2-Final-Project-RF-DETR-for-Object-Detection-.git
   cd CO2.2-Final-Project-RF-DETR-for-Object-Detection-
   ```

2. **Install Dependencies**:
   Use Python ≥3.8 and install the following:
   ```bash
   pip install -r requirements.txt
   ```
   *(You may need to manually install the Roboflow RF-DETR package or follow instructions on [Roboflow’s documentation](https://blog.roboflow.com/rf-detr/))*

3. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

4. **Open and Run**: Open `project.ipynb` and run all cells sequentially.

## Results Summary

| Trial | Epochs | LR     | mAP@0.5 | Precision | Recall |
|-------|--------|--------|---------|-----------|--------|
| 1     | 10     | 1e-4   | 0.9704  | 0.9438    | 0.9100 |
| 2     | 20     | 3e-4   | 0.9749  | 0.9319    | 0.9400 |

- **Trial 1** was more stable and generalizable.
- **Trial 2** showed higher recall but increased overfitting risk.

## Example Inference

Sample frames from test videos demonstrate successful detection of people in indoor and outdoor scenes, even under occlusion and poor lighting.

## Limitations

- High computational cost and memory usage (especially for high-res or long training runs).
- Sensitive to learning rate and prone to overfitting beyond 10–12 epochs.

## Future Work

- Explore hybrid backbones or lightweight variants for real-time inference.
- Integrate data augmentation and multi-class detection.
- Optimize training for larger datasets and longer epochs.

## Project Links

- **Full Project Notebook**: `project.ipynb`
- **GitHub Repo**: [CO2.2 Final Project - RF-DETR](https://github.com/BenitoUy/CO2.2-Final-Project-RF-DETR-for-Object-Detection-)
- **Dataset**: [People Detection Dataset on Roboflow](https://universe.roboflow.com/prism-zhxxq/people-4wxxx)
- **References**: See full reference list in `project.ipynb`
