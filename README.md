### Hi there, I'm Barış

AI Engineer focused on **LLM compression** (pruning, distillation, quantization),
**agent systems**, and **Kubernetes infrastructure** — turning research into
working systems, from consumer hardware to air-gapped setups. My open models
and datasets on Hugging Face have passed **170K+ downloads**.

---

### What I Do

- **LLM Compression & Inference** — expert pruning (REAP) of MoE models, LoRA
  reasoning distillation, GGUF / MLX / MTPLX quantization, and speculative
  decoding with multi-token prediction (MTP) heads
- **Agent Systems** — multi-agent orchestration that routes cloud and local
  models to task agents, autonomous server-monitoring agents, MCP and tool
  calling; Claude Code on alternative model backends
- **Kubernetes Infrastructure** — one-command k3s stacks for VMs (KubeVirt,
  CDI), storage (Longhorn), VM networking (Multus), auth (Keycloak OIDC), a
  private CA (step-ca) and monitoring (VictoriaMetrics), portable to
  air-gapped environments and isolated with NetworkPolicy and Pod Security
- **AI Security** — trust boundaries and supply-chain integrity of open-weight
  and air-gapped LLM deployments

---

### Model Work · [huggingface.co/barozp](https://huggingface.co/barozp)

26 models and 4 datasets in GGUF, MLX and MTPLX formats.

- **[REAP-pruned + MTP-grafted MoE](https://huggingface.co/barozp/Qwen3.6-29B-REAP-Opus-Reasoning-Distill-MLX-3bit)** — pruned 20% of the experts with REAP and applied LoRA reasoning distillation, lifting ARC-Challenge *above* the unpruned model (0.53 → 0.62). Reverse-engineered the MTP head broken by pruning and grafted it back onto the new expert layout: **+39–67%** generation speed with llama.cpp speculative decoding
- **[Reasoning-distilled dense model](https://huggingface.co/barozp/Qwen3.8-27B-Opus-Distill-v2-MTPLX-4bit)** — LoRA distillation on an 11.7K-sample reasoning dataset doubled GPQA Diamond (0.23 → 0.47); MTP raised generation speed **2.4×** on Apple Silicon
- **[opus-reasoning-distill-v2](https://huggingface.co/datasets/barozp/opus-reasoning-distill-v2)** — the reasoning-trace dataset behind the distillations

---

### Technical Reports

- **[Speculation or Substance? Rethinking How LLMs Get Faster](https://github.com/ozp3/speculative-decoding-vs-mtp)** (2026) — speculative decoding vs. multi-token prediction: architecture, cost, energy, and the real bottlenecks of production inference · [DOI](https://doi.org/10.5281/zenodo.21504354)
- **[Can We Trust Open-Weight Large Language Models?](https://github.com/ozp3/open-weight-llm-trust-boundary)** (2026) — a security perspective on air-gapped deployments, supply-chain trust, and the limits of transformer-based systems · [DOI](https://doi.org/10.5281/zenodo.21430999)

---

### Selected Work

**AI & LLMs**

- **[anthropic-openai-proxy](https://github.com/ozp3/anthropic-openai-proxy)** — local Anthropic ↔ OpenAI API translation proxy that lets coding agents like Claude Code drive vLLM, SGLang, or any OpenAI-compatible backend (reasoning, tool calls, SSE streaming)
- **[claude-code-deepseek](https://github.com/ozp3/claude-code-deepseek)** — Claude Code on DeepSeek V4 through its Anthropic-compatible API with the full 1M context, plus a sourced cost comparison against Claude plans
- **[Stack-in-a-Click](https://github.com/ozp3/stack-in-a-click)** — one-click SaaS provisioning with Hermes Agent + Stripe Projects, built for the Hermes Agent Accelerated Business Hackathon (NVIDIA × Stripe × Nous Research)
- **[SRMS](https://github.com/ozp3/srms-landing)** — AI-powered infrastructure issue reporting: a single photo goes through a two-stage AI pipeline and is routed to the responsible unit. Graduation project with a six-person team (Team Vexra) at Atılım University; I wrote the [benchmark tool](https://github.com/ozp3/srms-benchmark) for its DistilBERT classifier (ONNX Runtime), which reaches 90.7% accuracy over 14 categories

**Open Source**

- **[Deep-Live-Cam](https://github.com/hacksider/Deep-Live-Cam)** — AMD DirectML optimizations (GPU face detection, detection throttling, pre-load fix) that prevent live-mode crashes and raise frame rates, merged upstream ([PR #1710](https://github.com/hacksider/Deep-Live-Cam/pull/1710))

**Systems & Tools**

- **[Ultimate-Privacy-Server](https://github.com/ozp3/Ultimate-Privacy-Server)** — Pi-hole + Unbound + PiVPN (WireGuard) + Zapret DPI bypass on a single Linux server, with a step-by-step guide in English, Chinese, and Turkish
- **[PowerFlow](https://github.com/ozp3/PowerFlow)** — live power-flow Sankey diagram for Apple Silicon Macs (adapter → battery → system → CPU/GPU), no sudo required
- **[Simple-Metadata-Remover](https://github.com/ozp3/Simple-Metadata-Remover)** — Windows app that strips date, location, and device metadata from videos with FFmpeg, without re-encoding

---

### Languages & Tools

[![](https://skillicons.dev/icons?i=python,pytorch,bash,ts,c,cpp,cs,java&perline=8)](https://skillicons.dev/)
[![](https://skillicons.dev/icons?i=kubernetes,docker,linux,apple,githubactions,git,nextjs,nodejs,flask&perline=9)](https://skillicons.dev/)

**LLM stack:** llama.cpp · MLX · MTPLX · vLLM · SGLang · ONNX Runtime · lm-evaluation-harness  
**Infra:** k3s · KubeVirt · Longhorn · Multus · Traefik · Keycloak · step-ca · VictoriaMetrics · nftables

---

### Connect

- **LinkedIn:** [baris-ozpulat](https://www.linkedin.com/in/baris-ozpulat)
- **Hugging Face:** [barozp](https://huggingface.co/barozp)
- **X:** [@0xOzp](https://x.com/0xOzp)
