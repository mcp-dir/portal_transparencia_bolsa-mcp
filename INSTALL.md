# Instalação rápida

Portal da Transparência: Bolsa Família é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_portal_transparencia_bolsa`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Portal da Transparência: Bolsa Família` / `https://api.mcp.ai/p_portal_transparencia_bolsa`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "portal_transparencia_bolsa": { "type": "http", "url": "https://api.mcp.ai/p_portal_transparencia_bolsa" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=portal_transparencia_bolsa&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wb3J0YWxfdHJhbnNwYXJlbmNpYV9ib2xzYSJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "portal_transparencia_bolsa": { "url": "https://api.mcp.ai/p_portal_transparencia_bolsa" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=portal_transparencia_bolsa&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_portal_transparencia_bolsa%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "portal_transparencia_bolsa": { "type": "http", "url": "https://api.mcp.ai/p_portal_transparencia_bolsa" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_portal_transparencia_bolsa
```

Dúvidas? [portal_transparencia_bolsa@mcp.ai](mailto:portal_transparencia_bolsa@mcp.ai)
