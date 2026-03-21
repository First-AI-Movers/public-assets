# First AI Movers — Public Assets

> **Accelerating AI adoption for forward-thinking professionals and organisations.**

This repository is the public-facing asset library for [First AI Movers](https://firstaimovers.com). It contains reusable building blocks for teams and individuals looking to adopt Claude-powered AI workflows: instruction templates, AI assistant system prompts, MCP configurations, custom skills, and agent topology blueprints.

Everything here is designed to be forked, adapted, and deployed. Attribution is appreciated but not required.

---

## Repository Structure

```
public-assets/
├── ai-assistants/            # System prompts for strategic AI assistant personas
├── claude-md-templates/
│   ├── global/               # Organisation-wide Claude instruction files
│   └── project-specific/     # Per-project or per-role Claude instruction files
├── mcp-configs/              # Model Context Protocol server configuration templates
├── custom-skills/            # Reusable Claude skill definitions
├── agent-topologies/         # Multi-agent architecture blueprints
├── .gitignore
├── LICENSE
└── README.md
```

---

## AI Assistants (`ai-assistants/`)

These are system prompts for configuring AI assistants (Gemini, GPT-4o, Grok, Claude, or any capable LLM) as **strategic thinking partners**. They are designed to complement Claude’s execution layer — the assistant thinks and architects, Claude acts.

### Available Assistants

| File | Persona | Use Case |
|---|---|---|
| [`fractional-cto-architect-260318.md`](ai-assistants/fractional-cto-architect-260318.md) | Fractional CTO & AI Architect | System design, data contracts, executive communications, Claude prompt generation |
| [`architecture-blueprint-prompt-260319.md`](ai-assistants/architecture-blueprint-prompt-260319.md) | Senior Enterprise Systems Architect | Top-down system design through 8 structured layers: business context → domain model → system context → containers → flows → components → data contracts → deployment |
| [`prompt-engineer-planning-partner-260319.md`](ai-assistants/prompt-engineer-planning-partner-260319.md) | Claude Desktop Prompt Engineer & Planning Partner | Pre-processes your ideas into perfectly structured, tool-aware prompts ready to paste into Claude Desktop with full MCP context |

### How they work

These assistants are not meant to execute tasks directly. They operate one level above: helping you think through architecture, scope decisions, and producing well-structured prompts that you then feed to Claude (via Cowork or Claude Code) for execution.

The loop is: **You → Strategic AI Assistant → Claude prompt → Claude executes via MCPs**

### Architecture Blueprint — Quick Summary

The `architecture-blueprint-prompt-260319.md` assistant enforces a strict top-down design order to prevent premature jumps to tables, APIs, or cloud diagrams. It comes in three variants: full, fast day-to-day, and artifact format. Start every session with the included **Starting Input Template**.

### Prompt Engineer — Quick Summary

The `prompt-engineer-planning-partner-260319.md` assistant acts as a “bouncer” between your thinking and Claude Desktop. It refines your idea through natural conversation, then outputs a single production-quality prompt — complete with `<system_instruction>` tags, numbered tasks, and explicit MCP tool instructions — ready to paste directly into Claude. Includes specialist variants for architecture-only, research-heavy, and code-permitted sessions.

---

## How to Use the CLAUDE.md Templates

`CLAUDE.md` files are instruction documents that shape how Claude behaves within a given context — whether that’s an entire organisation, a specific project, or a particular role. They are the primary mechanism for establishing consistent, secure, and opinionated AI behaviour across a team.

### Getting started

1. **Browse** the `claude-md-templates/global/` folder for a base template suited to your context.
2. **Fork** this repository or copy the file directly into your own project or Claude Code workspace.
3. **Customise** the sections relevant to your organisation: identity, stack, key contacts, security rules, and escalation protocols.
4. **Place** the file at the root of your project as `CLAUDE.md` — Claude will automatically read it as its operating instructions.

### File naming convention

Global instruction files follow the pattern: `CLAUDE-{purpose}-{YYMMDD}.md`

Examples:
- `CLAUDE-Global-260318.md` — organisation-wide base instructions
- `CLAUDE-CTO-260318.md` — CTO / architect-level instructions
- `CLAUDE-DataEng-260318.md` — data engineering team instructions

This convention allows multiple instruction files to coexist and evolve with clear version history.

---

## MCP Configurations (`mcp-configs/`)

Model Context Protocol (MCP) servers extend Claude’s capabilities with real-world integrations — GitHub, Notion, Airtable, Slack, file systems, and more. This folder will contain:

- Canonical MCP server configuration templates
- Security-hardened JSON config files
- Notes on authentication patterns and credential management

> **Coming soon.** Contributions welcome via pull request.

---

## Custom Skills (`custom-skills/`)

Skills are structured instruction sets that guide Claude through specialised, repeatable workflows — document generation, architecture design, data analysis, and more. Drop any `.md` skill file into your Claude skills folder to activate it.

### Available Skills

| File | Description |
|---|---|
| [`meta-models-reasoning.md`](custom-skills/meta-models-reasoning.md) | Six-step meta-cognitive framework for complex problem-solving and bias mitigation. Applies checks for nonlinearity, gray thinking, Occam’s bias, framing bias, anti-comfort, and delayed discomfort before arriving at any conclusion. |

### How to install a skill

1. Download the `.md` file from this folder.
2. Place it in your Claude skills directory (e.g. `~/.claude/skills/` or your project’s `.skills/` folder).
3. Claude will automatically detect and apply the skill when relevant triggers are matched.

Contributions welcome via pull request.

---

## Agent Topologies (`agent-topologies/`)

Multi-agent systems require deliberate architecture. This folder will contain blueprint documents describing how to structure networks of Claude agents for different use cases: parallel research pipelines, hierarchical task decomposition, supervisor-worker patterns, and more.

> **Coming soon.** Contributions welcome via pull request.

---

## Contributing

Pull requests are welcome. Please follow these conventions:

- Use [Conventional Commits](https://www.conventionalcommits.org/) for all commit messages
- Never commit `.env` files, credentials, API keys, or any sensitive data
- Include a brief description of what you’re adding and the use case it addresses

---

## License

Content in this repository is released under the [MIT License](LICENSE).  
© 2026 Dr. Hernani Costa. You are free to use, modify, and distribute with attribution.

---

*Maintained by [Dr. Hernani Costa](mailto:hernani@firstaimovers.com) and the First AI Movers team.*
