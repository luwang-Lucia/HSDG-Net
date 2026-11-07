# HSDG-Net

**A Hessian-Prior-Guided Sparse Directed Graph Network for SAR Ship-Wake Detection**

[![Paper](https://img.shields.io/badge/Paper-Pattern%20Recognition%202026-0F6E56?style=flat-square)](https://doi.org/10.1016/j.patcog.2026.114294)
[![DOI](https://img.shields.io/badge/DOI-10.1016%2Fj.patcog.2026.114294-185FA5?style=flat-square)](https://doi.org/10.1016/j.patcog.2026.114294)
[![License](https://img.shields.io/badge/License-Apache%202.0-854F0B?style=flat-square)](LICENSE)

Published in *Pattern Recognition*, 180: 114294, 2026 —
[DOI](https://doi.org/10.1016/j.patcog.2026.114294) ·
[ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0031320326012598)

> **Note:** the peer-reviewed version of this work appears under the title *SCRC-Net*; this repository keeps the original working name.

> **Code release status:** the implementation is being organised for release. Star or watch this repository to be notified when it lands.

## Overview

Ship wakes in SAR imagery are long, thin and strongly directional, and they are routinely buried in sea clutter and speckle noise. HSDG-Net treats wake extraction as a structured graph problem:

- **Hessian prior** — supplies curvature information about ridge-like wake structures, giving the network a geometric prior instead of asking it to learn directionality from scratch.
- **Sparse directed graph** — models the wake as a sparse set of directed edges, which suppresses clutter responses that do not form a continuous track.

## Environment

Validated on:

- Ubuntu 20.04
- CUDA 12.4
- Python 3.9
- PyTorch 2.0.1 + cu118

## Training

```bash
python train.py --config configs/hsdgnet.yaml --data-root /path/to/dataset
```

## Evaluation

```bash
python eval.py --checkpoint checkpoints/hsdgnet.pth --data-root /path/to/dataset
```

## Citation

If you find this work useful, please cite:

```bibtex
@article{qi2026scrcnet,
  title   = {SCRC-Net: A Structure-Constrained and Representation-Consistent Network for SAR Ship Classification},
  author  = {Qi, Yuhang and Wang, Lu and Zhao, Chunhui and Mathiopoulos, P. Takis and Ohtsuki, Tomoaki and Adachi, Fumiyuki},
  journal = {Pattern Recognition},
  volume  = {180},
  pages   = {114294},
  year    = {2026},
  doi     = {10.1016/j.patcog.2026.114294}
}
```

## Contact

Lu Wang — Harbin Engineering University — wanglu2019@hrbeu.edu.cn
