# Ehsas Sethi

**Local-First AI Systems · Apple Silicon · Python Architecture**

```
Born: 3 Jan 2007 · Abohar, Punjab, India
Studying: B.E. Computer Engineering, Thapar Institute (TIET), Patiala — Batch of 2030
Email: ehsassethi@gmail.com
LinkedIn: linkedin.com/in/ehsassethi
```

A small-town kid from Abohar with a deep obsession for clean architecture,
zero-bloat systems, and making AI run where it matters most — on your own
hardware, with your data, under your control.

I build agentic AI orchestration systems that run entirely on local hardware.
No cloud dependencies, no API keys, no data leaving your machine.
Just pure silicon doing intelligent work.

---

## Connect with me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/ehsassethi)

---

## The Evolution of the AI Build Engine

The AI Build Engine is my main project — an orchestration framework I've been
iterating on through 6 major versions. Each version represents a distinct
architectural philosophy:

### [mesh](https://github.com/Ehsas317/brain-loader-v6) — Visual Mesh (Latest)

A no-code AI orchestration platform using Docker, Ollama, Dify, and open-source tools.
The convergence of everything learned across 6 versions into a visual, distributed mesh.

- **6-layer Docker stack**: Ollama, Dify, PostgreSQL, Redis, Weaviate, n8n
- **Universal Bot Gateway**: WhatsApp, Telegram, Discord integration
- **Visual workflow builder**: Dify for no-code AI pipeline construction
- **Custom Ollama personas**: Brain Planner, Coder, Critic, Researcher
- **One-command setup**: `bash install.sh` deploys entire mesh
- **Wave execution engine**: YAML-defined task waves with parallel dispatch
- **Vector database**: Weaviate for semantic search and RAG
- **Hybrid execution**: Local MLX/Ollama + Cloud APIs with auto-failover

```yaml
Architecture:  Docker Mesh + Dify Visual Workflows + Ollama Personas
Stack:         Ollama, Dify, n8n, PostgreSQL, Redis, Weaviate
Interfaces:    Web UI (Dify) + Bot Gateway (WhatsApp/Telegram/Discord)
Deployment:    Docker Compose
License:       MIT
```

---

### [ladder](https://github.com/Ehsas317/brain-loader-v5) — Lazy Conductor

The convergence of everything learned across 5 versions. Combines the
**Ponytail minimal-code philosophy** with **Trio structured concurrency** to
build the most efficient orchestrator yet.

- **5-rung Ponytail Decision Ladder** skips unnecessary work before dispatching
  any specialists — saves 40-70% on API costs
- **Trio nurseries** guarantee zero orphaned tasks, clean Ctrl+C shutdown,
  and proper exception groups (no more `asyncio` gotchas)
- **8 backends**: Anthropic, OpenAI, OpenRouter, Groq, Gemini, DeepSeek,
  MLX (Apple Silicon), Ollama (any OS)
- **Per-role provider chains** with circuit breakers and auto-failover
- **Cost tracking** with budget warnings at 85% and hard stops at the limit
- **Terminal-native REPL** with Rich UI, live task tables, and HITL approval
- **httpx-native** — zero SDK dependencies, all HTTP through one async client
- 3 execution modes: `local` (zero cost), `api` (maximum speed), `hybrid` (best balance)

```yaml
Architecture:  Ponytail Decision Ladder + Trio Wave Engine
Concurrency:   Trio structured concurrency (nurseries, cancel scopes)
Backends:      6 cloud providers + MLX + Ollama
Models:        Qwen3-32B, Qwen2.5-Coder, Llama-3.3-70B, Claude, GPT-4o
Savings:       40-70% API cost reduction via Ponytail ladder
License:       MIT
```

---

### [surge](https://github.com/Ehsas317/brain-loader-v4) — Multi-Backend Orchestrator

Where the engine went from local-only to hybrid cloud+local. The big shift
from sequential to **wave-based parallel dispatch**.

- **Wave Engine**: Brain plans a wave of 2-5 parallel tasks instead of
  sequential 30-80 task lists
- **Universal Router** with per-role provider chains: coder, researcher,
  writer, math, critic each get their own failover sequence
- **Circuit breaker pattern** per provider (Closed/Open/Half-Open states)
- **Rich terminal REPL** with live task tables, `/status`, `/cost`, `/memory` commands
- **Human-in-the-loop approval** for every wave
- Full async architecture with `asyncio` + `aiohttp`

