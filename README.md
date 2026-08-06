# HSegFormer

Official implementation of **HSegFormer**, a hybrid CNN–Transformer framework for brain tumor segmentation in contrast-enhanced T1-weighted magnetic resonance imaging (MRI).

---

## Overview

HSegFormer+ is a hybrid semantic segmentation framework designed for automatic brain tumor segmentation from contrast-enhanced T1-weighted MRI. The proposed architecture combines convolutional neural networks and hierarchical vision transformers to jointly exploit local spatial representations and global contextual information.

The network consists of:

- Hybrid CNN–Transformer encoder
- Multi-scale CNN–Transformer feature fusion
- Normalization Attention Block (NABlock)
- Attention-guided decoder
- Atrous Spatial Pyramid Pooling (ASPP)
- Deep supervision during training

---

## Architecture

### Overall HSegFormer Architecture

<p align="center">
<img src="docs/Proposed.png" width="1000">
</p>

The proposed architecture consists of a dual-path hybrid encoder based on **ResNet-50** and **SegFormer**, followed by multi-scale feature fusion, an attention-guided decoder, ASPP refinement, and a binary segmentation head.

---

### Normalization Attention Block (NABlock)

<p align="center">
<img src="docs/NBock.png" width="700">
</p>

The NABlock combines depthwise separable convolution, Group Normalization, GELU activation, and a Squeeze-and-Excitation (SE) module for lightweight feature refinement and channel-wise attention.

---

### Attention Gate (At-G)

<p align="center">
<img src="docs/At_G.png" width="750">
</p>

The Attention Gate suppresses irrelevant encoder features using decoder guidance before skip connections are fused within the decoder.

---

## Repository Structure

```text
HSegFormer/
│
├── README.md
│
├── docs/
│   ├── Proposed.png
│   ├── NBlock.png
│   └── At_G.png
│
└── models/
    └── hsegformer_architecture.py
```

---

## Model Components

The implementation includes:

- Hybrid CNN–Transformer encoder
- Feature projection and multi-scale fusion
- Normalization Attention Block (NABlock)
- Attention Gate (At-G)
- ASPP module
- Attention-guided decoder
- Deep supervision outputs

---

## Paper

**HSegFormer: A Hybrid CNN–Transformer Framework for Brain Tumor Segmentation in Contrast-Enhanced T1-Weighted MRI**

*Citation information will be added after publication.*

---

## Repository Status

This repository currently provides the implementation of the HSegFormer+ architecture described in the accompanying manuscript.

Additional resources may be added in future updates.

---

## Contact

For questions regarding the implementation, please open a GitHub Issue.
