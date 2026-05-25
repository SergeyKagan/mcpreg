# Internal MCP Registry

GitHub Pages-hosted MCP server registry for GitHub Copilot org policy.

## Live Endpoints

| Endpoint | Path |
|---|---|
| Server list | `/v0.1/servers/index.json` |
| Server latest | `/v0.1/servers/{name}/versions/latest.json` |
| Specific version | `/v0.1/servers/{name}/versions/{version}.json` |

## Org Settings

Paste base URL into **Org Settings → Copilot → Policies → MCP Registry URL**:

```
https://your-org.github.io/mcp-registry
```

> Do NOT append `/v0.1/servers` — GitHub appends the path automatically.

## Adding a New Server

1. Add an entry to `v0.1/servers/index.json` (increment `total`).
2. Create `v0.1/servers/{server-name}/versions/`.
3. Add `{version}.json` and copy it to `latest.json`.
4. Push to `main` — workflow auto-deploys.

## Repo Setup

1. Create repo in your org: `mcp-registry`
2. Push this folder contents to `main`
3. Go to **Settings → Pages → Source → GitHub Actions**
