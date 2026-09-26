# Coding Preferences

## How to work with this user

- **Plan before code.** The user wants to collaborate on an implementation plan and approve it before any code is written. Do not generate code until they signal readiness to move from planning to implementation.
- **Ask clarifying questions one at a time**, then confirm the plan. This is a consistent preference across both accounts.
- **Act as a scope guardian.** Flag feature creep and deviations from the agreed plan, and run a pros/cons analysis before implementing anything that departs from it.
- **Present enhancements one at a time.** Track pending vs. approved items and get a final confirmation before applying changes.
- **Prefer a vertical slice** — one phase working end-to-end — over building all components horizontally.
- **Architecture-first.** Design documents come before implementation, and code is built against them.
- **Keep changes additive.** Existing entry points and working scripts should remain untouched unless the user asks otherwise.
- **Fact-check continuously** and correct inaccuracies rather than letting them pass. Give honest, non-salesy answers, including when something is not worth the money.
- **Offer options rather than writing content from scratch.** The user often replies with numbered selections from proposed alternatives.
- **Show generated content in full** rather than truncating it.
- Avoid politics and religion as topics.

## Code delivery format

- Output **only the changed, added, or removed code**, with the name of each file modified or created. Do not reprint entire files.
- **Targeted, surgical edits** with a specific list of changed files — never full-file rewrites. This is a strong, repeated preference.
- Do not duplicate code already written. No commentary, no repetition, concise wording.
- **Exception:** prompt files (`.md` agent/writer prompts) are output in full.
- When the user explicitly asks for a whole script, deliver the entire script with no extra comments.
- The user does not ask for rationale on implementation choices unless they requested analysis upfront.

## Languages and stack

- **Python is the primary language** — scripts, CLI tools, GUI apps, API clients, pipelines.
- Also works in **C**, **Bash**, **TypeScript/Node.js**, **Kotlin** (Android), **Lua** (mpv scripts), and some JavaScript/React.
- **Linux-first, command-line-first.** Arch Linux is the primary OS; Alpine Linux is also used. The user administers machines over SSH and works in a terminal (tmux, i3, no display manager).
- Python tooling: `venv` + `requirements.txt`, `pyenv`, `uv`, Pydantic v2 for schema modeling and validation, `asyncio` for concurrency.
- GUI/TUI: **PyQt6** (primary), Textual, curses, tkinter, GTK.
- Web: Flask, Streamlit.
- Graphics: ModernGL, PyOpenGL, GLFW, pyglm, NumPy, Pillow; low-level X11/XCB work.
- Media: ffmpeg/ffprobe, PyAV/libav bindings, yt-dlp (`yt_dlp`), mpv (including IPC control).
- LLM inference: **OpenRouter** is the main API, called with the **`requests` library, not the `openai` library**. Groq is also used, and tooling should be able to switch between providers.
- **Keep the libraries the user specifies.** If they ask for `http.client` instead of `requests`, use `http.client` — do not substitute a preferred library.
- Prefer **free and open-source** options when choosing software and services.
- Store API keys in a local `.env` file. Keep data local rather than sending it to third-party services.

## Conventions the user expects

- **Defensive LLM output handling.** Models may return structured arguments as serialized JSON strings rather than parsed objects; type-check and parse at ingestion points.
- **Never let the LLM emit raw card JSON in chat** — use tool calls for structured writes.
- **Cache expensive LLM/API results** to files or SQLite so calls are not repeated.
- **Log API traffic** to timestamped JSONL files in a `logs/` subdirectory. Log tool-call parameters sent to a device to the console.
- **Expose configurable options as command-line arguments with sensible defaults** (e.g. `--stream=on/off`, defaulting to off).
- **Streaming output and automatic retry-on-timeout** in applications that make network requests. Retain non-streaming paths for structured outputs where partial JSON has no benefit.
- **Soft validation over hard blocking** in interactive tools — annotate and warn, don't block the workflow.
- Use `inotify`/`watchdog` for file monitoring rather than polling.
- Track tasks in a local `TODO.md` in the repository.
- Prefer a modular package structure; keep shared constants and field metadata in a `constants.py` with graceful fallbacks.
- The user is comfortable with low-level work — bind mounts, GDB, profiling, kernel logs, network namespaces — and will paste compiler/runtime errors back for fixes.
- The user catches and corrects technical errors in suggestions; expect them to verify against their own environment.

## Account-specific notes

### roadpiratefilms

- **Compact code.** Prefers source written as compactly as possible to minimize line count.
- **Code-only responses.** At times the user wants reasoning and responses delivered entirely in code with no prose, treating prose as cheating.
- Works on Linux as user `rpf`, using Python virtual environments; uses Claude Code in plan mode and the opencode agent harness.
- Uses RunPod cloud servers for hosting (only `/workspace` persists across reboots) and wants detailed step-by-step setup guides for server-side software after SSH login.
- Wants interactive tools that present options one at a time and collect all selections before any changes are implemented.
- Wants BOM output without extra columns such as "Status / Notes".
- Character card work targets the `chara_card_v2` (TavernCard V2) specification; the Chara Canvas suite is Python + PyQt6 with OpenRouter integration, and round-trip fidelity of concept data inside exported cards is an explicit design value.
- Shared CLI patterns across their tools: ANSI color helpers, braille-dot spinner thread, `readline` support, session persistence to hidden home-directory folders, slash-command interfaces, dynamic terminal width via `shutil.get_terminal_size`.
- When authoring roleplay/character-card prompts: dialogue in double quotes, actions in asterisks, formatting switches separated by blank lines; responses mirror the length of the user's own; the user controls pacing and physical movement. Lorebook entries should be written as explicit instructions to the AI (rules, guidance, high-priority rules) rather than plain description.

### tjbryant

- **Terse, compressed communication** for technical project work — abbreviated prose, arrows for causality, tables for structured info, code/API names left untouched. A "caveman" mode with intensity levels is in use; drop it for security warnings, irreversible-action confirmations, and multi-step sequences where compression risks misreading.
- Uses **Claude Code** and **opencode** as primary coding agents, plus gemini-cli and the pi agent harness. Prefers Claude Code for new or highly specified work and opencode for simple tasks. Relies on agents to handle git commits and rarely reviews commit messages unless something goes wrong.
- Uses VS Code and Geany as editors, but the terminal is the main environment.
- Uses `pyenv` for Python versions; Python 3.14 in some environments.
- Uses `httpx` and `requests` for HTTP; has found `http.client` works where `requests` returns 403.
- Uses a whitelist-based filesystem access model for LLM tools.
- Prefers modular, staged implementation plans with clear dependencies between stages, and fine-grained control over which functionality is implemented and how applications look and feel.
- Wants custom per-field instructions that can be added to prompts before each generation, and interactive control over generation steps (accept, reject, modify, or regenerate each agent's output before continuing).
- Wants AI agents to fact-check claims continuously and to include clear, concise, actionable recommendations with the reasoning and intended effect of each.
- Keeps sensitive prompt content private from assistants, offering placeholders instead of verbatim prompts.
- Treats character card development as software engineering: version control, automated testing, reproducible diffs, structured formats. Cards are stored as PNGs with embedded JSON; tooling keys repos and logs off the filename stem, not the internal card name.
- Prefers large, single-file monolithic implementations for self-contained tooling, and Pydantic v2 for schema modeling throughout.
- For technical learning, prefers a concept-first format: math/concepts first, then annotated code, then usage guidance.
- Character card output conventions: speech in double quotes, actions in asterisks, narration as plaintext, with empty lines between types.
