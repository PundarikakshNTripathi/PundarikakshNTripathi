<div align="center">

# Pundarikaksh Narayan Tripathi

Undergraduate Researcher | Computer Science & Engineering  
Babu Banarasi Das University · Lucknow, India

<br>

<a href="https://pundarikakshntripathi.github.io/">
  <img src="assets/pictures/favicon.png" width="20" height="20" align="middle" style="vertical-align: middle; background-color: #ffffff; border-radius: 4px; padding: 2px;"> Portfolio
</a> &nbsp;·&nbsp;
<a href="https://www.linkedin.com/in/pundarikakshnarayantripathi/">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" width="20" height="20" align="middle" style="vertical-align: middle;"> LinkedIn
</a> &nbsp;·&nbsp;
<a href="https://x.com/PundarikakshNT">
  <img src="assets/pictures/x-logo-white.svg#gh-dark-mode-only" width="18" height="18" align="middle" style="vertical-align: middle;">
  <img src="assets/pictures/x-logo-black.svg#gh-light-mode-only" width="18" height="18" align="middle" style="vertical-align: middle;"> X (Twitter)
</a> &nbsp;·&nbsp;
<a href="mailto:pundarikaksh.dev@gmail.com">
  <img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/Gmail_icon_%282020%29.svg" width="20" height="20" align="middle" style="vertical-align: middle;"> Email
</a>

</div>

---

I spend most of my time exploring the intersection of algorithmic AI and high-performance systems. My core interests lie in frontier AI, language modeling, computer vision, reinforcement learning, and more recently, mechanistic interpretability. I am particularly drawn to efficient AI and hardware-aware architectures. I like studying and developing new architectures and optimizers that are mathematically and computationally efficient, always keeping the underlying hardware in mind rather than treating it as a black box.

I am not an expert yet and there is still a massive amount for me to learn, but I enjoy diving deep into both the theoretical side of frontier models and the metal-level systems programming required to run them. Lately, I have been trying to balance my time between understanding transformer representations and learning GPU programming and HPC to squeeze out better performance. It is a constant learning process, and I build things from scratch to figure out how they actually work under the hood.

---

### Technical Competencies

* **Languages:** C, C++ (C++17/20), CUDA C++, Triton, Python, Go, SQL
* **Technologies:**
  * **AI & Machine Learning:** PyTorch, JAX, Hugging Face, scikit-learn, ONNX, OpenCV, Quantization (1.58-bit / GGUF)
  * **MLOps & Tooling:** Weights & Biases (wandb), MLflow, Optuna, Docker, Git, Linux
  * **Backend & Systems:** gRPC, Redis, AVX2 SIMD Intrinsics, Memory Management, Distributed Data Parallel
* **Concepts:** Artificial Intelligence, High-Performance Computing (HPC), GPU Architecture, System Design, Data Engineering

---

### Current Research and Development

#### [TernixEngine (In Development) | C++20, AVX2 SIMD, CUDA, HPC](https://github.com/PundarikakshNTripathi/TernixEngine)
I started building TernixEngine to test the practical hardware limits of 1.58-bit ternary Large Language Models (LLMs) from the ground up, bypassing standard deep learning abstractions. The primary goal was to replace floating-point matrix multiplications with AVX2 SIMD-accelerated integer additions and in-register bitwise unpacking. I recently stabilized the core CPU compute kernel, achieving an 8.2x throughput speedup over naive scalar branching. Translating the theoretical whitepapers into branchless C++ instructions has taught me a lot about strict memory alignment, L1 cache footprints, and hardware-level bottlenecks. The current focus is extending this architecture to CUDA shared-memory tiling and writing the Python quantization pipeline to parse real model weights, with the long-term goal of scaling the engine to support multimodal Vision-Language Models (VLMs). It remains a challenging project, and I am continually navigating the intricacies of low-level hardware intrinsics.

#### [VoltaSplat (Active Research) | C++20, CUDA C++, PyTorch](https://github.com/PundarikakshNTripathi/VoltaSplat)
I became fascinated by 3D vision and neural rendering and decided to build a differentiable CUDA rasterizer for 3D Gaussian Splatting entirely from scratch. What started as an excuse to learn CUDA parallel programming quickly escalated into a deep dive into hardware-accelerated graphics compute. Writing custom PyTorch C++ ATen bindings, managing tile-based radix sorting with NVIDIA CUB, and manually deriving analytical autograd gradients gave me a profound appreciation for GPU memory architectures. I successfully engineered the parallelized forward and backward pass kernels to bypass PyTorch's VRAM bottlenecks, resulting in a fully functional, high-performance rendering pipeline. Currently exploring Spherical Harmonics and Half-Precision optimization.

#### [nanoDist: Distributed Engine (In Development) | NumPy, HPC, MLOps, Distributed Systems](https://github.com/PundarikakshNTripathi/nanoDist)
Frameworks like PyTorch and JAX abstract away the complex mechanics of distributed training, and I wasn't satisfied with that. To truly understand how foundational models are scaled across clusters, I built a production-grade distributed ML engine from scratch using pure NumPy. Implementing manual automatic differentiation, ring all-reduce communication primitives, and ZeRO Stage 2 optimizer state partitioning taught me more about memory efficiency and network bottlenecks than simply reading papers. By mathematically deriving mixed-precision (FP16) pipelines and activation checkpointing algorithms, and wrapping it all in modern MLOps infrastructure (Docker, CI/CD, Optuna), the project evolved from a learning sandbox into a fully robust distributed systems architecture.

#### [HiveTorch: Federated Core (In Development) | PyTorch, Federated Learning, Statistics, MLOps](https://github.com/PundarikakshNTripathi/HiveTorch)
The temporary withdrawal of Claude Fable and Mythos from the market in early June this year sparked a lot of discussion around Sovereign AI, which is when I found federated learning being brought up in one such forum. It sounded interesting and completely inverted the standard ML paradigms I was used to, so I decided to look it up. And I simply loved the idea. I really liked the emphasis on decentralized AI and data privacy technology that is already quietly powering applications we use every day, like on-device predictive text. I wanted to dig deeper, and what better way to understand something than to build it from first principles? I created HiveTorch to build a Federated Learning orchestration engine from scratch. I experimented with the foundational  FedAvg  algorithm, specifically targeting the statistical challenges of model convergence when data is highly heterogeneous, using Dirichlet distributions to simulate non-IID edge topologies. Beyond just algorithmic math, I treated infrastructure as a first-class citizen: I wrapped the entire PyTorch engine in a robust, cloud-native MLOps pipeline using Kubernetes, gRPC for tensor serialization, Docker, Weights & Biases, and Prometheus. Writing custom edge-side SGD loops and orchestrating them via containerized microservices has been an incredible deep dive into distributed ML engineering.

---

### Collaboration & Open Initiatives

I am always looking to team up with other developers and researchers who want to push the boundaries of open-source AI. If you are working on distributed training systems, novel model architectures, or deep systems-level optimizations, I would love to connect. 

If you are putting together a team for a hackathon, an ML or HPC competition, or if you are working on some interesting open-source R&D project, I would love to be involved. You can drop me an email at pundarikaksh[dot]dev[at]gmail[dot]com, or send a message on X.

<div align="center">

**Feel free to explore my repositories, open issues, and contribute to them if you want. Oh, and don't forget to star the ones you like!**

</div>
