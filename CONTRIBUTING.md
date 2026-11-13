# Contributing

Thanks for helping. This repo holds the **client side** of OsmO Phone Calls: the Agent Skill and
the config files that connect AI apps to OsmO's hosted MCP server. The server itself is not in this
repo.

Useful contributions:

- **A setup step that is wrong or out of date for your client.** Open an issue or a PR with the
  client name, its version and what you ran.
- **Setup for a client we don't cover yet.** Include the exact config and the client's own docs
  link, and say whether you completed sign-in and placed or previewed a call.
- **Skill wording that led an agent astray.** For example, it called without confirming or invented
  a result. Describe the prompt and what happened.

Please:

- Keep every manifest valid JSON. Run `python3 -m json.tool <file>` for each one you touch. For the
  Claude Code plugin, also run `claude plugin validate .`.
- Keep `version` in the manifests, `server.json` and `CHANGELOG.md` in step when you change behaviour.
- Never commit an access token, phone number, call transcript or recording link. Redact them in
  issues too.
- Don't add scripts, hooks or dependencies. This repo intentionally has no executable code.

Questions: team@getosmo.app.
