# Workbench MCP icons + Cursor marketplace

Public logos and Cursor plugin packs for local Workbench MCP endpoints
(`127.0.0.1`). No secrets in this repo — auth uses `${env:WORKBENCH_MCP_TOKEN}`.

## Install (icons visible in Cursor)

`~/.cursor/plugins/local` **does not render** logos
([plugin-template#7](https://github.com/cursor/plugin-template/issues/7)).
Install from this **public** marketplace instead:

```text
/add-plugin https://github.com/ivanlark2000/workbench-mcp-icons
```

Or: Dashboard → Plugins → Team Marketplaces → Import from Repo → same URL.

Then install the plugins you need → **Developer: Reload Window**.

Keep only non-plugin servers in `~/.cursor/mcp.json` (engram / doppler / docs)
to avoid duplicates.

## Layout

Each plugin directory:

- `.cursor-plugin/plugin.json` — manifest (`logo`: `assets/logo.svg`)
- `mcp.json` — localhost MCP endpoint
- `logo.svg` — CDN-compatible path
- `assets/logo.svg` — Cursor marketplace logo

Root `.cursor-plugin/marketplace.json` lists all plugins.

## CDN

```text
https://cdn.jsdelivr.net/gh/ivanlark2000/workbench-mcp-icons@master/<plugin>/logo.svg
```
