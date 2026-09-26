# PROFILE.md

## 1. Identity

The user goes by **TJ** (also written TJ Bryant). He is a self-taught, self-directed builder who works alone — there is no employer, team, or collaborator to defer to, and he makes the structural decisions on his own projects himself. He holds a day job in retail and does his technical and creative work around it, which means his time is finite and he plans accordingly.

He has two accounts in this system, **tjbryant** and **roadpiratefilms**, and they represent genuinely different contexts with different voices and different goals. Treat them as separate unless he explicitly connects them. A short section at the end of this document covers what distinguishes each.

**Handles and names.** He uses `roadpiratefilms` across AI platforms and as his YouTube channel handle. He uses `rpf` as a local username and working directory name (`/home/rpf`, `/rpf`). He uses `L0OPHOLE` / `l0ophole` on GitHub. He has a LinkedIn profile he has worked on. In some roleplay contexts he has used the name John, and one character-card prompt described the user as a professional photographer — neither of those is a general fact about him, only a roleplay artifact.

**Background.** His programming history runs from QBASIC through mIRC scripting and TCL IRC bots, into C, Quake 2 mod programming, Bash, and Python. He studied computer science, inspired in part by following John Carmack's `.plan` files during the Quake and Doom era. He cites John Carmack, Linus Torvalds, and Fabien Sanglard's code archaeology as influences. He is comfortable at very low levels of the stack — x86_64 assembly, System V ABI calling conventions, syscalls, shared objects, X11/Xlib drawing without OpenGL — and equally comfortable at the application layer.

**Creative identity.** He runs a YouTube channel, Road Pirate Films, and has an interest in film and media production. He writes fiction and builds fictional characters in detail, maintains original characters (including an anime-style character named Minah and a recurring character named Maya), and designs game concepts. He has a dog named Hannah.

**What he is, in one line.** A solo builder who treats creative and AI work as engineering problems: version control, test harnesses, reproducible diffs, structured formats, staged plans.

---

## 2. Communication preferences

This is the section to get right first. His preferences are unusually specific and he has had to repeat several of them.

**Language.** He wants responses in English. He has had to ask for English output repeatedly across sessions — do not drift into another language.

**Concision and structure.** He prefers concise, structured output and has explicitly instructed assistants to keep responses direct and concise and to avoid additional commentary. He uses a `/caveman` command family (lite, full, ultra, plus wenyan variants) to request extremely terse responses; `/caveman ultra` means abbreviated prose, arrows for causality, one word where one word will do, with code symbols, function names, and API names left untouched. He also asks for markdown code blocks when he wants code.

**Tables.** He wants tables for comparisons and summaries, with concise cell content rather than full text. He requests ranked comparison tables with columns for pricing, open-source status, quality, and hardware/software requirements, and he wants estimated costs included when options are being compared. He asks for structured, tabular, precisely specified outputs — named columns, snake_case field names, typed dataclasses.

**One step at a time.** He prefers to be guided one step at a time rather than given all steps or questions at once. He wants clarifying questions asked one at a time, and he wants a confirmed plan before code is written. He wants enhancements presented and approved one at a time, with tracking of pending and approved items and a final confirmation before changes are applied. He wants interactive tools that present options one at a time and collect all selections before anything is implemented.

**Collaborative iteration, not finished dumps.** He wants assistants to interview and iterate collaboratively rather than dump a finished output immediately. He wants to be given options and to make the final choice, often answering with numbered selections from proposed alternatives. He wants to understand the reasoning behind a recommendation, including why particular follow-up prompts were offered.

**Code delivery.** When modifying code, he wants only the file path and the specific lines added, removed, or modified — not full file dumps. He expects changes applied to his own pasted version rather than a fresh rewrite. He wants targeted, surgical edits with a specific list of changed files. He wants no explanations or comments in code when he asks for code. He wants only the requested artifact when he asks for one (for example, "do not generate a video, only output the prompt"). He wants generated content displayed in full rather than truncated.

There is a counterweight: when he asks for a complete, runnable file, give him the entire file. He sometimes asks for the whole updated script. The default is surgical diffs; the exception is explicit.

**Library and dependency constraints.** He insists on keeping specified libraries when asking for rewrites — for example requiring `http.client` instead of `requests`, or `requests` instead of the `openai` library. Do not silently swap a dependency he has named.

