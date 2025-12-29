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

## Quick Start

```bash
# Install globally
npm install -g @compilr-dev/cli

# Start the CLI
compilr

# Set your API key (interactive prompt)
/keys
```

## Features

### Multi-LLM Support

Use your preferred AI provider:

```bash
compilr                              # Claude (default)
compilr --provider openai            # OpenAI GPT-4
compilr --provider gemini            # Google Gemini
compilr --provider ollama            # Local models
```

### Project Workflows

Built-in commands for structured development:

| Command | Description |
|---------|-------------|
| `/init` | Initialize a new project with guided wizard |
| `/design` | AI-driven requirements gathering |
| `/sketch` | Quick 6-question project outline |
| `/refine` | Iterative refinement of requirements |
| `/backlog` | Manage project backlog |

### Coding Tools

The CLI includes tools for file operations, git, and code search:

- **File Operations** - Read, write, edit files with permission prompts
- **Git Integration** - Status, diff, commit, branch management
- **Code Search** - Find definitions, references, TODOs
- **Project Detection** - Auto-detect project type and structure

### Smart Context

- **Auto-compaction** - Keeps context manageable for long sessions
- **COMPILR.md** - Project-specific instructions loaded automatically
- **Token tracking** - Monitor usage with `/tokens`

## Commands

| Command | Description |
|---------|-------------|
| `/help` | Show available commands |
| `/keys` | Manage API keys |
| `/config` | Configure settings |
| `/init` | Initialize new project |
| `/design` | Requirements gathering workflow |
| `/sketch` | Quick project outline |
| `/refine` | Refine requirements iteratively |
| `/backlog` | Manage project tasks |
| `/tools` | List available tools |
| `/tokens` | Show token usage |
| `/context` | Show context statistics |
| `/compact` | Compress conversation context |
| `/clear` | Clear conversation history |
| `/exit` | Exit the CLI |

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Esc` | Cancel running operation |
| `Enter` | Send message |
| `↑` / `↓` | Navigate history |

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

Environment variables take priority over stored keys.

### Project Configuration

Create a `COMPILR.md` file in your project root to provide context:

```markdown
# COMPILR.md

## Project Overview
This is a React application using TypeScript...

## Coding Standards
- Use functional components
- Prefer hooks over class components
...
```

The CLI automatically loads this file at startup.

## Requirements

- **Node.js** 18 or higher
- **API Key** for your chosen provider (except Ollama)

## Built With

- [@compilr-dev/agents](https://www.npmjs.com/package/@compilr-dev/agents) - Multi-LLM agent framework
- [@compilr-dev/agents-coding](https://www.npmjs.com/package/@compilr-dev/agents-coding) - Coding-specific tools

## Links

- [Website](https://compilr.dev)
- [Documentation](https://compilr.dev/docs)
- [npm Package](https://www.npmjs.com/package/@compilr-dev/cli)
- [GitHub Issues](https://github.com/compilr-dev/cli/issues)

## License

MIT - See [LICENSE](LICENSE) for details.

---

```
[^_^] Built with @compilr-dev/agents
```
