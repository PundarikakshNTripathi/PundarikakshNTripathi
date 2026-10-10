<div align="center">

# Pundarikaksh Narayan Tripathi

AI research and engineering, from the math to the metal  
Lucknow, India

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

Hi, I'm Pundarikaksh.

I got into machine learning because I wanted to know why it works, and I've never been satisfied with the
answer "because the library does it." So I tend to rebuild things until I can see inside them: the kernel that
makes a 1.58-bit model fast, the backward pass behind a renderer, the all-reduce that keeps a hundred GPUs
agreeing with each other. Some of that is engineering. A lot of it is just trying to understand.

What I'm really after is the harder question underneath. Why do models interpolate so well and extrapolate so
badly? What would it take for a system to reason causally instead of imitating text that was written by people
who did? I read a lot of the math around that (causal hierarchies, compression and abstraction, program
synthesis, the ARC problem), and I use the systems work to keep myself honest about what can actually be
measured. I haven't published yet. That's the plan for this year.

### Things I've built

- **[TernixEngine](https://github.com/Quiet-Intelligence/TernixEngine)**: 1.58-bit LLM inference kernels in C++,
  AVX2 and CUDA. With ternary weights there's nothing to multiply, so the whole game is not wasting what you
  saved. It runs 10.2× faster than the scalar baseline on a single CPU core, and every kernel matches an integer
  reference bit for bit.
- **[Aegis](https://github.com/Quiet-Intelligence/aegis)**: eBPF and Go. It watches what an autonomous agent does
  at the kernel and learns what normal looks like, because the dangerous attacks are sequences of steps that are
  each allowed on their own. I wrote it after reading about a real sandbox escape built exactly that way.
- **[VoltaSplat](https://github.com/PundarikakshNTripathi/VoltaSplat)**: a differentiable 3D Gaussian Splatting
  rasterizer in CUDA, with the gradients derived by hand. 612 FPS at 100k Gaussians.
- **[nanoDist](https://github.com/PundarikakshNTripathi/nanoDist)**: distributed training in plain NumPy. Ring
  all-reduce over real sockets, ZeRO Stage 2, 68% less memory per worker.
- **[HiveTorch](https://github.com/PundarikakshNTripathi/HiveTorch)**: federated averaging over gRPC on
  Kubernetes, with deliberately skewed clients.
- **[Causal-DML](https://github.com/PundarikakshNTripathi/Causal-DML)**: double machine learning on 30 GB of
  listening logs, served as a counterfactual API.
- **[LumaSort-Engine](https://github.com/PundarikakshNTripathi/LumaSort-Engine)**: 640K particles sorting
  themselves by brightness in real time. Just for fun.

### Along the way

- Interned at [FlyRank AI](https://flyrank.ai) over the summer, on ranking and causal inference. The result I'm
  proudest of is a negative one: a random split said 0.94, the honest split said 0.70.
- Third on both leaderboards at the last check in the Amazon ML Challenge 2026 (entity resolution, score
  0.991762). We missed the finals.
- Second place at HackArena 2025.

### Toolbox

- **Languages:** C, C++17/20, CUDA C++, Triton, Python, Go, SQL
- **ML:** PyTorch, JAX, ONNX, scikit-learn, XGBoost, LightGBM, Hugging Face, OpenCV
- **Causal and RL:** EconML, DoWhy, double machine learning, LinUCB bandits, process reward models
- **Systems:** SIMD/AVX2 intrinsics, GPU programming, eBPF and Linux security modules, AWS Cedar, CMake
- **Data and infrastructure:** DuckDB, Apache Arrow, Docker, Kubernetes, gRPC, FastAPI, Kafka, Spark, Redis,
  PostgreSQL
- **Experiments:** Weights & Biases, MLflow, Optuna, Prometheus

---

### Say hello

If you're working on inference, kernels, causal methods, or the theory of how models generalize, I'd like to
hear what you're stuck on. If you're hiring for research or ML systems, or you want a collaborator on something
hard, write to me. I read every email.

**pundarikaksh[dot]dev[at]gmail[dot]com** · [LinkedIn](https://www.linkedin.com/in/pundarikakshnarayantripathi/)
· [X](https://x.com/PundarikakshNT) · [Portfolio](https://pundarikakshntripathi.github.io/)
