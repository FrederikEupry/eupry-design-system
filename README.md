# Eupry Design System

The design backbone for Eupry-branded tools, pages, and components — colors, typography
(Instrument Sans), components, spacing, and the squid logo.

## Use it with Claude

**Claude Desktop:** download [`skill/eupry-design-system.zip`](skill/eupry-design-system.zip)
and upload it under **Settings → Capabilities → Skills**. Full steps in
[`skill/INSTALL.md`](skill/INSTALL.md). After that, just ask Claude to build something
"in the Eupry style" and it follows the rules automatically.

**Claude Code (CLI):** drop `skill/eupry-design-system/` into `~/.claude/skills/`, or point
Claude at this repo and tell it to read `DESIGN.md` + `tokens.json`.

## What's here

| File | What it is |
|------|------------|
| [`DESIGN.md`](DESIGN.md) | Full spec — every color scale, type scale, component CSS, breakpoints, effects |
| [`tokens.json`](tokens.json) | All design tokens as structured data |
| [`CLAUDE.md`](CLAUDE.md) | Quick reference for AI agents |
| `fonts/` | Instrument Sans (`.woff2`) |
| `icons/` | The `eupry-squid` brand mark (UI icons use [Lucide](https://lucide.dev)) |
| `skill/` | Packaged Claude Desktop skill + install guide |

## Icons

UI icons use [Lucide](https://lucide.dev) via CDN. The squid logo is the only custom icon.
