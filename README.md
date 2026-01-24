# UAV-Based Damage Detection in Overhead Power Lines from Aerial Imagery

## Repository Overview

This repository hosts experimental resources for our manuscript submitted to **IEEE Transactions on Industrial Electronics (IEEE TIE)**. The work focuses on UAV-based damage detection for overhead power lines using aerial imagery. The repository will be updated to support reproducibility.

⚠️ **Availability Notice (Under Review):**  
At this stage, only **experimental and demo videos** are available. The following materials will be released **after the manuscript is accepted**:
- Source code for **PLSNet** and the **GAN-based damage detector**
- Trained weights and deployment scripts
- The **Power Line Damage Dataset (PLDD)** and accompanying documentation

---

## Method Summary

We propose a UAV-deployable, two-stage pipeline.

- **Power-line segmentation (PLSNet)**  
  A lightweight U-Net-based segmentation network with multi-branch downsampling fusion and multi-scale feature fusion. It is designed for thin-structure extraction under complex backgrounds while maintaining high inference efficiency.

- **Damage detection via GAN-based reconstruction**  
  A GANomaly-style encoder-decoder reconstruction network that identifies damage by combining reconstruction inconsistency and discriminator response. The network is streamlined using small convolution kernels and fewer feature channels for embedded inference.

- **PLDD dataset**  
  A balanced dataset containing **440 images** (**220 normal** and **220 damaged**) collected using a **DJI M300 UAV**, including **artificially induced damage samples** for systematic evaluation.

- **Embedded deployment**  
  The complete pipeline is deployed on an **NVIDIA Jetson Xavier NX** with TensorRT acceleration and validated through outdoor UAV flight tests in real inspection environments.

---

## Results Snapshot

Representative results reported in the manuscript include:
- **Segmentation performance** evaluated on **PLD500** and **PLD-UAV** using mIoU and related metrics
- **Damage detection performance** evaluated on **PLDD** with **99.09% classification accuracy**
- **Real-world validation** via outdoor UAV flight tests using a **DJI M300** platform

> Note: runtime depends on deployment settings and pipeline configuration. The final release will include benchmarking scripts and environment specifications.



## Citation

If you use this repository in your research, please cite our paper after it is published. Final publication metadata will be updated here.

```text
@article{Zhang2026_UAVLineDamage,
  author  = {Yulong Zhang and Xianghong Xue and Jing Xin and Lingxia Mu and Yichi Yang and Youmin Zhang},
  title   = {UAV-Based Damage Detection in Overhead Power Lines from Aerial Imagery},
  journal = {IEEE Transactions on Industrial Electronics},
  year    = {2026},
  volume  = {},
  number  = {},
  pages   = {},
  doi     = {}
}
