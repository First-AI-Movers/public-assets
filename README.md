# First AI Movers — Public Assets

> **Accelerating AI adoption for forward-thinking professionals and organisations.**

This repository is the public-facing asset library for [First AI Movers](https://firstaimovers.com). It contains reusable building blocks for teams and individuals looking to adopt Claude-powered AI workflows: instruction templates, MCP configurations, custom skills, and agent topology blueprints.

Everything here is designed to be forked, adapted, and deployed. Attribution is appreciated but not required.

---

## Repository Structure

```
public-assets/
├── claude-md-templates/
│   ├── global/               # Organisation-wide Claude instruction files
│   └── project-specific/     # Per-project or per-role Claude instruction files
├── mcp-configs/              # Model Context Protocol server configuration templates
├── custom-skills/            # Reusable Claude skill definitions
├── agent-topologies/         # Multi-agent architecture blueprints
├── .gitignore
└── README.md
```

---

## How to Use the CLAUDE.md Templates

`CLAUDE.md` files are instruction documents that shape how Claude behaves within a given context — whether that's an entire organisation, a specific project, or a particular role. They are the primary mechanism for establishing consistent, secure, and opinionated AI behaviour across a team.

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

Model Context Protocol (MCP) servers extend Claude's capabilities with real-world integrations — GitHub, Notion, Airtable, Slack, file systems, and more. This folder will contain:

- Canonical MCP server configuration templates
- Security-hardened JSON config files
- Notes on authentication patterns and credential management

> **Coming soon.** Contributions welcome via pull request.

---

## Custom Skills (`custom-skills/`)

Skills are structured instruction sets that guide Claude through specialised, repeatable workflows — document generation, architecture design, data analysis, and more. This folder will contain community-contributed and First AI Movers-authored skill definitions.

> **Coming soon.** Contributions welcome via pull request.

---

## Agent Topologies (`agent-topologies/`)

Multi-agent systems require deliberate architecture. This folder will contain blueprint documents describing how to structure networks of Claude agents for different use cases: parallel research pipelines, hierarchical task decomposition, supervisor-worker patterns, and more.

> **Coming soon.** Contributions welcome via pull request.

---

## Contributing

Pull requests are welcome. Please follow these conventions:

- Use [Conventional Commits](https://www.conventionalcommits.org/) for all commit messages
- Never commit `.env` files, credentials, API keys, or any sensitive data
- Include a brief description of what you're adding and the use case it addresses

---

## License

Content in this repository is released under the [MIT License](LICENSE) unless otherwise noted. You are free to use, modify, and distribute with attribution.

---

*Maintained by [Hernani](mailto:hernani@firstaimovers.com) and the First AI Movers team.*
