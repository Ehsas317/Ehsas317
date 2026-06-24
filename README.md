# Ehsas Sethi — Building Local-First AI Systems

**Edge AI · Apple Silicon · Python Systems**

I design agentic AI orchestration systems that run entirely on local hardware. No cloud dependencies, no API keys, no data leaving your machine. Just pure silicon doing intelligent work.

---

## About Me

| | |
|---|---|
| **Name** | Ehsas Sethi |
| **Born** | 3 January 2007 |
| **Hometown** | Abohar, Punjab, India |
| **Education** | B.E. Computer Engineering, Thapar Institute of Engineering & Technology (TIET), Patiala — Batch of 2030 |

A small-town kid from Abohar with a deep obsession for clean architecture, zero-bloat systems, and making AI run where it matters most — on your own hardware.

---

## Featured Projects

### [brain_loader](https://github.com/Ehsas317/brain_loader) — Agentic AI Orchestration
A portable, hardware-aware multi-agent system with a **pure-Python coordinator** and **single hot-swap model slot**.

- **Brain model** plans 30-80 task roadmaps and adapts after every task
- **Specialist models** (coder, researcher, writer, critic, math) execute each task
- **One model in RAM at a time** — all memory goes to the active model
- Targets Apple Silicon via MLX, includes Ollama backend for any system
- Deterministic regex parsing instead of LLM coordination — zero overhead, zero hallucination

```yaml
Architecture: Pure Python coordinator + hot-swap model slot
Backends:     MLX (Apple Silicon), Ollama (universal)
Models:       Qwen3-32B, Qwen2.5-Coder, Llama-3.3-70B
RAM Layout:   0 GB coordinator + 20-24 GB active model + 3-4 GB system
License:      MIT
```

**Key design insight:** Replacing the coordinator LLM with pure Python frees ~4 GB of RAM for the KV cache — that's the difference between fitting a 32B model and not.

---

### [trio](https://github.com/Ehsas317/trio) — Personal AI Ecosystem
Three specialized AI assistants sharing a unified core framework and vector database knowledge base on a Mac Mini M4.

| Assistant | Name | Role |
|-----------|------|------|
| **NAMI** | Network and Machine Intelligence | Telegram bot for system control and monitoring |
| **RUSH** | Recording and Understanding Speech Helper | Audio transcription via whisper.cpp + LLM summarization |
| **VEX** | Video Exploration Helper | Scene detection + automated clip extraction |

- Shared **ChromaDB vector store** for cross-assistant knowledge
- **Flask dashboard** for real-time monitoring
- **launchd** integration for macOS auto-start
- Metal-accelerated inference via whisper.cpp + Ollama

```yaml
Platform:     macOS (Apple Silicon)
Inference:    Ollama (local LLMs), whisper.cpp (Metal)
Vector DB:    ChromaDB with cross-assistant knowledge sharing
Interface:    Telegram bot + Flask web dashboard
License:      MIT
```

---

## Technical Focus

```
┌─────────────────────────────────────────────┐
│  Local-First AI Architecture                │
│  • Model orchestration & hot-swapping       │
│  • RAM-aware scheduling on constrained HW   │
│  • Deterministic coordination (no LLM bloat)│
│  • Apple Silicon optimization (MLX, Metal)  │
├─────────────────────────────────────────────┤
│  Systems Programming                        │
│  • Pure Python state machines               │
│  • Async I/O & process lifecycle management │
│  • Vector embeddings & semantic search      │
│  • Event-driven assistant architectures     │
├─────────────────────────────────────────────┤
│  Python Tooling                             │
│  • Modern packaging (pyproject.toml)        │
│  • Type hints & static analysis             │
│  • YAML/JSON configuration systems          │
│  • API design (Flask, Telegram bots)        │
└─────────────────────────────────────────────┘
```

---

## Stack

**Languages:** Python 3.11+ · YAML · Shell  
**AI/ML:** MLX · Ollama · ChromaDB · Whisper.cpp  
**Systems:** launchd · asyncio · multiprocessing  
**Web:** Flask · python-telegram-bot  
**Tools:** Git · Homebrew · ffmpeg · pyscenedetect  

---

## GitHub Stats

<p align="left">
  <img src="https://github-readme-stats.vercel.app/api?username=Ehsas317&show_icons=true&theme=dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=58a6ff&text_color=c9d1d9" height="150" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ehsas317&layout=compact&theme=dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9" height="150" />
</p>

---

## Currently Working On

- **Brain Loader v3** — Bug fixes, model compatibility (Qwen3, Llama 3.3), adaptive planning loop refinements
- Exploring **MLX quantization strategies** for fitting larger models on 16-32 GB systems
- Researching **multi-modal specialist routing** for the brain_loader architecture

---

## Philosophy

> *"The best AI is the one that runs on your hardware, with your data, under your control."*

I believe local-first AI isn't a compromise — it's a design choice that unlocks privacy, latency, and cost advantages cloud AI can't match. My work focuses on making local AI systems as capable and easy to use as their cloud counterparts.

---

<p align="center">
  <i>Built with obsession for clean architecture and zero-bloat systems.</i>
</p>
