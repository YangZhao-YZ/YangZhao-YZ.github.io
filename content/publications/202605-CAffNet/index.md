---
title: "CAffNet: Hard Constraint-Affine Neural Networks"
authors:
  - Yang Zhao
  - Jungeun Lee
  - Jeong hwan Jeon
  - Sze Zheng Yong
date: "2026-04-30"
publishDate: "2026-04-30"
publication: "The 43rd International Conference on Machine Learning"
publication_short: "ICML 2026"

abstract: We present a novel framework for embedding hard constraint satisfaction into neural network (NN) architectures, specifically feedforward neural networks and transformers, with input-dependent affine constraints of arbitrary cardinality. Traditional constraint enforcement approaches either rely on penalty-based soft constraints, which offer no guarantee of satisfaction, or on post-processing methods that enforce constraints after the NN is trained, which may lead to suboptimality. We introduce a trainable constraint-affine (CAffine) layer into NNs, yielding CAffNet, which goes beyond enforcing affine constraints via fixed orthogonal or parallel projections and enables joint optimization with network parameters. Moreover, we impose no restrictions on the constraint space dimensions and establish that our construction preserves the universal approximation properties of NNs, while providing provable guarantees on constraint adherence for all inputs. Experimental validation demonstrates robust performance across diverse domains requiring guaranteed constraint satisfaction.

tags:
 - Constrained Neural Networks
 - Hard Constraint Satisfaction
 - Universal Approximation
 - 
featured: true

links:
  - type: pdf
    url: https://arxiv.org/abs/2605.24437

image:
  preview_only: true
---
