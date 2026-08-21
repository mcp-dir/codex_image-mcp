# Codex Imagem

### Codex Imagem para Claude, ChatGPT e agentes de IA

Gere imagens pela sua própria assinatura do ChatGPT (Plus, Pro ou Team), sem gastar créditos de API. Conecte o login do Codex uma vez e peça a imagem em linguagem natural, o arquivo fica salvo na sua conta do mcp.ai.

- 📊 **2 ferramentas**
- 🔒 **Somente leitura**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Login via magic-link (sem senha)**

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `Codex Imagem` e **URL** `https://api.mcp.ai/p_codex_image`.

### Cursor

[➕ Instalar Codex Imagem no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=codex_image&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jb2RleF9pbWFnZSJ9)

### VS Code (Copilot Chat)

[➕ Instalar Codex Imagem no VS Code](vscode:mcp/install?name=codex_image&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_codex_image%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_codex_image
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Gere uma imagem de um mascote de raposa para a minha marca, estilo flat
Crie uma foto de produto de uma caneca de cerâmica em fundo claro
Qual assinatura do ChatGPT está conectada aqui?
```

---

## 2 ferramentas disponíveis

| Tool | Descrição |
|---|---|
| `codex_image_generate` | Gera uma imagem a partir de um texto, usando a cota de imagens da assinatura ChatGPT conectada (não consome créditos de API). |
| `codex_image_subscription` | Mostra qual assinatura ChatGPT está conectada (e-mail e plano). |

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Grátis.

---

## Privacidade & LGPD

- **Somente leitura**, nenhuma ferramenta altera dados na origem.
- **Sub-processadores**: OpenAI, o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills — tudo MIT.

**Posso usar com agente próprio (não Claude/Cursor)?**
Sim — qualquer cliente que suporte MCP over HTTP. URL: `https://api.mcp.ai/p_codex_image`.


---

## Suporte

- 📧 [codex_image@mcp.ai](mailto:codex_image@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/codex_image-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_codex_image` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
