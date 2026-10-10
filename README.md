<div align="center">

# Pundarikaksh Narayan Tripathi

ML systems and AI research · Lucknow, India  
B.Tech CSE (AI), Babu Banarasi Das University, 2027

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

I write the low-level parts of machine learning from scratch, measure them, and keep the numbers honest. The
longer-term aim is research on how models reason, and what it would take for a system to learn the way a
scientist does: from a few observations, with causal structure rather than correlation.

### Measured results

Every figure below is produced by a script in the linked repository, on an i7‑14650HX and an RTX 5060 Laptop.

| Project | What it is | Result |
|---|---|---|
| [TernixEngine](https://github.com/Quiet-Intelligence/TernixEngine) | 1.58-bit LLM inference kernels, AVX2 and CUDA, bit-exact against an integer reference | **10.2×** over scalar on CPU (86.8 → 8.5 ms, 512³, one core); **5.6×** over naive on GPU at 4096³ |
| [Aegis](https://github.com/Quiet-Intelligence/aegis) | eBPF LSM enforcement and behavioural scoring for autonomous coding agents | **3.75 µs** to score a kernel event; validated live on native Linux and WSL2 |
| [VoltaSplat](https://github.com/PundarikakshNTripathi/VoltaSplat) | Differentiable 3D Gaussian Splatting rasterizer in CUDA, hand-derived gradients | **612 FPS** at 100k Gaussians; **6.1 ms** forward at 1M; gradients match a reference to 1e‑6 |
| [nanoDist](https://github.com/PundarikakshNTripathi/nanoDist) | Data-parallel training in NumPy: ring all-reduce over TCP, ZeRO‑2, checkpointing | **−68%** memory per worker (106 → 34 MB) |
| [HiveTorch](https://github.com/PundarikakshNTripathi/HiveTorch) | FedAvg over gRPC on Kubernetes, Dirichlet non-IID clients | gRPC run equals in-process to **1e‑6**; 97.3% IID → 92.9% at α = 0.1 |
| [Causal-DML](https://github.com/PundarikakshNTripathi/Causal-DML) | Double machine learning on 30 GB of logs, served as a counterfactual API | Recovers a planted null effect under confounding (ATE −1.7e‑3) |
| [LumaSort-Engine](https://github.com/PundarikakshNTripathi/LumaSort-Engine) | Real-time luminance pixel sorting, C++20 and OpenGL compute shaders | **640K** particles at 60+ FPS |

### How the work is done

- **Derive it, then test it against something independent.** VoltaSplat's CUDA backward pass is checked against a
  separate PyTorch renderer, which is itself checked against float64 finite differences. TernixEngine's kernels
  are compared bit for bit with an integer GEMM. nanoDist's ZeRO‑2 must reproduce single-process Adam.
- **Say what was and wasn't measured.** The READMEs list what is not implemented and what hasn't been compared
  yet. TernixEngine is a kernel library, not a model runtime, and it says so on the first screen.
- **Keep negative results.** Leakage is the clearest case. On the FlyRank ranking task a random split scored
  P@50 0.94 and a client-grouped split scored 0.70. The grouped number is the one I report.

### Research directions

Reading and prototyping, nothing published yet:

- **Fluid intelligence and abstraction.** Program-synthesis and compression-based accounts of generalisation,
  ARC-style tasks, and why current models interpolate well and extrapolate poorly.
- **Causal reasoning.** Whether a system can climb Pearl's ladder (association, intervention, counterfactual)
  rather than imitate its text, and how to test that without leaking the answer.
- **Efficient models.** What ternary and other low-bit weights cost in capability, and whether interpretability
  tools such as sparse autoencoders still work on them.
- **Oversight of agents.** Behavioural scoring from kernel telemetry, the problem Aegis is built around.

### Competitions and work

- **FlyRank AI**, ML engineering intern, July to September 2026. Ranking pipeline over 79.8M interaction
  records; P@50 0.56 → 0.70 on a client-grouped holdout.
- **Amazon ML Challenge 2026**, entity resolution scored by macro F0.5. Third on both the public and private
  leaderboards at the last check (0.991762). We did not reach the finals, and the approach stays private.
- **HackArena 2025**, second place (Masai × NoBroker), backend for a civic complaint tracker.

### Stack

C, C++17/20, CUDA, Triton, Python, Go, SQL · PyTorch, JAX, ONNX, Hugging Face, scikit-learn · SIMD/AVX2, eBPF,
Cedar, gRPC, Kubernetes, Docker, DuckDB, FastAPI · EconML, DoWhy, MLflow, Prometheus

### Contact

Email is the quickest: pundarikaksh[dot]dev[at]gmail[dot]com. I'm glad to talk about inference, kernels,
causal methods, agent security or anything in the table above. Issues and pull requests are welcome.
