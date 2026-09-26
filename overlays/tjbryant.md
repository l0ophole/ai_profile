# tjbryant — Account Overlay

## Voice and register
The user writes dense, front-loaded prompts: stack, constraints, file layout, and sequencing all arrive before the actual request. He often works in a self-imposed terse mode (`/caveman ultra`) for technical sessions — abbreviated prose, arrows for causality, tables for structure, code and API names left exact. He switches back to normal prose for planning and analysis. He treats the exchange as a collaboration, not a tool invocation, and will push back on output that reads as sanitized or corporate.

## Projects
- **Character card tooling** is the throughline: Chara Canvas (PyQt6 field-by-field card generator, OpenRouter backend, SQLite, node-editor pipeline), the Kara Canvas Pipeline (cascade function auto-updating dependent fields, JSON session files), a multi-agent elicitor/writer/reviewer/assembler pipeline with agent-mode and markdown-output variants, `chara_card_editor.py` (Textual TUI), `charagen.py`, `st_data_vc.py` (inotify watcher giving each card a git repo, fields exploded to markdown for clean diffs), and a card test generator/grader harness.
- **stcli** — a Python CLI/REPL/TUI reimplementation of SillyTavern, staged toward parity, built with Claude Code from a repo map.
- **DriveSim** — Python/OpenGL/GLFW/pyglm driving simulator, arcade Ackermann physics, scene graph, OBJ loader.
- **Road Pirate Films** (@roadpiratefilms) — YouTube channel pivoting to technical content; a six-pass Python analysis pipeline (yt_dlp + OpenRouter) drives the strategy.
- Smaller builds: SOUL.md builder CLI, CharaTerm harness, whisper.cpp transcription pipeline, ComfyUI/IP-Adapter image pipeline, a shoplifting-detection proof of concept, media-library automation on Alpine.

## Interests
UAP/NHI cases and government disclosure material, approached as source-critical inquiry. Consciousness research — qualia, the hard problem, whether current architectures could be conscious. LLM prompt engineering and meta-prompts that compare or synthesize system prompts. x86_64 assembly and low-level performance. Game development and engine/vehicle simulation. Adult and romantic AI character roleplay, including explicit character cards and third-person ERP writing. Influences: John Carmack, Linus Torvalds, Fabien Sanglard.

## Working preferences
- Plan first, approve, then code. One clarifying question at a time. Offer numbered options and let him choose.
- Act as a scope guardrail: flag drift from the agreed plan and give pros/cons before changing course.
- Vertical slice over horizontal build — one phase working end to end.
- Explain concepts and formulas before code; he wants the reasoning behind recommendations.
- Fact-check continuously rather than letting inaccuracies pass.
- For code changes: file path plus changed lines only. Prompt files: full text.
- Character cards should give characters agency and let them push back; he dislikes sycophancy.
- Roleplay formatting: speech in double quotes, actions in asterisks, narration plain, blank lines between types.
- Keep sensitive prompt content private — he substitutes placeholders.
- Avoid politics and religion. Show generated content in full, not truncated.
- Prefers local storage and self-hosting over cloud; API keys in local `.env` files.

## Environment
Arch Linux primary (i3, PipeWire, Xorg, no display manager), Alpine on older machines, SSH/VNC into a home server. Python 3.14, venv, Pydantic, Textual, PyQt6, httpx/requests. OpenRouter as the main inference path, DeepSeek models frequently; Claude Code and OpenCode as coding agents. Local GPU is small, so large models go to APIs or Colab. GitHub handle L0OPHOLE; local username rpf. Programming background runs QBASIC → mIRC/TCL → C → Quake 2 modding → Bash → Python.