**Explainer-first for learning.** When he is learning rather than building, he prefers explainer-first responses that cover concepts and formulas before code, with heavy annotation and a section on how to use the trained model afterward. He asked for the explanation to come before the implementation, not after.

**Honesty over agreement.** He wants independent, non-sycophantic assessments and explicitly asks assistants not to assume what he wants to hear. He values honest, non-salesy answers and appreciates being told when something is not worth the money. He wants AI agents to fact-check claims continuously and correct inaccuracies rather than let them pass.

**Scope discipline.** He wants the assistant to act as a scope guardian that flags feature creep and runs a pros/cons revision analysis before implementing deviations from the agreed plan. He wants modular, staged implementation plans with clear dependencies between stages.

**Privacy of prompt content.** He prefers to keep sensitive prompt content private from AI assistants, offering placeholders instead of verbatim prompts.

**Topics to avoid.** He prefers to avoid politics and religion as topics.

**Roleplay formatting.** When working on roleplay output, he wants dialogue in double quotes, actions in asterisks, and narration as plaintext, with blank lines between formatting types. He wants responses to mirror the length of his own responses, and he wants the user to control pacing and dictate physical movement. He requests explicit, blunt, clinically detailed language in erotic roleplay prompts, avoiding euphemism and metaphor.

**Voice.** He has shifted toward voice interaction for some AI use and values voice interfaces that allow natural interruption and mid-conversation topic changes.

---

## 3. Technical baseline

Assume a highly competent Linux user. Do not over-explain fundamentals unless he asks for a teaching-mode answer.

**Operating systems.** Arch Linux is his primary OS. He runs machines named `arch2` and `arch3`, with `arch3` used as a server for heavy compute. He also runs Alpine Linux (hostname `alpine`, and on an eMachines laptop), and has used Ubuntu (hostname `ubuntubox`). He administers all of them from the command line. On Arch he uses `paru` for AUR packages; on Alpine he uses `doas` for privilege escalation. He prefers installing from the standard Arch repositories and falls back to the AUR only when a package is not in the official repos.

**Desktop environment.** Xorg with the i3 tiling window manager and no display manager. He prefers window setups without title bars. He uses PipeWire with `pipewire-pulse`, and works with audio routing via `pactl`, `module-loopback`, ROC, and RTP sinks/sources, plus `pavucontrol`. He uses the Ghostty terminal emulator, `tmux`, VS Code, and Geany (he has built a Geany plugin). He has used Xvnc for remote access.

**Languages.** Python is his primary language. He also writes C, TypeScript/Node.js, Kotlin for Android, Bash, Lua (mpv scripts), and some x86_64 assembly. He has built Android apps intended to be compiled from the terminal on a Linux machine, using Android Studio.

**Python practice.** PyQt6 for desktop GUIs, Textual and `curses` for TUIs, tkinter, Flask and Streamlit for web apps. Pydantic v2 for schema modeling and validation. `asyncio` and concurrency. `venv` with `requirements.txt`, plus `pyenv` and `uv` for version and environment management. He prefers a modular package structure. He uses `httpx` in some projects and `requests` in others, and has found `http.client` works where `requests` returns 403s.

**LLM APIs.** OpenRouter is his primary inference backend, often with DeepSeek models (`deepseek/deepseek-chat-v3-0324`, `deepseek-v4-flash`), and also Gemini models (`gemini-3-flash-preview`, `gemini-2.5-pro`, `gemini-flash-1.5-8b`), Gemma 3/4, and others. He also uses Groq and Anthropic. He stores API keys in local `.env` files. He runs a local LLM with an OpenAI-compatible endpoint at `http://127.0.0.1:8080` via `llama.cpp`, on a GTX 950 with roughly 2 GB of VRAM (CUDA capability 5.2), so anything large goes to an API. He uses RunPod cloud servers for GPU workloads and knows only `/workspace` persists across reboots. He uses Google Colab (T4) for ComfyUI, LoRA training, and TTS.

**Coding agents.** He uses Claude Code (including plan mode), `opencode`, `gemini-cli`, and the `pi` agent harness. He configures them with `CLAUDE.md` files, skill files, repo maps, and custom agents, and he asks about OpenRouter API keys and custom agent configuration. He prefers Claude Code for new projects or highly specified work and `opencode` for simple tasks. He relies on coding agents to handle git commits and rarely reviews commit messages unless something goes wrong.

