---
title: 'From Threads to Tiles: T2T, a Compiler for CUDA-to-NPU Translation via 2D Vectorization'

# Authors
authors:
  - Shuaijiang Li
  - Jiacheng Zhao
  - Ying Liu
  - Shuoming Zhang
  - Lei Chen
  - Yijin Li
  - Yangyu Zhang
  - Zhicheng Li
  - Runyu Zhou
  - Xiyu Shi
  - Chunwei Xia
  - Yuan Wen
  - Xiaobing Feng
  - Huimin Cui

date: '2026-01-01T00:00:00Z'
doi: '10.1109/CGO68049.2026.11395190'

# Schedule page publish date (NOT publication's date).
publishDate: '2026-01-01T00:00:00Z'

publication_types: ['paper-conference']

publication: In *Proceedings of the 2026 IEEE/ACM International Symposium on Code Generation and Optimization (CGO)*
publication_short: In *CGO 2026*

abstract: 'CUDA’s programming model, exposing massive parallelism via fine-grained scalar threads, has become the de facto standard for GPU computing. Concurrently, NPUs are emerging as highly efficient accelerators, but their architecture is fundamentally different, relying on coarse-grained, explicit 2-D tile-based instructions. This creates a critical challenge: bridging the semantic gap "From Threads to Tiles". A direct translation is infeasible, as it requires lifting the implicit parallelism of CUDA’s scalar model into the explicit, multi-dimensional vector space of NPUs, a problem we formalize as a lifting challenge.This paper introduces T2T, a compiler framework that automates this "Threads to Tiles" translation via the 2-D Vectorization technique. T2T first transforms a CUDA kernel’s implicit SIMT parallelism into a structured, explicit loop nest via our Unified Parallelism Abstraction (UPA), making the parallelism analyzable. From this representation, T2T’s core vectorization engine systematically selects optimal pairs of loops and maps them onto the NPU’s 2-D tile instructions to maximize hardware utilization. To ensure correctness and handle performance-critical CUDA features, a final set of semantics-preserving optimizations is applied, including efficient control-flow management and vectorization of warp-level intrinsics.We implement T2T based on Polygeist and evaluate representative NPU architectures. On a diverse set of benchmarks, kernels translated by T2T achieve up to 73% of native CUDA performance on an A100 GPU and outperform baseline translation approaches by up to 6.9×. Our work demonstrates that a systematic, compiler-driven approach to 2-D vectorization is a principled and high-performance path for porting the rich CUDA ecosystem to the evolving landscape of NPU accelerators.'

summary: ''

tags:
  - MLIR
  - CUDA
  - Auto-Vectorization
  - Heterogeneous Computing
  - AI Accelerators

featured: false

url_pdf: 'https://ieeexplore.ieee.org/abstract/document/11395190'
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

image:
  caption: ''
  focal_point: ''
  preview_only: false

projects:
  - []

slides: ""
---