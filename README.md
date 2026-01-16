# <img src="assets/img/logo.png" alt="Quick preview"></a> CuSafe: Capturing Memory Corruptions on NVIDIA GPUs

## Overview of CuSafe

CuSafe is the **first** open-sourced sanitizer on NVIDIA GPUs. It captures all
kinds of memory corruptions, including out-of-bounds access, use-after-free,
double-free.

We show that CuSafe with extreme accuracy (100%) and low overhead (1.13x on
average). CuSafe also scales to large applications, e.g., it can run on LLaMA 3 8B
with less than 15% overhead.

