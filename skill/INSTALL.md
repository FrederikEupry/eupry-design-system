# Install the Eupry Design System skill (Claude Desktop)

This makes Claude generate **Eupry-branded** pages, components, and emails automatically —
correct colors, Instrument Sans font, pill buttons, the squid logo, all of it.

## 1. Download the skill

Download **`eupry-design-system.zip`** from this folder (in the GitHub repo:
`skill/eupry-design-system.zip` → click it → **Download**).

> Don't unzip it. Claude Desktop wants the `.zip`.

## 2. Upload it in Claude Desktop

1. Open **Claude Desktop**.
2. Go to **Settings → Capabilities → Skills** (on some versions it's **Settings → Features**).
3. Click **Upload skill** and pick `eupry-design-system.zip`.
4. Make sure the skill is toggled **on**.

> Requires a paid Claude plan (Pro/Team/Enterprise). If you don't see a Skills section,
> your plan or workspace admin hasn't enabled custom skills.

## 3. Use it

Just ask normally — Claude picks up the skill on its own when the task is visual:

- *"Build an Eupry landing page for our new wireless sensor."*
- *"Make an Eupry-branded email announcing a webinar."*
- *"Create a pricing card component in the Eupry style."*

If it ever doesn't trigger, nudge it: *"Use the Eupry Design System skill."*

## What's inside

- `SKILL.md` — the rules Claude follows (colors, type, components, logo, icons).
- `DESIGN.md` / `tokens.json` — full spec + tokens for anything not in SKILL.md.
- `fonts/` — Instrument Sans (Claude can copy these into projects it builds).
- `assets/eupry-squid.svg` — the Eupry logo.

## Updating

When the design system changes, download the new `.zip` and re-upload it (Claude Desktop
replaces the old version). Check the repo for the latest.

---

### For Claude Code users (not Desktop)

If you use the **Claude Code CLI** instead, you don't need the zip. Either:
- Drop the `eupry-design-system/` folder into `~/.claude/skills/`, or
- Just point Claude at this repo: *"Use the Eupry design system — read DESIGN.md and tokens.json."*
