
<div align="center">

# SteelDefectNet

**Robust Steel Surface Defect Classification using Deep Learning and PyTorch**

<p>
  <img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white">
  <img src="https://img.shields.io/badge/Computer%20Vision-CNN-blueviolet?style=for-the-badge">
  <img src="https://img.shields.io/badge/Dataset-NEU%20DET-success?style=for-the-badge">
</p>

[Dataset](https://www.kaggle.com/datasets/kaustubhdikshit/neu-surface-defect-database)
•
[PyTorch](https://pytorch.org/)

---

*A comprehensive study on neural network fundamentals, defect classification, model hardening, and hyperparameter optimization for real-world manufacturing environments.*

</div>

---

## Overview

Steel manufacturing requires reliable surface inspection to maintain product quality. Traditional manual inspection is:

- Time-consuming
- Expensive at scale
- Subject to human inconsistency
- Unable to consistently detect subtle defects

This project develops and evaluates deep learning models capable of automatically classifying steel surface defects while improving robustness against variations in lighting, orientation, and surface conditions.

---

## Features

### Neural Network Foundations
- Custom 2-layer neural network implementation
- ReLU vs Sigmoid comparison
- CrossEntropyLoss vs MSELoss analysis
- Optimizer benchmarking
- Training stability experiments

### Defect Classification
- CNN built entirely using `nn.Module`
- End-to-end PyTorch training pipeline
- Per-class evaluation and confusion analysis

### Model Hardening
- Data augmentation
- Batch Normalization
- Dropout regularization
- Generalization analysis

### Hyperparameter Optimization
- Grid Search
- Learning Rate Scheduling
- Bayesian Optimization with Optuna

---

## Dataset

### NEU Surface Defect Database

| Property | Value |
|-----------|--------|
| Total Images | 1,800 |
| Classes | 6 |
| Images per Class | 300 |
| Resolution | 200 × 200 |
| Image Type | Grayscale |

### Defect Categories

| Class | Description |
|-------|-------------|
| Cr | Crazing |
| In | Inclusion |
| Pa | Patches |
| PS | Pitted Surface |
| RS | Rolled-in Scale |
| Sc | Scratches |

---

## Methodology

```text
NEU Dataset
     │
     ├── Preprocessing
     │      └── Normalization
     │
     ├── Baseline CNN
     │
     ├── Model Hardening
     │      ├── Data Augmentation
     │      ├── Batch Normalization
     │      └── Dropout
     │
     ├── Hyperparameter Search
     │
     └── Final Evaluation
```

---

## Repository Structure

```text
SteelDefectNet/
│
├── NeuralNetwork.ipynb
├── ANN.ipynb
├── archive/
│   └── NEU-DET/
│
├── figures/
├── models/
├── requirements.txt
└── README.md
```

---

## Implemented Experiments

### Part 0 — Neural Network Foundations

| Experiment | Description |
|------------|-------------|
| Activation Functions | ReLU vs Sigmoid |
| Loss Functions | CrossEntropy vs MSE |
| Optimizers | SGD, Momentum, Adam |
| Stability Methods | BatchNorm / Dropout |

---

### Part A — Surface Defect Classification

- Dataset loading with `ImageFolder`
- Data preprocessing and normalization
- CNN training and validation
- Learning curve visualization
- F1-score and confusion matrix analysis

---

### Part B — Model Hardening

#### Data Augmentation
```python
RandomHorizontalFlip()
RandomRotation(15)
RandomCrop(180)
```

#### Regularization
```python
BatchNorm2d()
Dropout(0.4)
```

#### Objectives
- Improve robustness
- Reduce overfitting
- Increase deployment reliability

---

### Part C — Hyperparameter Tuning

#### Grid Search

```python
learning_rates = [0.001, 0.01]
batch_sizes = [16, 32]
```

#### Learning Rate Scheduling

```python
StepLR(
    step_size=5,
    gamma=0.5
)
```

#### Bayesian Optimization

```python
lr: 1e-4 → 1e-1
batch_size: 8 → 64
```

Implemented using **Optuna**.

---

## Technology Stack

<div align="center">

| Python | PyTorch | TorchVision | NumPy | Pandas | Matplotlib | Scikit-Learn | Optuna |
|:------:|:--------:|:------------:|:------:|:-------:|:-----------:|:------------:|:-------:|

</div>

---

## Installation

Clone the repository:

```bash
git clone https://github.com/Creative-Sandesh/SteelDefectNet.git
cd SteelDefectNet
```

Install dependencies:

```bash
pip install -r requirements.txt
```

or

```bash
pip install torch torchvision numpy pandas matplotlib scikit-learn optuna
```

---

## Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
NeuralNetwork.ipynb
```

Run all notebook cells sequentially.

---

## Evaluation Metrics

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Training Loss
- Validation Loss

---

## Future Work

- Transfer Learning (ResNet, EfficientNet)
- Grad-CAM Explainability
- Cross Validation
- Early Stopping
- Ensemble Learning
- Real-Time Defect Detection
- Deployment using FastAPI

---

## References

1. NEU Surface Defect Database
2. PyTorch Documentation
3. TorchVision Documentation
4. Optuna Documentation
5. Scikit-Learn Documentation

---

<div align="center">

**Built with PyTorch for intelligent manufacturing and computer vision research.**

⭐ Star this repository if you found it useful.

</div>
````