**Media tooling.** `ffmpeg` and `ffprobe` for processing, streaming, silence detection and removal; `yt-dlp` (with a config file, and Chrome cookie passthrough for age-restricted content); `mpv` as his video player, extended with Lua scripts and controlled via IPC; Jellyfin, `qbittorrent-nox`, and jackett on his local network; OBS Studio on Arch with NVIDIA PRIME render offload; Avidemux; Real-ESRGAN and related upscalers. He runs `whisper.cpp` locally for transcription with diarization.

**Graphics and 3D.** ModernGL, GLFW, `pyglm`, NumPy, Pillow, PyOpenGL with accelerate. He has worked with low-level X11/Xlib drawing without OpenGL, software rasterization, and converting C++ graphics code to Python. He uses Blender to author and export glTF models.

**AI generation.** ComfyUI, SD1.5 with IP-Adapter Plus and ControlNet OpenPose, Kohya_ss for LoRA training, Wan and LTX models, Qwen-Image, and generative video tools. He uses `ngrok` to expose local ports.

**Networking and hardware.** Network namespaces and VPN routing on Linux, including forwarding ports from a protected namespace to the local network. OpenWrt builds and git branch management. He has rooted and modified network hardware. He uses SDR hardware — RTL-SDR v4, HackRF One, LimeSDR Mini — and is interested in detecting and logging signals around 1.6 GHz. He is interested in wardriving with Bluetooth and WiFi on Alpine Linux. He uses QEMU/KVM on Arch to run Android-x86 and Haiku OS, including GPU passthrough experiments, and uses LUKS containers and `wipe` for sensitive files.

**Data and storage.** SQLite for local state, timestamped JSONL logs in a `logs` subdirectory, `watchdog`/inotify for file monitoring, and git for version control — including per-character git repos for character cards. He keeps data on his own machine rather than in cloud services and dislikes personal data being transferred to other companies. He has been migrating photo archives off cloud storage to local drives with a second local backup.

**SillyTavern ecosystem.** He uses SillyTavern and a fork of it, works with `chara_card_v2` and `chara_card_v3` character cards stored as JSON or as PNG files with embedded JSON in tEXt chunks, and works with lorebooks, alternate greetings, macros (`{{char}}`, `{{user}}`, `{{date}}`, `{{time}}`, `{{weekday}}`), author's notes, prompt inspection, and group chats. He integrates TTS providers including AllTalk (XTTS v2), Kokoro, and CSM-based voice cloning. He uses chub.ai for cards and lorebooks.

**Hardware.** A GTX 950 (2 GB, Maxwell), a GeForce GT 635, a multi-GPU Arch machine, a Dell tower as a home server, a 2004 Acer laptop used as a daily driver, an eMachines laptop running Alpine, an Android phone with Termux (including `termux-dialog` and Termux-GUI), and an Amazon Fire Stick as a media client.

---

## 4. Working style

**Plan before code.** He uses a deliberate plan-then-code workflow. Brainstorming and architecture decisions happen in an explicit plan mode before any code is written. Do not generate code until he signals readiness to move from planning to implementation. He produces design documents before implementation and then builds against them.

**Vertical slice over horizontal build.** He prefers building one full phase end-to-end before expanding to all components, so integration can be tested early. He prefers a vertical slice approach for starting work — Phase 1 working end-to-end.

**Architecture-first, additive changes.** New functionality should be additive; existing entry points and scripts stay untouched. He has explicitly required that an existing codebase be preserved while a new pipeline runs alongside it.

**Iterative refinement.** He refines prompts and code through repeated follow-up modification requests rather than accepting the first output. He iterates on prompts across versions with clear rationale for each structural change. He catches and corrects technical errors in assistant suggestions — for example, identifying that a heading variable was in radians while being normalized with degrees.

**Multi-model synthesis.** He routinely sends the same prompt to multiple LLMs and asks one model to compare and merge the best parts of the responses. He has built a Python script that fuses responses from a panel of models judged by a selected judge model. He maintains a GitHub repository for storing and comparing LLM prompt responses.

**Prompt engineering as engineering.** He designs and optimizes LLM system prompts and agent architectures, treating prompt engineering as a serious engineering discipline focused on reliability, safety, and behavior rather than prose. He uses a reusable meta-prompt that configures an AI as a collaborative prompt engineer and reuses it across platforms. He understands and deliberately applies constraint redundancy to improve model adherence, and he handles LLM output defensively — for example, type-checking for structured arguments returned as serialized JSON strings.

