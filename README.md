<h1 style="
  display: flex;
  align-items: center;
">
  <img src="assets/img/logo.png" style="height:1.5em;">
  <span style="font-size: 48pt; margin-left: 0.2em;">
  CuSafe: Capturing Memory Corruptions on NVIDIA GPUs
  </span>
</h1>


<style>
/* 布局 */
.nav {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2em;
}

/* a 按钮 */
a.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;

  height: 60px;
  padding: 0 18px;

  background: #007acc;
  color: white;
  border-radius: 6px;

  text-decoration: none;
  font-weight: 500;
}

a.btn:hover {
  color: #005fa3;          /* 浅一点的白 */
}

summary.btn:hover {
  color: #005fa3;          /* 浅一点的白 */
}

details.inline > summary {
  all: unset;                 /* ← 关键：清空所有 UA 样式 */
  display: inline-flex;
  align-items: center;
  justify-content: center;

  height: 60px;
  padding: 0 18px;

  background: #007acc;
  color: white;
  border-radius: 6px;

  cursor: pointer;
  font-weight: 500;
}

details.inline {
  display: inline-block;   /* 不再撑高 flex 行 */
  position: relative;
  margin: 0;
  padding: 0;
}

summary.btn::after {
  display: none;
}

/* details 定位 */
details.inline {
  position: relative;
}

/* 弹窗 */
.popup {
  position: absolute;
  top: 120%;
  left: 50%;
  transform: translateX(-50%);

  background: #f9f9f9;
  color: black;

  padding: 16px;
  border: 1px solid #ccc;
  border-radius: 8px;

  width: 1000px;
  z-index: 10;
}
</style>## Overview of CuSafe

CuSafe is the <code style='color:#c52f21'>first</code> open-sourced sanitizer on NVIDIA GPUs. It captures all
kinds of memory corruptions, including out-of-bounds access, use-after-free,
double-free.

We show that CuSafe with extreme accuracy (<code
  style='color:#c52f21'>100%</code>) and low overhead (avg. <code
  style='color:#c52f21'>1.13x</code>). CuSafe also scales to large
applications, e.g., it can run on LLaMA 3 8B with less than 15% overhead.

<div class="nav">
  <a class="btn" href="./">Paper</a>

  <details class="inline">
    <summary class="btn">Cite</summary>
    <div class="popup">
      <h3>Citation</h3>
      <p>
@inproceedings{cusafe,  
author = {Hongyi Lu and Fengwei Zhang and Zhenkai Zhang and Shuai Wang and Yanan Guo},  
title = {CuSafe: Capturing Memory Corruptions on NVIDIA GPUs},  
booktitle = {35rd USENIX Security Symposium (USENIX Security 26)},  
year = {2026},  
publisher = {USENIX Association},  
month = aug  
}  
    </p>
    </div>
  </details>

  <a class="btn" href="https://doi.org/10.6084/m9.figshare.30821396">Source</a>

</div>

## Demonstration

#### Detecting Out-of-Bounds on RTX 5090 with CuSafe

<center>
  <script src="https://asciinema.org/a/nE9Y577deBYHQqWf.js" id="asciicast-nE9Y577deBYHQqWf" async="true"></script>
</center>
