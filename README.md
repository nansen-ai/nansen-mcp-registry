# Nansen MCP Registry

This repository holds Nansen's entry in the [Official MCP Registry](https://registry.modelcontextprotocol.io/v0/servers?search=io.github.nansen-ai/nansen-mcp). Glama, PulseMCP and other MCP directories import from that registry, so a change here reaches them too.

## Servers

| Server | URL | Sign-in |
|---|---|---|
| Full tool catalog | `https://mcp.nansen.ai/ra/mcp` | `NANSEN-API-KEY` header |
| Curated tools | `https://mcp.nansen.ai/ra/connector-curated/mcp` | Nansen account through OAuth |

Setup guide: https://docs.nansen.ai/mcp/overview

## Updating the registry entry

1. Edit `server.json` and raise `version`. The registry never lets a version be published twice.
2. Open a pull request. CI validates the file with `mcp-publisher validate`.
3. Merge to `main`. The `MCP Registry` workflow publishes the new version through GitHub Actions OIDC. No personal token or org Owner login is involved.

To deprecate an old version, add it to `deprecated` in `registry-status.json` with a short message and merge. The workflow skips versions that are already deprecated.

Keep chain counts and tool counts out of `server.json`. They change often, and the docs are the source of truth for both.

## Checking the live entry

```bash
curl -s 'https://registry.modelcontextprotocol.io/v0/servers?search=io.github.nansen-ai/nansen-mcp' | jq '.servers[] | {version: .server.version, meta: ._meta}'
```