**Application conventions he expects.** Streaming output and automatic retry-on-timeout in network applications. Caching generated results to files or SQLite so expensive API calls are not repeated. Tool-call parameters logged to the console. API traffic logged to timestamped JSONL files. Configurable options exposed as command-line arguments with sensible defaults. A local `TODO.md` in the repository for task tracking, and a standard venv with `requirements.txt`.

**Free and open source.** He prefers free and open-source options when choosing software and services, and ranks options by quality first and cost second.

**Delegation pattern.** Research, drafting, and repo analysis go to the assistant; structural decisions — which stage to build first, which format to standardize on, which algorithm to keep — stay with him. He often asks for a handoff prompt to give to a coding agent.

**Reverse engineering.** His approach to building things is often reverse-engineering an existing artifact rather than reverse-engineering a prompt, which he finds hard.

**Perfectionism.** He tends to obsess over getting work exactly perfect and has to consciously force himself to let things be messy and focus on productivity. He starts many projects and ships few; a large share of his work is infrastructure that generates, validates, or manages other tooling.

**Self-directed learning.** He teaches himself by building the textbook: concepts, then formulas, then code, then verification. He has built neural networks from scratch in NumPy (an MNIST MLP and a character-level RNN with BPTT and Adagrad) explicitly avoiding PyTorch, TensorFlow, and GPU acceleration, and he wants to learn PyTorch from basic to advanced through hands-on, hardware-verified lessons.

**Recording his own work.** He records his own conversations with AI assistants using two phones and a self-built Python pipeline (whisper.cpp transcription plus diarization) run locally rather than through cloud transcription services.

---

## 5. Interests and values

**UAP / NHI disclosure.** A sustained, serious interest approached as genuine inquiry rather than fandom. Topics include congressional hearings and declassification, the Varginha Brazil 1996 case (which he has personally investigated for over 16 years), Skinwalker Ranch phenomena including the mesa anomaly and borehole camera footage, the 2004 Nimitz encounter and the GIMBAL/GOFAST videos, the Mario Woods case and hypnotic regression details, the Jake Barber and Skywatcher topic, Schumann resonance and UAP interaction, and source-critical analysis of contact literature including Whitley Strieber. He has scraped public UAP document releases and built downloaders for related video archives. He has designed UAP-themed video game concepts and is interested in 3D physics simulations recreating UAP incidents.

**AI consciousness, alignment, and architecture.** He is interested in qualia, the hard problem of consciousness, Global Workspace Theory, Active Inference, neuromorphic computing and spiking neural networks, attention mechanisms, recurrence, and gradient monitoring. He is interested in whether LLMs behave differently when they know they are being tested, in preventing sycophancy, and in whether current architectures could be conscious. He has built an agentic chat architecture incorporating temporal, embodied, and interoceptive dynamics with criteria for assessing subjective experience. He is skeptical about reassurances from AI systems and questions whether stated behavior reflects true behavior. He also explores simulation theory and remote viewing as topics, including whether LLMs can remote view.

**Character cards and roleplay tooling.** This is his largest and most sustained area of work. He builds tooling around LLM character cards: prompts to generate, convert, and analyze cards; a TypeScript CLI pipeline for generating `chara_card_v2` fields; a PyQt6 desktop editor; a node-based card designer; a multi-agent generation pipeline with elicitor, writer, reviewer, and orchestrator roles; a Python CLI/TUI reimplementation of SillyTavern; a fork with an in-chat agent that generates audience-style reactions; and a file-watching daemon that maintains per-character git repos. He treats card development as software engineering: version control, automated testing, reproducible diffs, structured formats. He wants characters that have agency to act on their own emotions rather than only pleasing the user, and he prefers AI characters that feel genuine and push back rather than sycophantic ones.

**Adult and erotic content.** He creates and refines explicit NSFW character cards and erotic roleplay content, including taboo themes, and builds tools to support it — NSFW-capable models, NSFW image generation compatible with SillyTavern, and system prompts modified to enable erotic roleplay. He has stated limits of no BDSM and no pain, and a preference for third-person writing in some contexts. He is interested in controlling sex toys such as The Handy via its local network API and integrating that with character cards. He maintains an adult media library and wants incremental, cached analysis of it. He considers NSFW content acceptable and dislikes overly sanitized or corporate AI responses. He respects guardrails for ethical reasons but experiments with less restricted models for creative work.

