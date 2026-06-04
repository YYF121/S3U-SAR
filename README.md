# S³U-SAR: Physics-Driven Semantic Scattering Structure Understanding of Aircraft Target in SAR Images

This repository is the official implementation of:

**Physics-Driven Semantic Scattering Structure Understanding of Aircraft Target in SAR Images**

S³U-SAR establishes a physical-semantic representation paradigm for SAR aircraft interpretation. Instead of representing aircraft targets as unordered local scattering responses, the proposed framework parses a SAR aircraft image into semantic scattering keypoints, visibility-aware attributes, and a physics-constrained structural topology.

> Code, dataset, and pretrained models will be released upon acceptance.

## Overview

Synthetic aperture radar (SAR) aircraft targets usually appear as sparse and discontinuous scattering responses due to coherent electromagnetic imaging. Conventional scattering-center-based representations are unordered and component-agnostic, making them unstable for fine-grained aircraft understanding.

S³U-SAR introduces:

- **Semantic scattering keypoints** to associate local electromagnetic responses with physically meaningful aircraft components.
- **Visibility-aware attributes** to distinguish scattering-salient, scattering-degraded, and semantically invalid responses.
- **Physics-constrained topology** to organize keypoints into a stable rigid-body structure.
- **Physics-guided supervision** to incorporate scattering heterogeneity, rigid-body topology, speckle uncertainty, and confidence-gated optimization.

## Framework

<p align="center">
  <img src="assets/framework.png" width="90%">
</p>

## Dataset: KP-SAR-Aircraft-1.0

We construct **KP-SAR-Aircraft-1.0**, a fine-grained benchmark for semantic scattering structure understanding of SAR aircraft targets.

The dataset provides:

- SAR aircraft target chips from Gaofen-3 imagery
- 10 semantic scattering keypoint annotations
- Visibility-aware attributes
- Physics-constrained topology definitions
- Aircraft category labels
- Orientation annotations

More details will be available in `docs/dataset.md`.

## Semantic Scattering Keypoints

The benchmark defines 10 semantic scattering keypoints corresponding to key aircraft components, including the nose, fuselage-wing region, tail, wing tips, wing roots, and engine-related regions.

<p align="center">
  <img src="assets/keypoint_definition.png" width="80%">
</p>

## Visibility Attributes

Each keypoint is assigned a SAR-specific visibility attribute:

- `v = 2`: scattering-salient keypoint
- `v = 1`: scattering-degraded but physically existing keypoint
- `v = 0`: semantically invalid or irrelevant response

## Results

S³U-SAR achieves strong performance on KP-SAR-Aircraft-1.0 and demonstrates robustness in cross-category evaluation, cross-dataset transfer, and downstream orientation estimation.

Detailed results, pretrained models, and evaluation scripts will be released later.

## TODO

- [ ] Release training and evaluation code
- [ ] Release dataset annotation format
- [ ] Release pretrained checkpoints
- [ ] Release visualization tools
- [ ] Release benchmark evaluation protocol

## Citation

If you find this work useful, please cite:

```bibtex
@article{Yin2026S3USAR,
  title   = {Physics-Driven Semantic Scattering Structure Understanding of Aircraft Target in SAR Images},
  author  = {Yin, Yifei and Shi, Hao and Li, Wei},
  journal = {IEEE Transactions on Image Processing},
  year    = {2026},
  note    = {under review}
}
