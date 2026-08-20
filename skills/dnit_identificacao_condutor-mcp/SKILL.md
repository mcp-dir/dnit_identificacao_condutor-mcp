---
name: dnit_identificacao_condutor-mcp
description: Skill da REST API do DNIT: Identificação de Condutor Infrator na MCP.AI: 1 endpoint em /api/dnit_identificacao_condutor. DNIT: Identificação de Condutor Infrator, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# DNIT: Identificação de Condutor Infrator — REST API skill

Você tem acesso à **DNIT: Identificação de Condutor Infrator** REST API na MCP.AI.

> DNIT: Identificação de Condutor Infrator, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/dnit_identificacao_condutor
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/dnit_identificacao_condutor/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"usuario":"...","senha":"...","ait":"...","nome":"...","cpf":"...","rg":"...","cnh":"...","pais":"...","uf":"...","url_formulario":"...","url_cnh":"...","url_documento":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/dnit_identificacao_condutor/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `dnit_identificacao_condutor_consultar`

DNIT: Identificação de Condutor Infrator, consulta em fonte oficial. _(POST /api/dnit_identificacao_condutor/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `usuario` | string | Sim | Parâmetro de consulta "usuario". |
| `senha` | string | Sim | Parâmetro de consulta "senha". |
| `ait` | string | Sim | Parâmetro de consulta "ait". |
| `nome` | string | Sim | Parâmetro de consulta "nome". |
| `cpf` | string | Sim | Parâmetro de consulta "cpf". |
| `rg` | string | Sim | Parâmetro de consulta "rg". |
| `cnh` | string | Sim | Parâmetro de consulta "cnh". |
| `pais` | string | Sim | Parâmetro de consulta "pais". |
| `uf` | string | Sim | Parâmetro de consulta "uf". |
| `url_formulario` | string | Sim | Parâmetro de consulta "url_formulario". |
| `url_cnh` | string | Sim | Parâmetro de consulta "url_cnh". |
| `url_documento` | string | Sim | Parâmetro de consulta "url_documento". |
| `url_procuracao` | string | Não | Parâmetro de consulta "url_procuracao". |
| `url_outros` | string | Não | Parâmetro de consulta "url_outros". |
| `doenca_deficiencia` | string | Não | Parâmetro de consulta "doenca_deficiencia". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_dnit_identificacao_condutor` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
