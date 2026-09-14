# Sato Plugins

A [Claude Code plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces)
published by [Sato Hub](https://satohub.ai) — the agent builder hub for crypto.

## Install it in one line

```sh
claude mcp add --transport http satohub https://satohub.ai/api/mcp   # Claude Code
codex mcp add satohub --url https://satohub.ai/api/mcp               # Codex CLI
gemini mcp add --transport http satohub https://satohub.ai/api/mcp   # Gemini CLI
```

One click for [VS Code](https://vscode.dev/redirect/mcp/install?name=satohub&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fsatohub.ai%2Fapi%2Fmcp%22%7D)
or [VS Code Insiders](https://insiders.vscode.dev/redirect/mcp/install?name=satohub&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fsatohub.ai%2Fapi%2Fmcp%22%7D&quality=insiders).

**Cursor, Windsurf, Zed, Cline, Continue, JetBrains, LM Studio, Goose, Warp,
Claude Desktop** — deep links and the exact config block for each, generated
from one endpoint constant: **<https://satohub.ai/install>**
(machine-readable at [`/api/install.json`](https://satohub.ai/api/install.json)).
GitHub strips `cursor://` and `lmstudio://` links from READMEs, which is why the
one-click buttons live on that page rather than here.

Then drop in the [agent kit](https://satohub.ai/kit) — `AGENTS.md`,
`CLAUDE.md`, `.cursor/rules/satohub.mdc`, `.windsurfrules` — so the model
reaches for the server instead of answering from memory. Copies in
[`kit/`](./kit).

## Install

```sh
/plugin marketplace add satohubai/sato-plugins
/plugin install sato-hub@sato-plugins
```

## What's in it

### `sato-hub`

One plugin, two halves:

- **The MCP server** — the hosted Sato Hub endpoint at
  `https://satohub.ai/api/mcp` (Streamable HTTP, no key, nothing to run
  locally). Search the daily-rebuilt index of onchain-agent tooling
  (frameworks, MCP servers, wallets, x402 rails, ERC-8004 registries, agent
  skills), read agent-economy numbers per venue and chain, look up an Agent
  Passport, run a **Preflight** check on a repo, package, MCP endpoint,
  ERC-8004 agent or ERC-20 token before you install, connect, pay or trade,
  and ask **Sato Route** which venue to use with the fee disclosed and every
  reason named. Current tool list: <https://satohub.ai/mcp>.
- **The skill** — [`satohubai/sato-hub-skill`](https://github.com/satohubai/sato-hub-skill),
  which teaches the model *when* to reach for those tools, how to read a Sato
  Score, and to cite the `sato_url` on every record it surfaces. The plugin
  installs it from that repo, so the skill and the plugin never drift.

The plugin is read-only and non-custodial: it signs nothing, holds no keys, and
never broadcasts a transaction. A Sato Score is a 0–100 measure of how open,
active and verifiable a project is — **not** a safety, quality or returns
grade ([methodology](https://satohub.ai/sato-score)).

## Other ways to install the same thing

```sh
# any Agent Skills client (Claude Code, Codex, Cursor, Hermes, …)
npx skills add satohubai/sato-hub-skill

# MCP server only, no skill
claude mcp add --transport http satohub https://satohub.ai/api/mcp
```

## Licence

Tooling MIT. Catalog data CC-BY-4.0, attribution *data by satohub.ai*.
