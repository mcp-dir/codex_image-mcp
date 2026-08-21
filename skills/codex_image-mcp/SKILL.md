---
name: codex_image-mcp
description: Skill da REST API do Codex Imagem na MCP.AI: 2 endpoints em /api/codex-image. Gere imagens pela sua própria assinatura do ChatGPT (Plus, Pro ou Team), sem gastar créditos de API. Conecte o login do Codex uma vez e peça a imagem em linguagem natural, o arquivo fica salvo na sua conta do mcp.ai. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Codex Imagem — REST API skill

Você tem acesso à **Codex Imagem** REST API na MCP.AI.

> Gere imagens pela sua própria assinatura do ChatGPT (Plus, Pro ou Team), sem gastar créditos de API. Conecte o login do Codex uma vez e peça a imagem em linguagem natural, o arquivo fica salvo na sua conta do mcp.ai.

## Base URL

```
https://api.mcp.ai/api/codex-image
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
curl -X POST https://api.mcp.ai/api/codex-image/generate \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"prompt":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/codex-image/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (2)

#### `codex_image_generate`

Gera uma imagem a partir de um texto, usando a cota de imagens da assinatura ChatGPT conectada (não consome créditos de API). _(POST /api/codex-image/generate)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `prompt` | string | Sim | Descrição da imagem. Quanto mais concreto (cena, assunto, estilo, iluminação, texto exato entre aspas), melhor o resultado. |
| `account` | string | Não | Qual assinatura ChatGPT usar (e-mail ou id da conexão). Só é necessário quando há mais de uma conectada. |

#### `codex_image_subscription`

Mostra qual assinatura ChatGPT está conectada (e-mail e plano). _(POST /api/codex-image/subscription)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `account` | string | Não | Qual assinatura ChatGPT usar (e-mail ou id da conexão). Só é necessário quando há mais de uma conectada. |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_codex_image` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
