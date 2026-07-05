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

#### [TernixEngine (In Development) | C++20, AVX2 SIMD, HPC](https://github.com/PundarikakshNTripathi/TernixEngine)
I started building TernixEngine because I wanted to see how far I could push CPU inference for quantized models. I was fascinated by 1.58-bit ternary vision-language networks and wanted to understand the math and memory access patterns from the ground up, without relying on heavy frameworks. Replacing standard FP16 matrix multiplications with AVX2 SIMD-accelerated integer additions has been fun and helped me learn about hardware-level optimization, memory footprints, and token throughput bottlenecks, which I probably would not have if I just kept myself isolated to reading theory. It is a challenging project, and I am still figuring out a lot of the low-level intrinsics as I go.

#### [VoltaSplat (Active Research) | C++20, CUDA C++, PyTorch](https://github.com/PundarikakshNTripathi/VoltaSplat)
I got interested in 3D vision and neural rendering and decided to try implementing a differentiable CUDA rasterizer for 3D Gaussian Splatting from scratch. It started as a way to learn CUDA and parallel programming, but writing custom PyTorch C++ bindings and dealing with tile-based radix sorting using NVIDIA CUB really, let's just say, gave me a whole new perspective on the complexities of hardware-accelerated graphics and compute. I am currently working on engineering parallelized forward and backward pass kernels, which has been a great learning experience in GPU architecture.

#### [nanoDist: Distributed Engine (In Development) | NumPy, HPC, MLOps, Distributed Systems](https://github.com/PundarikakshNTripathi/nanoDist)
Frameworks like PyTorch and JAX abstract away the complex mechanics of distributed training, and I wasn't satisfied with that. To truly understand how foundational models are scaled across clusters, I built a production-grade distributed ML engine from scratch using pure NumPy. Implementing manual automatic differentiation, ring all-reduce communication primitives, and ZeRO Stage 2 optimizer state partitioning taught me more about memory efficiency and network bottlenecks than simply reading papers. By mathematically deriving mixed-precision (FP16) pipelines and activation checkpointing algorithms, and wrapping it all in modern MLOps infrastructure (Docker, CI/CD, Optuna), the project evolved from a learning sandbox into a fully robust distributed systems architecture.

#### [HiveTorch: Federated Core (In Development) | PyTorch, Federated Learning, Statistics](https://github.com/PundarikakshNTripathi/HiveTorch)
The withdrawal of Claude Fable and Mythos from the market in early June this year sparked a lot of discussion around Sovereign AI, which is when I found federated learning being brought up in one such forums. It sounded interesting and different from most of the common ML patterns I had seen, so I decided to look it up and learn exactly what it is. And I, in simple terms, just loved the idea. I really liked the emphasis on decentralized AI and privacy, and you know, it is already powering common applications we use everyday (like on-device auto-typing and word prediction)! I wanted to dig deeper, and what better to understand something than to build it from first principles? So, I created HiveTorch to build a Federated Learning system from scratch. I'm experimenting with FedAvg and simulating non-IID data topologies using Dirichlet distribution sharding. It is an ongoing project where I am figuring out the statistical challenges of model convergence when data is highly heterogeneous across edge devices. Writing custom client-side SGD loops and centralized state-dict aggregations has been a solid way to practice orchestrating complex ML pipelines.

---

### Collaboration & Open Initiatives

I am always looking to team up with other developers and researchers who want to push the boundaries of open-source AI. If you are working on distributed training systems, novel model architectures, or deep systems-level optimizations, I would love to connect. 

If you are putting together a team for a hackathon, an ML or HPC competition, or if you are working on some interesting open-source R&D project, I would love to be involved. You can drop me an email at pundarikaksh.dev@gmail.com, or send a message on X.

<div align="center">

**Feel free to explore my repositories, open issues, and contribute to them if you want. Oh, and don't forget to star the ones you like!**

</div>
