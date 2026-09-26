# Project Context

Projects, goals, and status, most recent first. Two accounts are in play and are kept separate: **roadpiratefilms** (creative/media, roleplay tooling, hardware and signal work) and **tjbryant** (software engineering, character-card infrastructure, self-hosted systems).

---

## Account: roadpiratefilms

### Active and recent (2026)

- **PyTorch learning path** — *Goal, Sep 2026.* The user wants to learn PyTorch from basic to advanced level through hands-on lessons verified against real hardware.
- **TEIC-Agent** — *Project, Sep 2026.* An agentic chat architecture incorporating temporal, embodied, and interoceptive dynamics, with explicit criteria for assessing subjective experience. Active.
- **Drone/UAV build** — *Project, Sep 2026.* Autonomous flight, SDR capabilities, and bill-of-materials revisions. In progress.
- **SDR and signal work** — *Interest, Sep 2026.* RTL-SDR v4, HackRF One, and LimeSDR Mini hardware; detecting and logging signals around 1.6 GHz. Related: wardriving with Bluetooth and WiFi on Alpine Linux.
- **Adult media library analysis** — *Project, Sep 2026.* Maintaining a large adult video library and building incremental/cached analysis over it. Related earlier work: directory scanning, ffprobe metadata extraction, SQLite storage.
- **SillyTavern roleplay prompt engineering** — *Project, ongoing.* Building and refining roleplay prompts, including NSFW and character-card system prompts, plus detailed system prompts with trackers for scenes, time, relationships, secrets, events, status, achievements, inventory, and reputation.
- **NSFW/erotic roleplay tooling** — *Project, ongoing.* Prompts for erotic roleplay partners and NSFW image generation compatible with SillyTavern; explicit character cards for sexual roleplay, including taboo themes.
- **SillyTavern CLI/TUI reimplementation** — *Project, Aug 2026.* A Python CLI/TUI reimplementation of SillyTavern with staged, modular functionality.
- **SillyBunny** — *Project, Aug 2026.* A SillyTavern fork including an in-chat agent called Chatroom that generates audience-style reactions.
- **Character card production workflow** — *Project, Aug 2026.* A reusable system for producing professional-grade character cards from source material (transcripts, scripts, web research) via meta-prompts and templates.
- **AI video reimagining** — *Project, Aug 2026.* ComfyUI with Wan and LTX models, using free cloud options such as Google Colab.
- **Companion agent with sensor access** — *Project, Jul 2026.* A companion agent that runs alongside a character, shares context, and accesses the phone's webcam and other sensors.
- **Hidden-rule game prompts** — *Project, Aug 2026.* Prompts instructing an LLM to answer only yes/no, or to answer the opposite of correct, until a secret code word is given.
- **Web-based card management system** — *Planned, Jun 2026.* Vue.js front end, Node.js/Express back end, PostgreSQL, including relationship graphs.
- **Indie vehicle simulation game** — *Project, May 2026.* Granular, part-by-part mechanical simulation (engine, transmission, suspension, electrical) running in real time. A parallel Python/OpenGL/pygltflib driving sim loads glTF vehicle models.
- **AI music generation** — *Project, May 2026.* HeartMuLa model with CUDA. Earlier: a React DAW-styled prompt creator component calling the Anthropic API.
- **Device control via LLM tool calls** — *Project, May 2026.* LLM-driven applications giving an AI character tool-calling control over physical devices through a REST API (The Handy stroker).
- **AllTalk TTS integration** — *Project, May 2026.* AllTalk (XTTS v2 engine) integrated with SillyTavern as a TTS provider; run in Google Colab, with recurring loss of work on instance disconnects.
- **SillyTavern character-card tooling** — *Project, ongoing since 2025.* Custom prompts, in-chat agents, a TypeScript CLI pipeline for generating chara_card_v2 fields, and a card management project (cardproz/cardedit) for reading, editing, analyzing, and generating cards via LLM APIs.
- **Mr. Robot Show Bible** — *Project, mid-2026.* A comprehensive analytical Show Bible covering all four seasons, built with bash tooling over a large transcript file, organized into character arcs, world rules, plot chronology, dialogue motifs, and relationship maps.
- **Video summarization prompts** — *Recent work, May 2026.* System prompts accepting VTT and SRT captions and producing structured output (one-sentence overview, prose summary, bullet takeaways).

### Earlier (2025)

