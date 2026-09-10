# Unmanned Aerial Vehicle-Based Damage Detection in Overhead Power Lines from Aerial Imagery

## Overview

This repository accompanies a manuscript prepared for submission to *Engineering Applications of Artificial Intelligence* (EAAI). The work investigates an artificial-intelligence-based system for detecting damage to overhead power lines from aerial imagery acquired by unmanned aerial vehicles (UAVs).

The proposed system combines lightweight semantic segmentation, reconstruction-based anomaly detection, and onboard deployment to support practical power-line inspection.

## Manuscript Status

The manuscript is currently being prepared for submission to EAAI.

During the submission and peer-review stage, this repository provides selected demonstration materials. The following research materials are planned for public release after acceptance:

- Source code and trained models for PLSNet
- Source code and trained models for the damage-detection network
- Training, evaluation, and deployment scripts
- The Power Line Damage Dataset (PLDD) and its documentation
- Configuration files and instructions for reproducing the reported experiments

## Method Overview

The proposed framework contains two main stages.

### 1. Power-line segmentation

PLSNet is a lightweight semantic-segmentation network designed to extract thin power-line structures from complex aerial backgrounds. It incorporates:

- Multi-branch downsampling and feature fusion to reduce information loss
- Multi-scale feature aggregation for improved contextual representation
- Attention-based feature refinement
- A lightweight architecture for real-time onboard inference

### 2. Power-line damage detection

The segmented power lines are processed by a Generative Adversarial Network (GAN)-based reconstruction model. The method learns the distribution of normal power-line appearances and identifies potential damage using reconstruction inconsistencies and latent-representation differences.

## Datasets

The method is evaluated using the following datasets:

- **PLD500:** a public dataset used to evaluate power-line segmentation
- **PLD-UAV:** a public UAV-image dataset used to evaluate segmentation performance under diverse backgrounds
- **PLDD:** the Power Line Damage Dataset constructed for this study

PLDD contains 440 balanced samples:

- 220 damaged power-line samples
- 220 normal power-line samples

The damaged samples include artificially induced conductor defects collected under controlled conditions using a DJI M300 UAV platform. PLDD is planned for public release after acceptance of the manuscript.

## Deployment and Outdoor Validation

The complete system is deployed on an iCrest onboard computer equipped with an NVIDIA Jetson Xavier NX. The implementation uses TensorRT for inference acceleration and is integrated with a DJI M300 UAV and an H20T camera.

Outdoor experiments were conducted in residential and roadside environments to evaluate the practical applicability of the proposed method under different backgrounds and illumination conditions.

## Main Results

The manuscript reports:

- Competitive segmentation performance on the PLD500 and PLD-UAV datasets
- An F1-score of 97.74% and an inference speed of 87 FPS on PLD500
- An F1-score of 85.46% and an inference speed of 87 FPS on PLD-UAV
- A damage-classification accuracy of 99.09% on PLDD
- End-to-end operation at approximately 12 FPS on the embedded platform
- Outdoor validation in representative UAV inspection scenarios

For the complete experimental settings, evaluation protocols, and comparisons, please refer to the manuscript.

## Citation

Please cite the final published article once its bibliographic information becomes available. Until publication, use the following manuscript-level entry only when a citation is necessary:

```bibtex
@unpublished{Zhang2026UAVDamageDetection,
  author = {Yulong Zhang and Xianghong Xue and Jing Xin and Lingxia Mu and Youmin Zhang},
  title  = {Unmanned Aerial Vehicle-Based Damage Detection in Overhead Power Lines from Aerial Imagery},
  note   = {Manuscript prepared for submission to Engineering Applications of Artificial Intelligence},
  year   = {2026}
}
```

The citation entry will be replaced with the final journal metadata, DOI, volume, and article number after publication.

## Release Notice

The repository is under active preparation. File organization, documentation, and interfaces may change before the complete research package is released.
