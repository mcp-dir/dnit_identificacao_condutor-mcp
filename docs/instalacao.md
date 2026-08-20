# Instalação detalhada

DNIT: Identificação de Condutor Infrator é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_dnit_identificacao_condutor`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_dnit_identificacao_condutor` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_dnit_identificacao_condutor` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_dnit_identificacao_condutor` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.dnit_identificacao_condutor` (ou `servers.dnit_identificacao_condutor` no VS Code) do config do cliente e reinicie.
