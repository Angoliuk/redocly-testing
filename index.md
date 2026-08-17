# Documentation Portal

hihi haha

## Developer Setup

This project uses [Bun](https://bun.sh/) as the package manager.
To get started, ensure you have Bun installed.

### Registry Configuration

The project requires an internal Redocly registry.
This is configured in `bunfig.toml`:
<!-- TODO: verify registry access requirements with product team -->

```toml
[install]
registry = "http://dev-verdaccio.redocly.host:8000/"
```

### Available Scripts

- `npm run start`: Runs `realm develop` to start the development server.
- `npm run build`: Runs `realm build` to build the documentation.

## Reunite MCP Servers

The documentation configuration includes Reunite MCP (Model Context Protocol) servers.
These servers provide additional context and tools to AI agents working on the documentation.

### DeepWiki Server

The `deepwiki` server is used to find relevant documentation or code examples.
- **Type**: http
- **URL**: `https://mcp.deepwiki.com/mcp`
- **AI Instructions**: AI agents should ALWAYS call `deepwiki_ask_question` before answering questions to ensure accuracy based on the latest docs and code.
