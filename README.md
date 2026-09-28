<div align="center">

# Pundarikaksh Narayan Tripathi

Independent AI and ML systems researcher · Founder, [Quiet Intelligence](https://quietintelligence.org)  
Final-year B.Tech CSE (AI), Babu Banarasi Das University · Lucknow, India

<br>

<a href="https://pundarikakshntripathi.github.io/">
  <img src="assets/pictures/favicon.png" width="20" height="20" align="middle" alt=""> Portfolio
</a> &nbsp;·&nbsp;
<a href="https://www.linkedin.com/in/pundarikakshnarayantripathi/">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" width="20" height="20" align="middle" alt=""> LinkedIn
</a> &nbsp;·&nbsp;
<a href="https://x.com/PundarikakshNT">
  <img src="assets/pictures/x-logo-white.svg#gh-dark-mode-only" width="18" height="18" align="middle" alt="">
  <img src="assets/pictures/x-logo-black.svg#gh-light-mode-only" width="18" height="18" align="middle" alt=""> X (Twitter)
</a> &nbsp;·&nbsp;
<a href="mailto:pundarikaksh.dev@gmail.com">
  <img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/Gmail_icon_%282020%29.svg" width="20" height="20" align="middle" alt=""> Email
</a>

</div>

---

I work on the layer of machine learning most people never have to look at: kernels, memory traffic, and the
systems that decide whether a model is fast enough, and safe enough, to be useful.

I learn things by building a smaller version of them. When I wanted to understand how distributed training
moves data between machines, I wrote it in plain NumPy and derived every backward pass by hand. When the
1.58-bit papers came out, I wanted to know how fast a ternary model could run on an ordinary CPU, so I wrote
the kernels myself. My coursework mostly stops at calling the library, and I kept wanting to know what the
library was doing.

This year I founded **[Quiet Intelligence](https://quietintelligence.org)**, a small independent research
lab for that work. It has three threads: the systems that run models, research on the models themselves, and
mechanistic interpretability. It's early days.

### Now

- **Leading** research at Quiet Intelligence, where I'm building Aegis and TernixEngine.
- **Interning** as an ML engineer at [FlyRank AI](https://flyrank.ai). I built a ranking pipeline over 79M+
  interaction records and took Precision@50 from 0.24 to 0.74 against the program's heuristic baselines.
- **Placed third** in the Amazon ML Challenge 2026 on both the public and private leaderboards (business
  entity resolution; official results pending).
- **Studying:** B.Tech CSE (AI), graduating in 2027.

---

### Selected work

#### [Aegis](https://github.com/Quiet-Intelligence/aegis) · Go, eBPF, SQLite, AWS Cedar
A kernel-level security and memory layer for autonomous coding agents. It started with a real vulnerability
in which a prompt-injected agent used perfectly legitimate `git` commands to escape its workspace. No single
step was forbidden; the sequence was the attack.
- eBPF LSM hooks stream every file open, connection and exec into a temporal behavior graph.
- Sequences it has judged before are recalled from a local vector memory, and new ones go to a pluggable
  LLM adjudicator.
- A LinUCB bandit tunes the scorer's sensitivity.
- Hard rules are written in Cedar and compiled into kernel maps.

It sustains 5,120 events/s with no drops, at 0.42 ms p99 pipeline latency.

#### [TernixEngine](https://github.com/Quiet-Intelligence/TernixEngine) · C++20, AVX2, CUDA, PyBind11
A dependency-free inference engine for 1.58-bit ternary LLMs. With ternary weights you never need to multiply.
- **CPU:** weights are unpacked inside registers, and matrix products become branchless AVX2 adds and
  subtracts. On a 512×512 ternary matmul that's **8.2× faster** than the scalar baseline (122.4 ms to
  15.0 ms on an i7‑14650HX).
- **CUDA:** weights stream into shared memory with `cp.async`, and each warp reduces with shuffles.

#### Amazon ML Challenge 2026 · third place · Python, LightGBM, multilingual-e5
Business entity resolution: find every record of the same business across three noisy directories, scored
by macro F0.5.
- **Retrieval:** 13 lexical retrievers plus an e5 embedding search reach 99.8% candidate recall.
- **Ranking:** LightGBM ranks the candidates, then fine-tuned cross-encoders in a five-seed bag re-rank them.
- **Selection:** a calibrator picks each match set to maximize expected F0.5.
- **Unlabeled region:** France appeared only in the test set, so closing that gap took pseudo-labels and
  audited rules.

The final public score was 0.9918. The code stays private until the results are announced.

#### [VoltaSplat](https://github.com/PundarikakshNTripathi/VoltaSplat) · C++20, CUDA, PyTorch
A differentiable 3D Gaussian Splatting rasterizer written from scratch and plugged into PyTorch through ATen.
- The pipeline is tile-based, with 64-bit depth sorting through NVIDIA CUB and shared-memory staging.
- Both passes are hand-written, including analytical gradients.
- It renders at 476 FPS at 100k Gaussians, with a 16.2 ms forward pass at 1M (RTX 5060 Laptop, 800×800).

#### Also built
- **[nanoDist](https://github.com/PundarikakshNTripathi/nanoDist):** distributed training in pure NumPy, with
  hand-derived autograd, ring all-reduce, ZeRO Stage 2, mixed precision and activation checkpointing. It cuts
  peak memory per worker from 106 MB to 34 MB (−68%).
- **[HiveTorch](https://github.com/PundarikakshNTripathi/HiveTorch):**
  - What it is: federated learning (FedAvg) on Kubernetes over gRPC, with Dirichlet-sharded non-IID clients.
  - How it started: the talk about sovereign AI earlier this year got me reading about federated learning,
    and I wanted to build it from first principles.
- **[Causal-DML](https://github.com/PundarikakshNTripathi/Causal-DML):** double machine learning (EconML,
  DoWhy) to estimate what a retention offer would actually do for each user, with a FastAPI and Streamlit
  counterfactual simulator.
- **[LumaSort-Engine](https://github.com/PundarikakshNTripathi/LumaSort-Engine):** real-time pixel sorting by
  luminance, 640K particles at 60+ FPS in C++20 and OpenGL compute shaders.

---

### Toolbox

- **Languages:** C, C++17/20, CUDA C++, Triton, Python, Go, SQL
- **ML:** PyTorch, JAX, ONNX, scikit-learn, XGBoost, LightGBM, Hugging Face, OpenCV
- **Causal and RL:** EconML, DoWhy, double machine learning, LinUCB bandits, process reward models
- **Systems:** SIMD/AVX2 intrinsics, GPU programming, eBPF and Linux security modules, AWS Cedar, CMake
- **Data and infrastructure:** DuckDB, Apache Arrow, Docker, Kubernetes, gRPC, FastAPI, Kafka, Spark, Redis,
  PostgreSQL
- **Experiments:** Weights & Biases, MLflow, Optuna, Prometheus

---

### Get in touch

I'm happy to talk about research, collaborations, internships, competitions or open-source work. If you're
working on inference, kernels, distributed training or interpretability and want another pair of hands, I'd
especially like to hear from you.

The easiest way to reach me is email, at pundarikaksh[dot]dev[at]gmail[dot]com, or a message on X.
Issues and pull requests on any of these repositories are welcome.
