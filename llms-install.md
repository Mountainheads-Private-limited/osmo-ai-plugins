# Installing OsmO Phone Calls (for AI agents such as Cline)

OsmO Phone Calls is a hosted remote MCP server. There is nothing to clone, build or run. Your client
connects to `https://api.getosmo.app/mcp` over Streamable HTTP. Then OsmO's voice AI can place real
phone calls for the user and read back the outcome, summary and transcript.

## 1. Add the server

There is **no API key**. The server uses OAuth 2.1 (PKCE, dynamic client registration), so your
client must support MCP OAuth sign-in. In Cline, add this to `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "osmo": {
      "type": "streamableHttp",
      "url": "https://api.getosmo.app/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

Other clients: add a remote/HTTP server named `osmo` with the same URL.

## 2. Sign in

On first use the client opens `https://api.getosmo.app/mcp/oauth/connect` in the browser. **The user**
enters their phone number and the one-time code there. Never ask for the code in chat, never type it
for the user, and never store it. New users in the US, Canada, the UK and Australia get 50 free credits. With free credits, OsmO calls businesses and toll-free numbers; calling your contacts and scheduling calls need an OsmO app plan.

## 3. Check it

Call `osmo_help`. It is read-only and places no call. It lists what this account can do.

**Do not call `place_call` as a test.** A confirmed call rings a real phone and uses credits.
`place_call` without `confirmed: true` only returns a preview. Show that preview to the user and send
`confirmed: true` only after they say yes. Keep `autoApprove` empty so the user approves each call.

## Notes

- With free credits, OsmO calls businesses and toll-free numbers; calling your contacts and scheduling calls need an OsmO app plan. It does not call emergency services, send text messages or send email.
- An answered call uses 3 credits; an unanswered call is free.
- Follow [`skills/osmo-phone-calls/SKILL.md`](skills/osmo-phone-calls/SKILL.md) for how to use the
  tools. Network details: [README, Authentication and network](README.md#authentication-and-network).