- **Multi-agent pipeline** — *Project, Oct 2025.* Multi-agent AI pipelines and agent harnesses, including `github.com/l0ophole/multi-agent-pipeline`.
- **CardDesigner** — *Project, Oct 2025.* A node-based character card designer with draggable nodes and data links, primarily in modern Python. Related: node-based editor tools in Python with PyQt6.
- **OpenRouter card analysis tool** — *Project, Oct 2025.* A Python tool using the OpenRouter API (deepseek-r1) to analyze and modify SillyTavern character cards.
- **Card format conversion** — *Project, Oct 2025.* Converting between chara_card_v2 and chara_card_v3 formats and using LLMs to analyze and enhance cards.
- **AI upscaling on Linux** — *Project, Oct 2025.* Real-ESRGAN and related tools for video/image upscaling.
- **NSFW roleplay cards and lorebooks** — *Project, Jul 2025.* Characters including Amber, Collie, Curzia, Zoey, and Vanessa; ongoing interest in lorebooks, SillyTavern extensions, and alternatives to SillyTavern.
- **The Handy integration** — *Interest/project, Nov–Dec 2025.* Programmatic control of The Handy automatic stroker via its local network API, integrated with SillyTavern character cards.

### Standing interests that shape projects

UAP/UFO disclosure (congressional hearings, the Varginha Brazil 1996 case, declassification, Skinwalker Ranch, the Mario Woods case, 3D physics simulations recreating incidents); AI consciousness, alignment, and whether LLMs behave differently when they know they are being tested; LLM internals (attention, recurrence, gradient monitoring); narrative point of view and prompting for specific POV styles; local and cloud TTS for SillyTavern; rooting and modifying network hardware; consciousness science (Global Workspace Theory, Active Inference).

---

## Account: tjbryant

### Active and recent (2026)

- **Model-fusion script** — *Project, Sep 2026.* A Python script that fuses responses from a panel of models judged by a selected judge model, similar to OpenRouter's fusion feature.
- **Agentic media-library system** — *Project, Sep 2026.* A media library with a custom system prompt and tooling.
- **Agent system prompt design** — *Project, Sep 2026.* Meta-prompts for synthesizing and adversarially reviewing agent system prompts; prompt engineering treated as a serious engineering discipline focused on reliability, safety, and behavior.
- **SillyTavern CLI/TUI (stcli)** — *Project, Aug–Sep 2026.* A Python CLI/TUI/REPL reimplementation of SillyTavern over a shared core, with staged modular functionality and Character Card V3 support. Driven from a project directory containing a SillyTavern clone and a generated repo map.
- **SillyTavern extensions and UI** — *Project, Aug 2026.* A draggable terminal-styled popup window for displaying messages; a browser extension/popup; a repo map of the SillyTavern codebase.
- **Agent framework skills** — *Project, Aug 2026.* Custom skills including personality customization and skill loading; work on self-improving skill infrastructure with trace logging, failure clustering, and reviewer-gated diffs.
- **Original character authoring process** — *Project, Aug 2026.* A Python dataclass schema and LLM-guided question flow for authoring original characters for roleplay.
- **chub.ai API library** — *Planned, Aug 2026.* A Python library for chub.ai API interaction.
- **Kara Canvas Pipeline** — *Project, Jul 2026.* A character-card generation system with a cascade function that auto-updates dependent fields, stored under a `.karaCanvasPipeline` directory as JSON session files. Related: SillyTavern worksheet mode and Kara Canvas.
- **Character card creation framework (V3)** — *Project, Jul 2026.* A framework targeting the V3 spec for programmatic, collaborative character creation workflows.
- **Agentic roleplay harness** — *Project, Jul 2026.* Uses OpenRouter for LLM inference and tool calling.
- **Shoplifting-detection proof of concept** — *Project, Jul 2026.* YOLOv8-pose with wrist-to-hip proximity heuristics and dwell-time tracking, batch evaluation scripts, and a pitch document prepared for internal presentation at the user's workplace.
- **Voice-enabled character pipeline** — *Project, Jul 2026.* CSM-1B TTS with a local server and a Colab-hosted cloud server; experimentation with speaker ID selection for female-sounding voices.
- **ALPM tooling** — *Project, Jul 2026.* Python tooling interfacing directly with the Arch Linux package manager library.
- **Character card version control** — *Project, Jul 2026.* A file-watching daemon that monitors the SillyTavern character directory, maintains per-character git repos keyed by PNG filename stem, explodes card fields into markdown for clean diffs, and writes commit-log manifests.
- **Card extractor / PNG tooling** — *Project, Jun–Jul 2026.* Extracting embedded card JSON from PNG tEXt chunks with V2/V3 spec detection.
- **AI image generation pipelines** — *Project, Jun 2026.* Refining a character's face across reference images and varying lighting and pose; ComfyUI with SD1.5, IP-Adapter, and ControlNet OpenPose on Colab, with LoRA training as the end goal.
- **Media library and download automation** — *Project, Jun 2026.* yt-dlp, mpv, qBittorrent-nox, and an OpenVPN network namespace on Alpine Linux. Related: a curses-based yt-dlp download queue manager with mpv integration and a media library browser.
- **YouTube channel analysis pipeline** — *Project, Jun 2026.* A Python multi-pass pipeline using yt-dlp and OpenRouter (via `requests`, not the `openai` library) with six specialist passes — Performance Analyst, Content Strategist, SEO Specialist, Monetization Advisor, New Content Direction, and Synthesizer — plus an owner Q&A intake step. Two reports generated; a meta-analysis identified prompt-level fixes still to implement.
- **Vehicle simulation game** — *Project, May 2026.* A Python realistic vehicle simulation using ModernGL and GLFW on Linux/PC, developed through a structured multi-phase plan (pre-production, prototyping, production, testing). Related: engine simulation work covering RPM, throttle, fuel consumption, and engine audio realism.
- **Programmatic video analysis** — *Project, May 2026.* Face detection, extraction, and alignment in Python using face_recognition/dlib.
- **Character design assets** — *Project, May 2026.* Character bibles, consistency anchor sheets, and AI video scene scripts.
- **Console LLM harness** — *Project, May 2026.* A custom console-based Python LLM harness using the OpenRouter API, slash commands, Claude-spec skills, and SQLite-stored system prompts. Related: multi-worker streaming LLM clients with per-worker output panes.
- **Character card node editor** — *Project, May 2026.* Located at `/rpf/chara-node-editor`.
- **UAP document scraping** — *Project, May 2026.* Scraping public UAP/UFO document releases, including PDFs, images, and video.
- **Roleplay LLM training** — *Project, Apr 2026.* Training a roleplay LLM with reinforcement learning (DPO) and exporting to 4-bit GGUF.
- **Android character card viewer/editor** — *Project, Apr 2026.* Kotlin, built from the Arch Linux console.
- **LLM agent applications** — *Project, Apr 2026.* Python applications using the OpenRouter API with multi-agent orchestration, PyQt6 GUIs, and git integration.
- **Quake II modding** — *Interest/project, Apr 2026.* Modifying Quake II source code to add vehicles and turrets.
- **Character card viewer/editor** — *Project, Feb 2026.* A tool that opens SillyTavern/TavernAI-compatible cards from JSON or PNG, working both in a Linux console and as a PyQt6 GUI.
- **yt-dlp download queue manager** — *Project, Feb 2026.* A curses-based queue manager with mpv player integration and a media library browser.

