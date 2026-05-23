# Adaptive Feature Fusion of ResNet50 and Vision Transformer for Robust Agricultural Pest Classification

## Overview

This repository contains the implementation of the proposed Adaptive Feature Fusion Network (AFFN) for agricultural pest classification.

The proposed framework combines:

* ResNet50
* Vision Transformer (ViT)
* Temperature-regulated adaptive feature fusion

to improve fine-grained agricultural pest classification performance.

---

## Repository Structure

```text
AFFN-Agricultural-Pest-Classification/
│
├── notebooks/
├── figures/
├── sample_results/
├── README.md
└── requirements.txt
```

---

## Included Notebooks

| Notebook                     | Description                                  |
| ---------------------------- | -------------------------------------------- |
| 01_resnet50_baseline.ipynb   | ResNet50 baseline model                      |
| 02_vit_baseline.ipynb        | Vision Transformer baseline                  |
| 03_static_fusion.ipynb       | ResNet50 + ViT without adaptive fusion       |
| 04_affn_final_tau_2_0.ipynb  | Proposed AFFN model with adaptive fusion     |
| 05_temperature_tau_0_5.ipynb | Temperature sensitivity experiment (τ = 0.5) |
| 06_temperature_tau_1_0.ipynb | Temperature sensitivity experiment (τ = 1.0) |
| 07_temperature_tau_1_5.ipynb | Temperature sensitivity experiment (τ = 1.5) |
| 08_ip102_experiment.ipynb    | Evaluation on IP102 dataset                  |

---

## Key Features

* Hybrid CNN + Vision Transformer architecture
* Adaptive feature fusion mechanism
* Temperature-regulated gating strategy
* CLAHE preprocessing
* Fine-grained agricultural pest classification
* Evaluation on Agricultural Pest Dataset and IP102 Dataset

---

## Temperature-Regulated Gating Mechanism

The proposed AFFN dynamically balances CNN and Transformer feature contributions using a learnable adaptive fusion mechanism.

The final reported model uses:

```python
temperature = 2.0
```

Additional experiments with:

* τ = 0.5
* τ = 1.0
* τ = 1.5

are included to support reproducibility and sensitivity analysis.

---

## Datasets

### Agricultural Pest Dataset

https://www.kaggle.com/datasets/vencerlanz09/agricultural-pests-image-dataset

### IP102 Dataset

https://github.com/xpwu95/IP102

---

## Experimental Environment

* Python 3.10+
* PyTorch
* Torchvision
* CUDA-enabled GPU
* Kaggle GPU Environment

---

## Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
```

---

## Reproducibility

All experiments were originally executed using Kaggle notebooks.

The repository contains:

* baseline implementations
* adaptive fusion implementation
* temperature sensitivity experiments
* IP102 evaluation experiments

to improve reproducibility and transparency of the proposed framework.

---

## Citation

If you use this work, please cite the corresponding research paper.

---

## Contact

For academic queries related to this work, please contact the corresponding authors.
