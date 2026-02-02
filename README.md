# HAMC: Hyperbolic Asymmetric Multi-view Clustering

[![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=flat-square&logo=PyTorch&logoColor=white)](https://pytorch.org/)

This repository contains the PyTorch implementation for **Hyperbolic Asymmetric Multi-view Clustering (HAMC)**.
## Requirements

The code is implemented in Python 3.10+ and PyTorch 2.9+.

Install the required dependencies:

```bash
pip install torch torchvision numpy scipy scikit-learn munkres
```
## Data Preparation

Place your dataset files (`.mat` format) in the `./Data/` directory. The current `utils.py` supports the following datasets:
* **Dual-view**: `CUB`, `BDGP`, `Animal`, `Wiki`, `Reuters`, `Scene15`, `Caltech101`, `NoisyMNIST`, `MNIST-USPS`.
* **Multi-view**: `100Leaves`, `LandUse21` (3 views); `YoutubeFace`, `ALOI100` (4 views).

## Directory Structure Example
```text
.
├── Data/
│   ├── CUB.mat
│   └── ...
├── SaveWeight/      # Training weights are automatically saved here
├── main.py          # Main entry point for training and inference
├── model.py         # HAMC network architecture and hyperbolic utilities
└── utils.py         # Data loading and evaluation metrics
