
# Azure MCP Server Demo

This repository demonstrates how to start and use the Azure Model Context Protocol (MCP) Server with Node.js.

## Prerequisites

- Node.js (v14 or higher)
- Azure CLI (for authentication)


## Getting Started


### 0. Clone the Repository

First, clone this repository to your local machine:

```sh
git clone <repo-url>
cd <repo-directory>
```

### 0.1 Open in VS Code Dev Container

If you are using Visual Studio Code, open the repository in a Dev Container for a pre-configured development environment:

1. Open the folder in VS Code:
   - `code <repo-directory>`
2. When prompted, reopen in the Dev Container (or use the Command Palette: `Dev Containers: Reopen in Container`).



### 1. Login to Azure

Authenticate to your Azure tenant:

```sh
az login --tenant <tenant-id>
```


### 2. Start the Azure MCP Server

You can start the Azure MCP Server with a single command:

```sh
npx -y @azure/mcp@latest server start
```

Or, if using VS Code, use the provided `.vscode/mcp.json` configuration for one-click startup.

### 3. Explore Azure Resources

Once authenticated and the server is running, you can use the MCP server to interact with your Azure resources (e.g., list resource groups, query resources, etc).

## Project Structure


- `.vscode/mcp.json`: VS Code config for starting the Azure MCP Server
- `README.md`: This file
- `MCP-Architecture.png`: Architecture diagram (optional)

## Sample Prompts for Azure MCP Server

You can use the following prompts with GitHub Copilot Agent Mode or your custom MCP client to interact with your Azure resources:

```
List all of the resource groups in my subscription
List all of the storage accounts in my subscription
Get the available tables in my storage accounts
```

Example output for listing resource groups:

```
The following resource groups are available for your subscription:

1. **DefaultResourceGroup-EUS** (Location: `eastus`)
2. **rg-testing** (Location: `centralus`)
3. **rg-azd** (Location: `eastus2`)
4. **msdocs-sample** (Location: `southcentralus`)
14. **ai-testing** (Location: `eastus2`)

Let me know if you need further details or actions related to any of these resource groups!
```

For more sample prompts and details, see the [official documentation](https://learn.microsoft.com/en-us/azure/developer/azure-mcp-server/get-started?tabs=one-click%2Cazure-cli&pivots=mcp-github-copilot#use-prompts-to-test-the-azure-mcp-server).


## Resources

- [Azure MCP Documentation](https://github.com/Azure/mcp)
- [Azure MCP npm package](https://www.npmjs.com/package/@azure/mcp)
- [Get started with Azure MCP Server (Microsoft Learn)](https://learn.microsoft.com/en-us/azure/developer/azure-mcp-server/get-started?tabs=one-click%2Cazure-cli&pivots=mcp-github-copilot)

## License

This project is for demonstration purposes. For license details, see the [Azure MCP repository](https://github.com/Azure/mcp).
