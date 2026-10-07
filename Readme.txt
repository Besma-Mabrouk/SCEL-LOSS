 Saturated Class-wise ECDF Loss (SCEL)

Code, results, and manuscript tables for the paper:

> **A Saturated Class-wise Empirical Cumulative Distribution Function Loss
> for Stable Three-Dimensional Segmentation of Hippocampal Subfields:
> A Two-Phase Ablation Study**

## Overview

This repository contains the full experimental pipeline for SCEL, a
bounded and calibration-free boundary-aware loss for 3D medical image
segmentation. The pipeline has two phases:

- **Phase 1**: architecture saturation. A fixed BCE--Dice loss is used
  to ablate a cumulative chain of architectural additions to a 3D
  residual U-Net. No variant meets the pre-registered saturation
  criterion (Delta Dice > 0.01 with bootstrap CI excluding zero).
- **Phase 2**: loss ablation. The baseline architecture is frozen and
  seven losses are compared over ten seeds: BCE--Dice, euclidean,
  old_ecdf, improved_ecdf, boundary_kervadec, tversky, and the proposed
  SCEL.


