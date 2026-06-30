# Ehsas317: AI Systems Architect

AI Systems Architect specializing in **Local-First AI & Multi-Agent Orchestration**, with a strong focus on optimizing performance for **Apple Silicon (MLX)**. My work centers around building robust, efficient, and intelligent systems that empower developers and users with advanced AI capabilities directly on their hardware.

---

## Featured Projects

### Brain Loader Series: Multi-Backend Agentic AI Orchestration

The `Brain Loader` series represents an evolving exploration into sophisticated AI orchestration, designed for hardware-aware, agentic systems. Each iteration builds upon the last, pushing the boundaries of local AI capabilities and multi-agent coordination.

*   **Brain Loader v6 (Mesh)**: The latest iteration, focusing on a **Visual Mesh + Universal Bot Gateway**. This no-code AI orchestration platform leverages Docker, Ollama, Dify, and other open-source tools to create a seamless visual workflow for AI agents.
*   **Brain Loader v5**: Introduces the **Lazy Conductor Architecture**, a multi-backend AI orchestration system built with a 
Ponytail minimal-code philosophy and Trio structured concurrency. It supports local MLX/Ollama and Cloud APIs with auto-failover.
*   **Brain Loader v4**: A multi-backend agentic AI orchestrator featuring local MLX, local Ollama, Cloud API integration, hybrid parallel execution, auto-failover, and a terminal-native REPL.
*   **Brain Loader v3**: A portable, hardware-aware agentic AI orchestration system with a pure Python coordinator, single hot-swap model slot, and adaptive planning loop. Targets Apple Silicon via MLX and includes an Ollama backend.
*   **Brain Loader v2**: Focuses on a Sequential Orchestration Architecture for Apple Silicon, utilizing a 4GB permanent coordinator and a 20GB hot-swap slot for brain and specialists.
*   **Brain Loader v1 (brain-loader)**: An MLX Multi-Agent Orchestrator for Apple Silicon, where a Brain LLM plans projects, delegates to worker models, and iteratively reviews until production quality.

### [Trio](https://github.com/Ehsas317/trio) — Personal AI Ecosystem

A comprehensive AI ecosystem designed for Mac Mini M4, featuring three specialized AI assistants (NAMI, RUSH, VEX) that share a unified core framework and a vector database for knowledge sharing. It includes a web dashboard for real-time monitoring.

| Assistant | Name | Role |
|-----------|------|------|
| **NAMI** | Network and Machine Intelligence | Telegram bot for system control, monitoring, and remote command execution |
| **RUSH** | Recording and Understanding Speech Helper | Audio transcription via whisper.cpp (Metal-accelerated) + Ollama summarization |
| **VEX** | Video Exploration Helper | Scene detection via PySceneDetect + ffmpeg automated clip extraction |

Key features include a shared ChromaDB vector store, a unified core framework with state, memory, and checkpoint managers, a Flask dashboard, and `launchd` integration for macOS auto-start.

### [GitHub Repo Skill](https://github.com/Ehsas317/github-repo-skill) — Repository Composition Engine

An evolution of the original GitHub Repo Finder, this skill is designed to help build complex projects faster by discovering, evaluating, and generating blueprints to combine existing open-source tools with minimal custom code. It features an advanced scoring engine, an automated recipe builder, and AI-agent optimization for token efficiency.

| Feature | Original "Github Repo Finder" | New "Github-Repo-Skill" |
| :--- | :--- | :--- |
| **Primary Goal** | Finding a single useful repo. | **Building a full system** by combining repos. |
| **Search Intelligence** | Keyword-based. | **Task-to-Capability mapping.** |
| **Scoring** | Star count. | **Multi-dimensional health scoring.** |
| **Output** | List of links. | **Architectural blueprints (Recipes).** |
| **Comparison** | Manual. | **Automated side-by-side analysis.** |
| **Bug Status** | Unknown. | **Fully Debugged & API Verified.** |

---

## Technical DNA

My technical expertise is rooted in a **Local-First AI Architecture**, emphasizing:

*   **Model orchestration & hot-swapping** at the RAM level.
*   **RAM-aware scheduling** on memory-constrained hardware.
*   **Deterministic coordination** (pure Python over LLM bloat).
*   **Apple Silicon optimization** (MLX framework, Metal GPU).
*   **Structured concurrency** (Trio nurseries over asyncio fire-and-forget).
*   **Docker containerization** for distributed deployment.
*   **No-code AI workflow integration** (Dify, n8n).
*   **Vector search and RAG pipelines** (Weaviate, ChromaDB).

In **Systems Programming**, I focus on:

*   Pure Python state machines and event loops.
*   Async I/O & process lifecycle management.
*   Vector embeddings & semantic search (ChromaDB, Weaviate).
*   Event-driven assistant architectures.
*   Circuit breaker patterns & graceful degradation.
*   Shell scripting for automated deployment.

My **Python Tooling** practices include:

*   Modern packaging (`pyproject.toml`, `setuptools`).
*   Type hints & static analysis (`mypy`).
*   YAML/JSON configuration systems.
*   API design (Flask, Telegram bots, `httpx`).
*   Regex-based deterministic parsing pipelines.

---

## Stack

**Languages:** Python 3.11+ · YAML · Shell · Bash  
**AI/ML:** MLX · Ollama · ChromaDB · Weaviate · Whisper.cpp · `sentence-transformers`  
**Systems:** Docker · `launchd` · `asyncio` · Trio · `multiprocessing` · `psutil`  
**Web:** Flask · Dify · `python-telegram-bot` · `httpx` · `n8n`  
**Tools:** Git · Homebrew · `ffmpeg` · `pyscenedetect` · Rich  

---

## Philosophy

> *"The best AI is the one that runs on your hardware, with your data, under your control."*

I believe local-first AI isn't a compromise — it is a design choice that unlocks privacy, latency, and cost advantages cloud AI can't match. Every version of the engine has been a step toward making local AI systems as capable and easy to use as their cloud counterparts, while using a fraction of the resources.

---

<p align="center">
  <i>Built with obsession for clean architecture and zero-bloat systems.</i>
  <br><br>
  <a href="mailto:ehsassethi@gmail.com">ehsassethi@gmail.com</a>
  <br>
  <a href="https://linkedin.com/in/ehsassethi">Connect on LinkedIn</a>
</p>
