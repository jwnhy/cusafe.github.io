<h1 style="
  display: flex;
  align-items: center;
">
  <img src="assets/img/logo.png" style="height:1.5em;">
  <span style="font-size: 48pt; margin-left: 0.2em;">
  CuSafe: Capturing Memory Corruptions on NVIDIA GPUs
  </span>
</h1>

## Overview of CuSafe

CuSafe is the <code style='color:#c52f21'>first</code> open-sourced sanitizer on NVIDIA GPUs. It captures all
kinds of memory corruptions, including out-of-bounds access, use-after-free,
double-free.

We show that CuSafe with extreme accuracy (<code
  style='color:#c52f21'>100%</code>) and low overhead (avg. <code
  style='color:#c52f21'>1.13x</code>). CuSafe also scales to large
applications, e.g., it can run on LLaMA 3 8B with less than 15% overhead.

<center >
  <button style="margin-right:2em;">
    <a href="./" style="color:white">Paper</a>
  </button>
  <button style="margin-right:2em">
    <a href='./' style="color:white">Cite</a>
  </button>
  <button>
    <a href='./' style="color:white">Source</a>
  </button>
</center>

## Demonstration

<center>
  <h4>
    Detecting Out-of-Bounds on RTX 5090 with CuSafe
  </h4>
</center>

<center>
  <script src="https://asciinema.org/a/nE9Y577deBYHQqWf.js" id="asciicast-nE9Y577deBYHQqWf" async="true"></script>
</center>
