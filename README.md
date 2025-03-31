<!-- 
All credit goes to Ola Alstad (https://github.com/olaals/end-to-end-RGB-pose-estimation-baseline) 
for creating the framework. This GitHub contains changes that are tailored for my master thesis.
-->

> **Disclaimer**: All credit goes to [Ola Alstad](https://github.com/olaals/end-to-end-RGB-pose-estimation-baseline) for creating the original framework.  
> This repository includes modifications that are tailored specifically for my master's thesis.

# A Baseline for End-to-End RGB Render-and-Compare Pose Estimation

![Training Inference Process](docs/example.png "Training inference process")

This repository implements a render-and-compare machine learning pipeline for 6D pose estimation using only RGB input and a known CAD model — no depth measurements required.

A neural network compares a real image and a rendered image of an object under an initial pose estimate. It then iteratively predicts pose updates until the rendered object matches the real image.

---

### Based on the work from DeepIM and CosyPose:

- **DeepIM**: [arXiv:1804.00175](https://arxiv.org/abs/1804.00175)  
- **CosyPose**: [arXiv:2008.08465](https://arxiv.org/abs/2008.08465)  
  GitHub: https://github.com/ylabbe/cosypose

Snippets of code have been reused from the CosyPose GitHub repository. All copied functions include comments attributing their source.

---

# Pre-requisites

## 1. Install Dependencies

1. Install PyTorch with CUDA from [pytorch.org](https://pytorch.org/get-started/locally/)
2. Install remaining dependencies:
   ```bash
   pip install -r requirements.txt
