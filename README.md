<div align="center">

# Mustafa Kemal Aydın

### AI Systems Engineer — Rust • .NET • Local LLM • Speech AI • Edge Inference

I build AI systems that run as complete products, not notebook experiments:
Rust cores, desktop agents, .NET services, and inference on commodity hardware.

<p>
<a href="https://github.com/mkaydin">
<img src="https://komarev.com/ghpvc/?username=mkaydin&style=flat-square" alt="Profile views"/>
</a>
</p>

</div>

<p align="center">
<img height="165" src="https://github-readme-stats.vercel.app/api?username=mkaydin&amp;show_icons=true&amp;hide=prs,issues,contribs&amp;border_radius=10&amp;hide_border=true" alt="GitHub stats — stars earned and commits in the last year"/>
</p>

---

## About

I like the part of AI engineering that happens after the model works: streaming
it to a user, remembering what mattered, keeping it honest, and shipping it on a
machine that has to actually run.

Most of my work lives at the seam between **language models**, **real-time
systems**, and **constrained hardware** — local-first inference, speech
pipelines, retrieval and knowledge graphs, and backends that hold up under load.
I reach for Rust where latency and predictability matter, and .NET where
shipping a maintainable service matters.

Current focus: local agentic systems, Turkish speech recognition, graph-shaped
memory, and edge inference on single-board computers.

---

## Featured Work

### 🧠 [Ayla](https://github.com/mkaydin/Ayla) — Local AI coworker with knowledge memory

Desktop AI coworker for conversation, research, document processing, and
long-term knowledge. A Tauri-independent Rust core is exposed to an Electron
host over a private MessagePack sidecar; Tauri stays as a compatibility host.

- Streaming Ollama chat with cancellable responses and local/cloud model choice
- Partial-stream TTS (Sherpa-ONNX / Piper) that starts speaking before the
  response finishes, filtering Markdown, code, equations, and tables out of speech
- Persistent memory: Qdrant vectors, a `petgraph` knowledge graph, SurrealDB for
  research results, and an approval step before anything enters the KB
- In-process PDF/OCR (pdfium-bundled), SearXNG + Lightpanda meta search, and a
  Live2D Mk6 avatar with lip sync and process-aware posing

### ⚖️ [Council of Minds](https://github.com/mkaydin/COM) — Multi-agent deliberation system

Specialized agents with distinct reasoning styles debate a question in parallel;
a Moderator turns their arguments into a decision space and a critique round
resolves real disagreements. Python/FastAPI backend, Electron or browser client.

- Router classifies the query into Oracle (OKF bundle), Scholar (RAG retrieval),
  or Sage (LLM wiki)
- Alignment, conflict detection, and a hold / revise / concede critique loop
- Argument archive and a persistent agent-profile library

### ⚡ [fast-then-slow](https://github.com/mkaydin/fast-then-slow) — Two-tier local inference

System 1 is a single non-autoregressive forward pass that answers typed decision
questions in **~28 ms** and never writes text — so there is nothing to parse and
nothing to hallucinate. System 2 is Qwen3.5-9B int4 on vLLM.

- The fast model decides *whether* to generate, *how much* deliberation is
  deserved, and *whether to trust* the result
- Verifier verdicts: ship, escalate once, or hand off to a human
- Measured on RTX 5060 Ti 16 GB (System 2) + RTX 4060 8 GB (System 1):
  27.8 ms median gate, ~44 tok/s decode

### 🕸️ [GCML](https://github.com/mkaydin/GCLM) — Graph Context Language Model

Research prototype replacing "keep appending history to the prompt" with a
structured context pair: a bounded token window `T` plus persistent graph memory
`G` holding entities, facts, relations, supersession history, and provenance.

- Facts update by supersession instead of erasure; exact stored values can be
  emitted by pointer rather than regenerated from weights
- Unknown facts route to abstention instead of plausible invention
- Currently migrating the from-scratch 515M TinyStories backbone to pretrained
  SmolLM2-360M, with the original path kept as a baseline

### 🔎 [PaperSearchEngine](https://github.com/mkaydin/PaperSearchEngine) — Scientific literature meta-search

SearXNG across 8 engines, Lightpanda for JavaScript rendering, and Ollama for
paper analysis. Concurrent PDF download, full-text extraction, relevance
scoring, and structured literature-review reports.

