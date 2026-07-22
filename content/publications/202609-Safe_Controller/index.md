---
title: "Learning Safe-by-Design Neural Network Controllers"
authors:
  - Yang Zhao
  - Jungeun Lee
  - Jeong hwan Jeon
  - Sze Zheng Yong
date: "2026-07-15"
publishDate: "2026-07-15"
publication: "65th IEEE Conference on Decision and Control"
publication_short: "CDC 2026"

abstract: Safety filters constructed from control barrier functions (CBFs) are commonly appended to pre-trained neural network controllers to enforce safety requirements. However, this decoupled design with hand-tuned, fixed CBF parameters often fails to adapt to the underlying controller, yielding overly conservative solutions. Thus, given a valid CBF, we address these limitations by jointly learning a neural network controller and neural-network-parameterized CBF parameters, enforcing the resulting affine safety constraints by construction and avoiding an online quadratic program (QP) safety filter at run time. To further improve computational efficiency and scalability, we introduce a lightweight projection architecture that enforces constraints without full constraint enumeration. Extensive simulation evaluations demonstrate reliable, scalable safety constraint satisfaction at reduced computational cost.

tags:
 - Constrained Neural Networks
 - Hard Constraint Satisfaction
featured: true

links:
  - type: preprint
    url: https://arxiv.org/abs/2605.26534

image:
  preview_only: true
---
