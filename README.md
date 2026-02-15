# @compilr-dev/cli

```
      \|/
    ╭══════════╮     ___  ___  _ __ ___  _ __ (_) |_ __
    ║'  ▐▌  ▐▌ │    / __|/ _ \| '_ ` _ \| '_ \| | | '__|
    ║          │   | (__| (_) | | | | | | |_) | | | |
    ╰─═──────═─╯    \___|\___/|_| |_| |_| .__/|_|_|_|
      \________\                        | | .dev
                                        |_| CLI
```

> AI-powered coding assistant for your terminal

[![npm version](https://img.shields.io/npm/v/@compilr-dev/cli.svg)](https://www.npmjs.com/package/@compilr-dev/cli)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview

A structured AI coding assistant that brings discipline to AI-assisted development. Supports 9 LLM providers, multi-agent teams, project workflows, and 25 interactive tutorials -- all in your terminal.

**Stop vibe coding. Start building.**

## Quick Start

```bash
# Install globally
npm install -g @compilr-dev/cli

# Start the CLI
compilr

# Set your API key (interactive prompt on first run)
# Or use /keys inside the CLI
```

## Features

### Multi-LLM Support (9 Providers)

Use your preferred AI provider with three tiers per provider (Fast / Balanced / Powerful):

| Provider | Models | API Key |
|----------|--------|---------|
| **Claude** | Haiku, Sonnet, Opus | `ANTHROPIC_API_KEY` |
| **OpenAI** | GPT-4o-mini, GPT-4o, o1 | `OPENAI_API_KEY` |
| **Gemini** | Flash, Pro, Ultra | `GOOGLE_API_KEY` |
| **Ollama** | Any local model | None (local) |
| **Together AI** | Open-source models | `TOGETHER_API_KEY` |
| **Groq** | Fast inference | `GROQ_API_KEY` |
| **Fireworks** | Open-source models | `FIREWORKS_API_KEY` |
| **Perplexity** | Search-augmented | `PERPLEXITY_API_KEY` |
| **OpenRouter** | Multi-provider | `OPENROUTER_API_KEY` |

Switch models anytime with `/model` -- a visual overlay with provider tabs, model cycling, and connection testing.

### Project Workflows

Built-in commands for structured development:

| Command | Description |
|---------|-------------|
| `/new` | Create a project with guided 8-step wizard |
| `/design` | AI-driven requirements gathering (creates PRD + backlog) |
| `/sketch` | Quick 6-question project outline |
| `/prd` | Update the Product Requirements Document |
| `/arch` | Create architecture documentation |
| `/scaffold` | Generate base project structure |
| `/build` | Implement a backlog item end-to-end |
| `/backlog` | Visual backlog management |
| `/docs` | Browse and edit all project documents |

### Multi-Agent Teams

Specialized AI agents with different expertise, tools, and model tiers:

- **`$arch`** Architect -- system design, patterns, tech decisions
- **`$dev`** Developer -- implementation, coding, debugging
- **`$qa`** QA Engineer -- testing, quality, code review
- **`$pm`** PM -- planning, task tracking, estimation
- **`$ops`** DevOps -- deployment, CI/CD, infrastructure
- **`$docs`** Technical Writer -- documentation, guides
- **`$ba`** Business Analyst -- requirements, metrics

Run agents in the background with `$agent message &`, manage with `/bg`, `/fg`, `/kill`.

### Smart Context

- **Auto-compaction** -- automatically manages context window
- **Anchors** -- persistent notes that survive compaction and sessions
- **Token tracking** -- real-time context visualization with `/context`
- **Session restore** -- pick up where you left off
- **COMPILR.md** -- project-specific instructions loaded automatically

### Safety & Permissions

- **Permission levels** -- always, session, once, deny (with wildcards)
- **Permission modes** -- Normal, Plan, Auto-accept
- **Delete protection** -- prevents accidental deletion outside project path
- **15 built-in guardrails** -- git safety, destructive command detection

### 418 Terminal Themes

Choose from 418 themes with live preview. Curated favorites plus browsing by Dark/Light.

### Interactive Tutorials

25 tutorials across 5 tabs (`/tutorial`): Basics, Projects, Plan & Build, Teams, Config.

## Commands

| Category | Commands |
|----------|----------|
| **Project** | `/new`, `/projects`, `/workflow`, `/backlog` |
| **Development** | `/design`, `/sketch`, `/prd`, `/arch`, `/scaffold`, `/build`, `/docs` |
| **Teams** | `/team`, `/bg`, `/fg`, `/kill`, `/pending`, `/filter` |
| **Config** | `/config`, `/model`, `/permissions`, `/keys`, `/anchors` |
| **Context** | `/context`, `/tokens`, `/compact`, `/status`, `/export` |
| **Navigation** | `/help`, `/tutorial`, `/clear`, `/exit` |

## Configuration

### API Keys

**Option 1: Use `/keys` command (recommended)**

Run `/keys` inside the CLI to securely store your API keys. Keys are encrypted and stored locally.

**Option 2: Environment variables**

```bash
export ANTHROPIC_API_KEY="sk-ant-..."   # Claude
export OPENAI_API_KEY="sk-..."          # OpenAI
export GOOGLE_API_KEY="..."             # Google Gemini
# Ollama: no key needed, just run `ollama serve`
```

### Project Configuration

Create a `COMPILR.md` file in your project root to provide AI context:

```markdown
# COMPILR.md

## Project Overview
This is a React application using TypeScript...

## Coding Standards
- Use functional components
- Prefer hooks over class components
```

The CLI automatically loads this file at startup.

## Requirements

- **Node.js** 20 or higher
- **API Key** for your chosen provider (except Ollama)
- **Platform:** macOS, Linux, or Windows via WSL2

### Windows Users

The CLI requires a Unix-like shell environment. On Windows, use [WSL2](https://learn.microsoft.com/en-us/windows/wsl/install) (Windows Subsystem for Linux):

```bash
# 1. Install WSL2 (run in PowerShell as Administrator)
wsl --install

# 2. Open your WSL terminal, then install Node.js 20+
#    (see https://nodejs.org for instructions)

# 3. Install the CLI inside WSL
npm install -g @compilr-dev/cli

# 4. Start coding
compilr
```

VS Code works seamlessly with WSL via the [WSL extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) -- open your project in VS Code, connect to WSL, and use the integrated terminal.

## Built With

- [@compilr-dev/agents](https://www.npmjs.com/package/@compilr-dev/agents) - Multi-LLM agent framework
- [@compilr-dev/agents-coding](https://www.npmjs.com/package/@compilr-dev/agents-coding) - Coding-specific tools

## Links

- [Website](https://compilr.dev)
- [npm Package](https://www.npmjs.com/package/@compilr-dev/cli)
- [Report Issues](https://github.com/compilr-dev/cli/issues)

## License

MIT - See [LICENSE](LICENSE) for details.

---

```
[^_^] Built with @compilr-dev/agents
```
