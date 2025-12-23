# Instalação do Supabase MCP Server

Como o ambiente atual não tem acesso ao `npm` para instalação automática, siga os passos abaixo para configurar o servidor MCP do Supabase no seu computador/IDE.

## 1. Pré-requisitos
Certifique-se de ter o **Node.js** instalado (v18 ou superior).

## 2. Instalação (Via CLI ou Configuração)

A maneira mais comum de usar o MCP Server é adicionando-o à configuração do seu Agente/IDE (ex: Cursor, Claude Desktop, Windsurf).

### Adicionar ao Arquivo de Configuração MCP
Localize o arquivo de configuração MCP do seu editor (geralmente em `~/.cursor/mcp.json` ou similar) e adicione:

```json
{
  "mcpServers": {
    "supabase": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-supabase"
      ],
      "env": {
        "SUPABASE_URL": "SUA_URL_DO_SUPABASE",
        "SUPABASE_KEY": "SUA_CHAVE_DO_SUPABASE"
      }
    }
  }
}
```

### Rodar Manualmente (Para teste)
Se quiser apenas testar o servidor rodando localmente:

```bash
npx -y @modelcontextprotocol/server-supabase
```

*Nota: Você precisará fornecer as variáveis de ambiente `SUPABASE_URL` e `SUPABASE_KEY` para que ele funcione corretamente.*
