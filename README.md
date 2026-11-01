# Vision Transformer Models for Pathology Slide Classification

A comparative deep learning study of Vision Transformer and CNN-based architectures for **colorectal cancer histopathology image classification**, including Grad-CAM visualizations for model interpretability.

## Overview

This research evaluates five pretrained deep learning architectures for classifying colon tissue images. It compares transformer-based, hybrid, and convolutional approaches using classification metrics, confusion matrices, and Grad-CAM explanations. Experiments were developed and executed in **Kaggle notebooks** using PyTorch.

## Models

| Model | GitHub Notebook | Run on Kaggle |
|---|---|---|
| Vision Transformer (ViT-Base) | [View Code](vit-base.ipynb) | [Open Kaggle](https://www.kaggle.com/code/iftekharislam/cse438-project-vit-base) |
| EfficientViT-B0 | [View Code](efficient-vit.ipynb) | [Open Kaggle](https://www.kaggle.com/code/iftekharislam/cse438-project-efficient-vit) |
| EfficientNet-B0 | [View Code](efficientnetb0.ipynb) | [Open Kaggle](https://www.kaggle.com/code/iftekharislam/cse438-project-efficientnetb0) |
| ConViT | [View Code](convit.ipynb) | [Open Kaggle](https://www.kaggle.com/code/iftekharislam/cse438-convit) |
| Swin Transformer | [View Code](swint.ipynb) | [Open Kaggle](https://www.kaggle.com/code/iftekharislam/swint) |
## Datasets

- **NCT-CRC-HE-100K:** Nine colorectal tissue classes.
- **CRC-VAL-HE-7K:** Independent colorectal tissue evaluation dataset with nine classes.
- **LC25000 (colon subset):** Binary colon adenocarcinoma versus normal tissue classification.

Dataset preparation, sampling, and evaluation settings differ by model; see the paper and individual notebooks for details. Dataset files are not included in this repository.

## Results

The following accuracies are reported in the research paper's comparison table for **CRC-VAL-HE-7K**:

| Model | Reported accuracy |
|---|---:|
| ViT-Base | 93.68% |
| EfficientViT-B0 | 92.00% |
| EfficientNet-B0 | 94.62% |
| ConViT | 88.52% |
| **Swin Transformer** | **96.25%** |

**Note:** The manuscript contains some differences between its narrative and tabulated metrics. The values above reproduce its final comparison table; refer to the notebooks for experiment-specific outputs. These are research results, not evidence of clinical readiness.

## Methods and Evaluation

- Pretrained models with task-specific classification heads
- Image resizing, normalization, and data augmentation
- Sampling strategies to address class imbalance
- Training and validation using PyTorch
- Accuracy, precision, recall, F1-score, and confusion matrices
- Grad-CAM visualizations for interpreting model predictions

## Run the Notebooks

1. Open [Kaggle Code](https://www.kaggle.com/code) and create a notebook or import one of the `.ipynb` files from this repository.
2. Enable a GPU accelerator where available.
3. Attach the relevant dataset(s) and update any `/kaggle/input/` paths as needed.
4. Install packages required by the selected notebook and execute its cells in order.

**Main libraries:** `torch`, `torchvision`, `timm`, `transformers`, `scikit-learn`, `numpy`, `pandas`, `matplotlib`, `seaborn`, `opencv-python`, `grad-cam`, and `kagglehub` (requirements vary by notebook).

> The notebooks were originally developed on Kaggle. They may contain environment-specific paths, package-install commands, or dataset access steps that require adjustment. Do not commit Kaggle API credentials or private datasets.

## Research Paper

**Title:** *Vision Transformer Models for Pathology Slide Classification*

**Authors:** Faiza Chowdhury, Iftekharul Islam Ifti, Md. Rashedur Rahman Tanvir, Dr. Ahmed Wasif Reza, K. M. Safin Kamal, and Md. Adnan Morshed.

**Affiliation:** Department of Computer Science and Engineering, East West University, Dhaka, Bangladesh.

[Read the research manuscript](Vision%20Transformer%20Models%20for%20Pathology%20Slide%20Classification%20%281%29.pdf)

*The supplied manuscript does not establish a confirmed publication DOI or publication status; please update this section when those details are available.*

## Research Use

This repository is intended for research and educational purposes only. The models are not validated clinical diagnostic tools. Dataset and pretrained model usage remains subject to their respective licenses.
