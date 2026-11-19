# memr.io plugin

[memr.io](https://memr.io) (said "mem'ry'oh") is a memory you own, shared by every AI assistant you use: your
to-dos, notes, projects, people, places and life events, kept as real records. Every change is numbered and can
be undone.

This repository holds the memr.io plugin for Claude: the connector, skills and rules that help an assistant use
memr.io well. Full documentation: **https://memr.io/docs**.

## What's inside

| Path | What it is |
|---|---|
| `plugins/memr-io/.mcp.json` | The memr.io connector, `https://memr.io/mcp` (OAuth sign-in on first use) |
| `plugins/memr-io/skills/memr/` | Everyday use: to-dos, notes, memory, what's ready or blocked |
| `plugins/memr-io/skills/memr-setup/` | New accounts and the guided setup of a first project, memory and a timeline |
| `plugins/memr-io/skills/memr-timeline/` | Recording life events, people, places and organizations: dates, sources, importance, privacy |
| `plugins/memr-io/skills/memr-review/` | What changed and undo, a weekly review, and tidying duplicates and gaps |
| `plugins/memr-io/rules/memr-io.md` | Short best-practice rules to paste into a `CLAUDE.md`, `AGENTS.md` or any assistant's instructions |
| `.claude-plugin/marketplace.json` | Makes this repository installable as a Claude Code plugin marketplace |

## Requirements

A memr.io account with an active plan. Personal starts with a
[14-day free trial](https://memr.io/billing). There is no free plan.

## Install

**Claude Code**

```
/plugin marketplace add kyle-nahrgang/memr-io-plugin
/plugin install memr-io@memr-io
```

Then run `/mcp` and sign in to memr.io.

**Claude (web, desktop, mobile)**: add the connector in Settings, Connectors, as a custom connector with the URL
`https://memr.io/mcp`. To use the skills there, upload the folders under `plugins/memr-io/skills/` in
Settings, Capabilities, Skills.

**Any other assistant**: add `https://memr.io/mcp` as a remote MCP server, and paste
`plugins/memr-io/rules/memr-io.md` into its instructions.

## Getting started

Say **"set me up with memr.io"**. See [memr.io/start](https://memr.io/start) for a 10-minute walkthrough.

## Your own rules win

The skills and rules are deliberately light. Where your own instructions (a `CLAUDE.md` or similar) differ,
they take priority.

## Support and policies

- Docs: https://memr.io/docs
- Support: support@memr.io
- [Privacy policy](https://memr.io/privacy) · [Terms of service](https://memr.io/terms)

Issues and suggestions for the skills and rules are welcome here.

## License

[MIT](LICENSE) © 2026 NahrDev LLC. The license covers the files in this repository; the memr.io service is
governed by its [terms of service](https://memr.io/terms).