### 🎧 [Ayla speech modules](https://github.com/mkaydin/ayla_stt_test_module) · [TTS](https://github.com/mkaydin/ayla_tts_test_module)

Packaged Turkish STT (Omnilingual 300M CTC via `sherpa-onnx`; FP32 on CUDA, INT8
on CPU) and the matching TTS path used by Ayla.

---

## More Projects

| Project | What it is |
| --- | --- |
| [customer_support_ticket_system](https://github.com/mkaydin/customer_support_ticket_system) | LLM-assisted support desk — ASP.NET Core 9 + EF Core (Oracle) + JWT, React/TypeScript/Vite/Tailwind frontend, MCP features |
| [kb_ready_code_doc](https://github.com/mkaydin/kb_ready_code_doc) | Rust crate/CLI turning a file, directory, or repo into human docs *and* a machine-parseable `.kb.md` graph document (stable UIDs, typed relations, provenance) |
| [glm_ocr_tests](https://github.com/mkaydin/glm_ocr_tests) | OCR CLI tool for the Ayla pipeline |
| [alert_analyze_system](https://github.com/mkaydin/alert_analyze_system) | Firewall / Defender log analysis and reporting |
| [pilab_containers](https://github.com/mkaydin/pilab_containers) | Container management automation for Raspberry Pi OS and Linux hosts |
| [esp32_pc_starter_relay](https://github.com/mkaydin/esp32_pc_starter_relay) | ESP32-S2 mini + TFT PC power/status indicator |
| [E-imza-DIY](https://github.com/mkaydin/E-imza-DIY) | Hardware-backed document/data signing experiment |
| [Insect-Detection-NN-Rust](https://github.com/mkaydin/Insect-Detection-NN-Rust) | CNN training in Rust (`tch` + `ndarray`) on insect imagery |
| [little_rust_ml](https://github.com/mkaydin/little_rust_ml) · [opencv-rust-tests](https://github.com/mkaydin/opencv-rust-tests) | Hand-written ML framework, MNIST CNNs, and computer-vision experiments |
| [E-Imam](https://github.com/mkaydin/E-Imam) | React Native / Expo + NativeWind mobile app |

---

## Stack

### Languages

<p>
<img src="https://skillicons.dev/icons?i=rust,cs,cpp,python,ts,js,go" alt="Rust, C#, C++, Python, TypeScript, JavaScript, Go"/>
</p>

### Desktop, Frontend & Backend

<p>
<img src="https://skillicons.dev/icons?i=dotnet,electron,tauri,react,svelte,actix,fastapi" alt=".NET, Electron, Tauri, React, Svelte, Actix, FastAPI"/>
</p>

### Infrastructure

<p>
<img src="https://skillicons.dev/icons?i=docker,linux,github,git,ansible,raspberrypi" alt="Docker, Linux, GitHub, Git, Ansible, Raspberry Pi"/>
</p>

**AI & inference:** Ollama · vLLM · sherpa-onnx (Piper TTS, Omnilingual CTC ASR) ·
ONNX · HuggingFace Transformers · Qdrant · RAG · knowledge graphs

**Backend & data:** ASP.NET Core · EF Core · Oracle · FastAPI · Actix Web ·
SurrealDB · MessagePack sidecars · JWT

**Systems:** tokio · async Rust · Docker Compose · Raspberry Pi · ESP32 ·
embedded Linux · SearXNG

---

## How I Work

> Build software that is fast, local, reliable, and useful.

- **Measure, don't guess** — every latency and throughput number in this README
  came from a run on my own hardware.
- **Local first** — inference on hardware you control, with graceful hand-off to
  a human or the cloud when confidence is low.
- **Finish the system** — memory, retrieval, OCR, and voice are not side quests;
  they're what makes an assistant usable.

---

<p align="center">

<a href="https://github.com/mkaydin?tab=repositories"><img src="https://img.shields.io/badge/all_repositories-181717?style=flat-square&amp;logo=github&amp;logoColor=white" alt="All repositories"/></a>
<a href="https://github.com/mkaydin/Ayla"><img src="https://img.shields.io/badge/Ayla-Rust%20%2B%20Electron-181717?style=flat-square&amp;logo=rust&amp;logoColor=white" alt="Ayla"/></a>
<img src="https://img.shields.io/badge/Open%20Source-Rust%20%C2%B7%20Linux%20%C2%B7%20AI-181717?style=flat-square" alt="Open source"/>

</p>