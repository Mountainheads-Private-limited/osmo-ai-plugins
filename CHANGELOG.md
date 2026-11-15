# Changelog

## 1.3.0

- New skill `osmo-ai-receptionist`: run your OsmO AI phone receptionist from your AI app (missed calls, greeting, caller rules, bookings).
- Receptionist keywords in every plugin manifest.

## 1.2.0

- Antigravity plugin (`.antigravity-plugin/plugin.json`, `mcp_config.json`). Sign-in uses OAuth client metadata documents, so no client id is needed.
- Skill 1.0.3: the description now starts "Make phone calls with AI".

## 1.1.0

- Claude Code plugin and marketplace (`.claude-plugin/`): `/plugin marketplace add Mountainheads-Private-limited/osmo-ai-plugins`.
- Codex plugin (`.codex-plugin/plugin.json`): `codex plugin marketplace add Mountainheads-Private-limited/osmo-ai-plugins`.
- Cursor plugin: display name, repository and skills path.
- `llms-install.md` for agents such as Cline. `assets/logo.png` is now 400×400 and under 50 KB (catalog icon limits).
- `server.json` with the repository link for the MCP Registry.
- `SECURITY.md`, `CONTRIBUTING.md`, issue templates.
- README: setup for every supported app, one-click Cursor and VS Code install, tool table, cost, and
  what it can't do. Fixed the OpenClaw install command (`openclaw skills install @getosmo/osmo-phone-calls`).
- Skill 1.0.2: Claude Code and Codex connect steps; who OsmO can call.

## 1.0.0

- First release: Agent Skill, Cursor plugin, Gemini CLI extension.
