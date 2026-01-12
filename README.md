# Cloudflare Worker Skill Plugin

A plugin that provides a skill for creating new Cloudflare Workers projects with modern tooling.

## Installation

### Claude Code

```bash
git clone https://github.com/mattzcarey/cloudflare-agent-plugin
/plugin install ./cloudflare-agent-plugin
```

### OpenCode

```bash
mkdir -p ~/.config/opencode/skill/new-cf-worker
curl -o ~/.config/opencode/skill/new-cf-worker/SKILL.md https://raw.githubusercontent.com/mattzcarey/cloudflare-agent-plugin/main/skills/new-cf-worker/SKILL.md
```

## Usage

Invoke the skill by:
- Typing `/new-cf-worker my-project-name`
- Asking Claude to "create a new Cloudflare Worker project"

## What it creates

- **npm** project with modern ES modules
- **wrangler.jsonc** with today's date for `compatibility_date`
- **wrangler types** for generating `Env` type (not `@cloudflare/workers-types`)
- **tsgo** for fast typechecking
- **observability** with logs and tracing enabled
- **.mcp.json** with Cloudflare docs MCP server for contextual help

## Project structure created

```
my-project/
├── src/
│   └── index.ts
├── package.json
├── tsconfig.json
├── wrangler.jsonc
├── .gitignore
└── .mcp.json
```

## License

MIT
