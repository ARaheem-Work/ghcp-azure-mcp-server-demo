
# Azure MCP Server Demo

This repository demonstrates how to start and use the Azure Model Context Protocol (MCP) Server with Node.js.

## Prerequisites

- Node.js (v14 or higher)
- Azure CLI (for authentication)

## Getting Started

### 1. Login to Azure

Authenticate to your Azure tenant:

```sh
az login --tenant 01eb1391-a04e-4e61-861b-dab40420f7c9
```

### 2. Start the Azure MCP Server

Start the server:

```sh
npx -y @azure/mcp@latest server start
```

Or use the `.vscode/mcp.json` config:

```jsonc
{
  "servers": {
    "Azure MCP Server": {
      "command": "npx",
      "args": [
        "-y",
        "@azure/mcp@latest",
        "server",
        "start"
      ]
    }
  }
}
```

### 3. Explore Azure Resources

Once authenticated and the server is running, you can use the MCP server to interact with your Azure resources (e.g., list resource groups, query resources, etc).

## Project Structure

- `.vscode/mcp.json`: VS Code config for starting the Azure MCP Server
- `README.md`: This file
- `MCP-Architecture.png`: Architecture diagram (optional)

## Resources

- [Azure MCP Documentation](https://github.com/Azure/mcp)
- [Azure MCP npm package](https://www.npmjs.com/package/@azure/mcp)

## License

This project is for demonstration purposes. For license details, see the [Azure MCP repository](https://github.com/Azure/mcp).
