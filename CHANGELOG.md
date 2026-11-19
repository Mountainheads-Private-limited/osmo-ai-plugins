# Changelog

## 1.6.0

- Three new skills, one job each, on the same OsmO MCP server and sign-in:
  - `osmo-call-screening`: screen calls to your own number (spam calls, missed calls, the caller's message instead of voicemail, block and VIP lists, caller rules).
  - `osmo-customer-service-calls`: call a company's customer care line, get through the phone menu, wait on hold and bring back the answer.
  - `osmo-book-by-phone`: restaurant reservations and appointments made, moved or cancelled by a phone call.
- Call-screening, spam-call, customer-service and reservation keywords in the plugin manifests.

## 1.5.0

- Describes MCP release 12: a live call card in AI apps that show MCP Apps cards (such as Claude) — Confirm, the call's progress, summary, recording player, Call again / Schedule; up to 5 calls placed together in one card.
- Scheduled calls in your own time zone: wall-clock time plus an IANA `timeZone` (daylight-saving safe); `list_scheduled_calls` shows local times.
- After a call, a ready result can offer to call again now or later with the same words (`callAgain`).
- In Claude and ChatGPT a status check waits for a short call to finish, so the result comes back in the same turn.
- A confirmed call is placed once (`confirmKey`; a repeat answers `already_placed`).
- Skill `osmo-phone-calls` 1.2.0 and `GEMINI.md`: confirmKey, call card, call-again offer and time-zone steps.
- Skill `osmo-ai-receptionist` 1.2.0: call-backs at a time in your own time zone, shown on the call card where the app supports cards.

## 1.4.0

- Every manifest describes all 27 tools of MCP release 11: calls (up to 5 numbers, scheduling, recordings, call-backs) and the AI receptionist (pause the AI, put-through, VIP and block lists, caller rules, assistant language, bookings, Facts, connections).
- Skill `osmo-phone-calls` 1.1.0: how to find numbers, call contacts and recent callers, schedule and cancel calls, open recordings and app chats, and read the account status.
- Skill `osmo-ai-receptionist` 1.1.0: removed the greeting claim (the greeting, names and voice are changed in the OsmO app); added pause AI, VIP and block lists, assistant and language, Facts, connections, recordings, tagging people in rules, upcoming and past bookings.
- `GEMINI.md` now covers the receptionist too.

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
