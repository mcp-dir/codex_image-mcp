# Codex Imagem

### Codex Imagem for Claude, ChatGPT and AI agents

Generate images with your own ChatGPT subscription (Plus, Pro or Team), without spending API credits. Connect your Codex login once and ask for the image in plain language, the file is saved to your mcp.ai account.

- 📊 **2 tools**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `Codex Imagem`, URL `https://api.mcp.ai/p_codex_image`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=codex_image&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jb2RleF9pbWFnZSJ9)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=codex_image&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_codex_image%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_codex_image
```

---

## 2 tools

| Tool | Description |
|---|---|
| `codex_image_generate` | Gera uma imagem a partir de um texto, usando a cota de imagens da assinatura ChatGPT conectada (não consome créditos de API). |
| `codex_image_subscription` | Mostra qual assinatura ChatGPT está conectada (e-mail e plano). |

---

## Pricing

Free.

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_codex_image` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
