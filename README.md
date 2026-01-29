# Polyvia AI Documentation

Documentation for [Polyvia AI](https://polyvia.ai) - the Visual Knowledge Index for Agents & MCPs.

## What is Polyvia?

Polyvia is visual search and reasoning infrastructure. We extract, index, and reason over charts, slides, and diagrams - turning scattered visuals into a queryable index of facts.

## Documentation Structure

### Getting Started
- **Introduction** - Overview of Polyvia and the visual knowledge pipeline
- **Quickstart** - Get up and running in minutes

### Products
- **Polyvia API** - REST API for visual search and reasoning
- **Polyvia MCP Server** - Connect Polyvia to Claude Desktop, Cursor, and MCP-compatible tools
- **Polyvia Studio** - Web app for visual search and exploration

### API Reference
- **Overview** - Authentication, base URL, rate limits
- **Endpoints**
  - `/ingest` - Upload and index documents
  - `/query` - Search and reason over your knowledge base

## Development

This documentation is built with [Mintlify](https://mintlify.com).

```bash
# Install Mintlify CLI
npm i -g mint

# Run local preview
mint dev
```

Preview at `http://localhost:3000`

## Links

- Website: [polyvia.ai](https://polyvia.ai)
- Studio: [app.polyvia.ai](https://app.polyvia.ai)
- Docs: [docs.polyvia.ai](https://docs.polyvia.ai)
