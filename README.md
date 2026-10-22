# Youshow IELTS MCP Server

Read-only MCP server for IELTS Writing Task 2 sample answers, Speaking Part 2 cue card topics and Writing band descriptors. No API key required.

Hosted, read-only and public: no API key, no account, no install step.

| | |
| --- | --- |
| **Endpoint** | `https://ielts.youshowedu.com/api/mcp` |
| **Transport** | streamable-http (POST, JSON-RPC 2.0, stateless, anonymous, CORS enabled) |
| **Authentication** | none |
| **Server card** | https://ielts.youshowedu.com/.well-known/mcp/server-card.json |
| **Product** | https://ielts.youshowedu.com |
| **MCP guide** | https://ielts.youshowedu.com/en/mcp |

## Tools

| Tool | Description |
| --- | --- |
| `list_writing_samples` | List public IELTS Writing Task 2 sample answers with prompts, source papers, reference bands, word counts and previews. |
| `get_writing_sample` | Read one public IELTS Writing Task 2 model essay in full by sample ID. |
| `list_cue_cards` | List public IELTS Speaking Part 2 cue card topics with prompts, points to cover and related Part 3 questions. |
| `get_band_descriptors` | Get the four IELTS Writing assessment criteria and plain-language Band 5 to Band 8 summaries. |

## Connect a client

### Claude Code

```bash
claude mcp add --transport http youshow-ielts https://ielts.youshowedu.com/api/mcp
```

### Cursor, VS Code, Windsurf or any other MCP client

Add a remote MCP server with the endpoint URL:

```
https://ielts.youshowedu.com/api/mcp
```

### Verify the endpoint by hand

```bash
curl -X POST https://ielts.youshowedu.com/api/mcp \
  -H 'Content-Type: application/json' \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
```

## About

This repository holds the published metadata for the hosted MCP server behind
https://ielts.youshowedu.com. The server itself is deployed and operated by the product team;
this repository exists so that MCP directories and registries can link to a
public source of truth.

- Product: https://ielts.youshowedu.com
- MCP guide: https://ielts.youshowedu.com/en/mcp
- Contact: official@youshowedu.com

## License

MIT