```yaml
Architecture:  Wave-based parallel dispatch + Universal Router
Backends:      MLX + Ollama + Anthropic + OpenAI + OpenRouter + Groq + DeepSeek + Google
Concurrency:   asyncio + aiohttp (fully async)
License:       MIT
```

---

### [port](https://github.com/Ehsas317/brain-loader-v3) — Portable Local Orchestrator

The breakthrough: replacing the coordinator LLM with **pure Python**.
This freed ~4GB of RAM for the KV cache — the difference between fitting a
32B model and not.

- **Pure Python coordinator** handles all routing, state, memory, and parsing
  with zero LLM overhead
- **Single hot-swap model slot**: only one model in RAM at a time
- **MLX backend** for Apple Silicon + **Ollama backend** for any system
- **Adaptive planning loop**: Brain reads real output and adapts after every task
- **Deterministic regex parsing** instead of LLM coordination — zero hallucination
- **memory.md** as constant-size persistent state (completed subtasks deleted,
  only current task's subtasks exist)
- Crash recovery via atomic writes + `state.json`
- Resume capability with constraint restoration

```yaml
Architecture:  Pure Python coordinator + single hot-swap model slot
Backends:      MLX (Apple Silicon), Ollama (universal)
Models:        Qwen3-32B, Qwen2.5-Coder-32B, Llama-3.3-70B
RAM Layout:   ~0 GB coordinator + 20-24 GB active model + 3-4 GB system
License:       MIT
```

---

### [relay](https://github.com/Ehsas317/brain-loader-v2) — Sequential Orchestration

The coordinator-as-resident-model architecture. A small coordinator LLM
stays permanently loaded, managing the hot-swap of larger brain and
specialist models.

- **Permanent coordinator** (~1.5B params, ~4GB) never unloads — manages
  all model loading/unloading
- **Brain model** (32B Q4, ~20GB) hot-swapped for planning and adaptation
- **Specialist models** hot-swapped for execution — coder, researcher,
  writer, debugger, math, critic
- **memory.md** with constant file size throughout the entire run
- **Stateless brain, stateful system** — all state lives in `memory.md`
- Atomic writes for crash recovery
- Built for overnight runs with 50+ tasks on MacBook Pro M1 Max

```yaml
Architecture:  Resident coordinator + hot-swap brain/specialists
Coordinator:   Qwen2.5-1.5B-Instruct (~4 GB permanent)
Brain:         Qwen3-32B-4bit (~20 GB hot-swap)
Specialists:   Coder, Researcher, Writer, Debugger, Math, Critic
Peak RAM:      24 GB hard ceiling (4 GB coord + 20 GB hot-swap)
License:       MIT
```

---

### [forge](https://github.com/Ehsas317/brain-loader) — The Original (v1)

Where it all started. A Brain LLM (8B) plans complex projects, delegates to
specialized worker models (15B/7B), and iteratively reviews their work until
production quality — all running locally on Apple Silicon.

- **Brain** (Llama 3.1 8B) creates master plans of 30-80 tasks
- **Workers** (Nemotron-4 15B, CodeLlama 7B, DeepSeek Coder 6.7B) execute tasks
- **Iterative review**: Brain rates worker output 1-10, creates remediation
  tasks for anything below 6
- **Model hot-swapping**: only one model in RAM at a time
- **Telegram notifications** for project milestones
- Final review with up to 5 iterations before declaring `PROJECT_COMPLETE`

```yaml
Architecture:  Brain + Worker loop with iterative review
Backends:      MLX (Apple Silicon)
Models:        Llama-3.1-8B (brain), Nemotron-4-15B, CodeLlama-7B, DeepSeek-Coder-6.7B
RAM Budget:    25 GB of 32 GB system
License:       MIT
```

---

## [Trio](https://github.com/Ehsas317/trio) — Personal AI Ecosystem

Three specialized AI assistants sharing a unified core framework and vector
database knowledge base, running on a Mac Mini M4.

| Assistant | Name | Role |
|-----------|------|------|
| **NAMI** | Network and Machine Intelligence | Telegram bot for system control, monitoring, and remote command execution |
| **RUSH** | Recording and Understanding Speech Helper | Audio transcription via whisper.cpp (Metal-accelerated) + Ollama summarization |
| **VEX** | Video Exploration Helper | Scene detection via PySceneDetect + ffmpeg automated clip extraction |

- **Shared ChromaDB vector store** for cross-assistant knowledge sharing
- **Unified core framework**: state manager, memory manager, checkpoint
  manager, controller, vector store
- **Flask dashboard** for real-time monitoring of all assistants
- **launchd integration** for macOS auto-start on boot
- Modern Python packaging with `pyproject.toml`, type hints, `pathlib`
- Entry-point CLI commands: `trio-nami`, `trio-rush`, `trio-vex`, `trio-dashboard`

```yaml
Platform:     macOS (Apple Silicon)
Inference:    Ollama (local LLMs), whisper.cpp (Metal)
Vector DB:    ChromaDB with cross-assistant knowledge sharing
Interface:    Telegram bot + Flask web dashboard
Scheduling:   launchd (macOS)
License:      MIT
```

---

## Other Projects

### [github-repo-finder](https://github.com/Ehsas317/github-repo-finder) — Production-Grade GitHub Repo Finder

A project designed to build a **production-grade GitHub Repo Finder** that can be used as a Claude Skill, ChatGPT Skill, MCP Server, Standalone CLI, Python package, and API component. The system helps LLMs discover the best GitHub repositories while minimizing token usage and maximizing reliability.

- **GitHub Search**: Advanced searching capabilities using GitHub's API.
- **Ranking Engine**: A sophisticated ranking algorithm to score repositories based on various metrics.
- **Token Optimization**: Strategies to minimize token usage for LLM interactions.
- **Trending Repositories**: Identification of currently trending and viral repositories.
- **Filtering**: Comprehensive filtering options by language, date, stars, and license.
- **Scoring**: Maintenance score, repository health score, activity score, popularity score, freshness score, and a final weighted ranking.

---

## Technical DNA

```
Local-First AI Architecture
  Model orchestration & hot-swapping at the RAM level
  RAM-aware scheduling on memory-constrained hardware
  Deterministic coordination (pure Python over LLM bloat)
  Apple Silicon optimization (MLX framework, Metal GPU)
  Structured concurrency (Trio nurseries over asyncio fire-and-forget)
  Docker containerization for distributed deployment
  No-code AI workflow integration (Dify, n8n)
  Vector search and RAG pipelines (Weaviate, ChromaDB)

Systems Programming
  Pure Python state machines and event loops
  Async I/O & process lifecycle management
  Vector embeddings & semantic search (ChromaDB, Weaviate)
  Event-driven assistant architectures
  Circuit breaker patterns & graceful degradation
  Shell scripting for automated deployment

Python Tooling
  Modern packaging (pyproject.toml, setuptools)
  Type hints & static analysis (mypy)
  YAML/JSON configuration systems
  API design (Flask, Telegram bots, httpx)
  Regex-based deterministic parsing pipelines
```

---

## Stack

**Languages:** Python 3.11+ · YAML · Shell · Bash  
**AI/ML:** MLX · Ollama · ChromaDB · Weaviate · Whisper.cpp · sentence-transformers  
**Systems:** Docker · launchd · asyncio · Trio · multiprocessing · psutil  
**Web:** Flask · Dify · python-telegram-bot · httpx · n8n  
**Tools:** Git · Homebrew · ffmpeg · pyscenedetect · Rich  

---

## GitHub Stats

<p align="left">
  <img src="https://github-readme-stats.vercel.app/api?username=Ehsas317&show_icons=true&theme=dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=58a6ff&text_color=c9d1d9" height="150" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Ehsas317&layout=compact&theme=dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9" height="150" />
</p>

---

## Philosophy

> *"The best AI is the one that runs on your hardware, with your data,
> under your control."*

I believe local-first AI isn't a compromise — it is a design choice that
unlocks privacy, latency, and cost advantages cloud AI can't match. Every
version of the engine has been a step toward making local AI systems as
capable and easy to use as their cloud counterparts, while using a fraction
of the resources.

---

<p align="center">
  <i>Built with obsession for clean architecture and zero-bloat systems.</i>
  <br><br>
  <a href="mailto:ehsassethi@gmail.com">ehsassethi@gmail.com</a>
  <br>
  <a href="https://linkedin.com/in/ehsassethi">Connect on LinkedIn</a>
</p>
