# Azure MCP Server Demo

This repository demonstrates how to start and use the Azure Model Context Protocol (MCP) Server using Node.js and the Azure MCP package.

## Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher recommended)
- [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli) (for authentication)

## Getting Started

### 1. Install Dependencies

No dependencies need to be installed in advance. The server will be started using `npx`, which downloads and runs the latest version of the Azure MCP package automatically.

### 2. Start the Azure MCP Server

You can start the Azure MCP Server using the following command:

```sh
npx -y @azure/mcp@latest server start
```

Alternatively, if you are using a tool or extension that reads the `.vscode/az-mcp-server.json` file, it will use the following configuration:

```
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
### 3. Login to Azure Tenant

You can login to the Azure tenant using Azure CLI command:
```sh
az login --tenant 01eb1391-a04e-4e61-861b-dab40420f7c9
```

## Project Structure

- `.vscode/az-mcp-server.json`: VS Code configuration for starting the Azure MCP Server.

## Resources

- [Azure Model Context Protocol (MCP) Documentation](https://github.com/Azure/mcp)
- [Azure MCP npm package](https://www.npmjs.com/package/@azure/mcp)

## License

This project is for demonstration purposes. See the [Azure MCP repository](https://github.com/Azure/mcp) for license details.