### Earlier (2025)

- **LLM-assisted code tooling** — *Project, Nov 2025.* A Python script for LLM-assisted code writing, analysis, and refinement with filesystem access tools.
- **Multi-LLM comparison repo** — *Project, Oct 2025.* `l0ophole/llm_prompts`, comparing responses from multiple LLMs to the same prompt.
- **Sequential agent card pipeline** — *Project, Oct 2025.* A Python AI agents pipeline that loads and refines character cards through sequential agents.
- **chara_card_v2 authoring** — *Project, Oct 2025.* Building cards in chara_card_v2 JSON format and loading/testing them in SillyTavern.
- **Multi-machine audio streaming** — *Project, Oct 2025.* Streaming audio between hosts on a multi-machine home setup.
- **Python game development** — *Project, Jun 2025.* moderngl-based game work, including a first-person shooter project.

### Standing interests that shape projects

UAP/UFO and non-human intelligence research, including the 2004 Nimitz and GIMBAL/GOFAST encounters, the Mario Woods case, the Jake Barber and Skywatcher topic, Schumann resonance, and source-critical analysis of abduction/contact literature; consciousness research (qualia, the hard problem, whether current AI architectures could be conscious); neuromorphic computing and spiking neural networks; simulation theory and remote viewing; software engineering practices including TDD, BDD, CI/CD, and agentic coding harnesses; x86_64 assembly on Linux (System V ABI, syscalls, shared objects) and low-level performance benchmarking; computer graphics programming including software rasterization; graphrag for repository and source-code management; hardware accelerators with large unified memory as an alternative to high-VRAM GPUs; AI companion and character-card setups including RAG/vector memory; adult-themed and romantic/sexual AI character roleplay and the architectures that support it; AI image generation for characters, including recurring characters used across roleplay and image/video work; TTS options and running them in Colab; forensic persona analysis and digital archaeology from IRC logs and similar data.

### Goals

- Move the YouTube channel in a new content direction rather than continuing the current type of content, with monetization as the primary objective.
- Record and save transcripts of AI voice conversations for later review.
- Create a PC video game as an independent developer, using LLM-guided phased development workflows.

---

## Cross-account notes

- Both accounts converge on the same core domain: character cards, SillyTavern, prompt engineering, and the tooling layer beneath them. The roadpiratefilms account leans toward creative/media production and hardware; the tjbryant account leans toward software engineering, version control, testing, and self-hosted infrastructure.
- Recurring working pattern on both accounts: the user states the full technical stack and constraints up front, prefers a plan approved before implementation, asks for targeted diffs rather than full-file rewrites, and iterates through repeated revision requests.
- Recurring infrastructure pattern: the user prefers local, self-hosted processing and storage over cloud services, and builds pipelines to extract and consolidate data he already owns.