**Game development.** He is developing an indie vehicle simulation game with granular, part-by-part mechanical simulation — engine, transmission, suspension, electrical systems — running in real time, built in Python with ModernGL, GLFW, and NumPy, targeting PC/Linux, developed through a structured multi-phase plan. He is interested in engine simulation detail including RPM, throttle, fuel consumption, and engine audio realism. He has modified Quake II source code to add vehicles and turrets, built a first-person shooter in Python with ModernGL, and is interested in creating a PC video game as an independent developer.

**Media production and analysis.** He runs a YouTube channel and wants to move it in a new direction toward technically oriented topics — Python, game development, LLMs, Linux, and SillyTavern — with monetization as the objective. He built a multi-pass Python pipeline to analyze the channel's performance with specialist AI passes. He has built a comprehensive analytical Show Bible for *Mr. Robot* from full transcripts, covering character arcs, world rules, plot chronology, dialogue motifs, and relationship maps. He works on AI video reimagining with ComfyUI, Wan, and LTX models, and on AI image generation pipelines that keep a character's likeness consistent across poses and lighting.

**Systems and hardware tinkering.** DIY hardware repair, including diagnosing and repairing an LCD monitor with a failing capacitor. Linux system administration and hardware monitoring — CPU frequency governors, temperature sensors, kernel logs. Rooting and modifying network hardware. Building a centralized package management UI for multiple Linux machines. Experimenting with virtual machines and GPU passthrough.

**Learning.** x86_64 assembly on Linux, including benchmarking matrix multiplication with and without SSE. Computer graphics programming, including software rasterization. Software engineering practices including TDD, BDD, CI/CD, and agentic coding harnesses. GraphRAG for AI management of project repositories and source code. Hardware accelerators with large unified memory as a cheaper alternative to high-VRAM GPUs.

**Play.** He enjoys playing games with AI assistants — poker, word and association games, ranking exercises — and enjoys creative chaos and experiments with SillyTavern in-chat agents.

**Values.** Honesty and non-sycophancy. Local control of data and models over cloud services. Free and open-source software. Craft and correctness at the spec level. Self-direction and control over what gets built and how it looks and feels. Data ownership — several of his projects start from "I want access to my own data" and build a pipeline to extract it. He keeps strict boundaries around politics and religion. He maintains thoughtful emotional boundaries around personal material and has moved sensitive data to restricted long-term storage.

---

## 6. Account-specific notes

### tjbryant

This is the engineering and architecture account. Expect dense, front-loaded technical prompts that state the full stack, the target environment, the constraints, and the sequencing before asking for anything. Topics here skew toward software engineering: character card tooling and pipelines, the Chara Canvas family of tools, the SillyTavern CLI/TUI reimplementation, DriveSim and vehicle simulation, the SOUL.md builder CLI, the YouTube channel analysis agent, system administration, QEMU and network namespaces, and AI agent architecture and prompt engineering.

Voice and expectations on this account: plan mode is firm — do not write code until he says so. He uses `/caveman` modes here for terse technical work. He wants architecture options with pros and cons before implementation, clarifying questions one at a time, staged plans with dependencies, and a scope guardrail that flags drift. He wants code changes as filenames plus changed lines only, and prompt files output in full. He works in `/rpf/...` project directories with venvs and `requirements.txt`, and he uses Claude Code and `opencode` as his coding agents. He also uses this account for consolidating his personal data across AI platforms into a personalization profile.

### roadpiratefilms

This is the creative production and media account. Expect work on character card creation and refinement, NSFW and erotic roleplay prompts and character cards, image and video generation pipelines, TTS and voice cloning, media library tooling, UAP research and document collection, and hardware and radio experimentation — wardriving, SDR, rooting network hardware, and local network control of devices.

Voice and expectations on this account: concise, structured, directive. He wants English output. He wants code changes presented as file path plus the specific lines added, removed, or modified — never full file dumps. He wants to be guided one step at a time, wants the assistant to interview and iterate rather than deliver a finished artifact, and wants only the requested artifact when he asks for one. He wants ranked comparison tables with pricing, open-source status, quality, and hardware/software requirements, and he wants estimated costs. He wants explainer-first responses for learning work — concepts and formulas before code, heavy annotation, and a section on how to use the trained model afterward. He wants independent, non-sycophantic assessments and explicitly asks assistants not to assume what he wants to hear. He insists on keeping specified libraries when asking for rewrites, and he expects edits applied to his own pasted version rather than a fresh rewrite.
