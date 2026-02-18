# Nansen MCP Registry

This repository contains the registry metadata for Nansen's Model Context Protocol (MCP) server.

## MCP Server Details

- **Server URL**: `https://mcp.nansen.ai/ra/mcp`
- **Transport**: Streamable HTTP
- **Authentication**: API Key header (`NANSEN-API-KEY`)
- **Documentation**: https://docs.nansen.ai/mcp/connecting

## Registry Submission

The `server.json` file in this repository is used to register Nansen MCP server with:
- Official MCP Registry (registry.modelcontextprotocol.io)
- PulseMCP (pulsemcp.com)
- GitHub MCP (github.com/mcp)
- Other MCP aggregators

## Getting Started

To use Nansen MCP:

1. Get your API key at https://app.nansen.ai/api
2. Configure your MCP client with:
   - Server URL: `https://mcp.nansen.ai/ra/mcp`
   - Header: `NANSEN-API-KEY: your_api_key`

## Features

Access blockchain analytics for AI agents:
- Smart Money signals
- Wallet profiling
- Token analytics
- Exchange netflows  
- DeFi portfolio data
- 20+ chain coverage
- 400M+ labeled wallets