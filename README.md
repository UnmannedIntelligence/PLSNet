# UAV-Based Damage Detection in Overhead Power Lines from Aerial Imagery

### Repository Overview

This repository provides the experimental resources for our manuscript submitted to *IEEE Transactions on Industrial Electronics *. It contains source code, experimental data, and UAV flight videos for detecting damage in overhead transmission lines from aerial images.

⚠️ **Note:** At present, only experimental/demo videos are available. The source code, trained weights (PLSNet & GAN-based detector), and the Power Line Damage Dataset (PLDD) will be uploaded after the manuscript is accepted.

## Abstract

Unmanned aerial vehicles (UAVs) enable flexible and safe inspection of overhead transmission lines, but detecting line damage from aerial images remains challenging due to slender targets, class imbalance, and real-time constraints.

In this study, we propose a two-stage, UAV-deployable approach:

* **Lightweight power-line segmentation (PLSNet):** An enhanced U-Net with multi-branch downsampling fusion, multi-scale feature fusion, and attention. It reduces layers/channels while preserving accuracy, reaching **95.55% mIoU** and **87 FPS** on PLD500, and **74.61% mIoU / 85.46% F1** on PLD-UAV.
* **GAN-based damage detection:** An encoder–decoder reconstruction network (GANomaly-style) that identifies defects via reconstruction loss and a defect discriminator. Using small kernels and fewer channels, it achieves high-speed inference and **99.09% accuracy** on our PLDD dataset.
* **New damage dataset (PLDD):** 440 images (220 normal / 220 damaged) collected with a DJI M300 UAV and online supplementation, covering artificially induced and naturally occurring defects.
* **Embedded deployment:** Implemented on NVIDIA Jetson Xavier NX with TensorRT; the complete onboard system runs at **\~9 FPS** during outdoor flight tests and is validated in two real-world environments using a DJI M300 UAV.

These results demonstrate both high accuracy and practical real-time performance, facilitating UAV-based grid inspection in the field.

## Citation

If you find this repository useful in your research, please cite our paper once it is published in *IEEE Transactions on Power Delivery*:

```text
@article{IEEE2025_Zhang_UAVLineDamage,
  author  = {Yulong Zhang, Xianghong Xue, Jing Xin, Lingxia Mu and Youmin Zhang},
  title   = {UAV-Based Damage Detection in Overhead Power Lines from Aerial Imagery},
  journal = {IEEE Transactions on Industrial Electronics},
  year    = {2026},
  volume  = {...},
  number  = {...},
  pages   = {...},
  doi     = {...}
}
```

## Contact

For questions or collaborations, please contact:

**Yulong Zhang** · [yulong.zhang@stu.xaut.edu.cn](mailto:yulong.zhang@stu.xaut.edu.cn)
