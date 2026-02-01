# Polyvia AI

**Visual Knowledge Index for Agents & MCPs**

Queryable index of facts for visual data.

[![Docs](https://img.shields.io/badge/docs-docs.polyvia.ai-blue)](https://docs.polyvia.ai)
[![Website](https://img.shields.io/badge/site-polyvia.ai-green)](https://polyvia.ai)
[![Studio](https://img.shields.io/badge/app-app.polyvia.ai-purple)](https://app.polyvia.ai)

Other solutions extract visuals or index text. Polyvia indexes and reasons over visuals — by connecting facts across your document corpus into a queryable knowledge base.

*"Pinecone for visual data" — but with agentic visual reasoning.*

Visual AI infrastructure layer for Agents & MCPs — visual search and reasoning at scale, on the ontology graph of connected facts.

## Quick Example

```python
from polyvia import Polyvia

client = Polyvia(api_key="...")

# Ingest financial reports
for doc in ["acme_10k_2024.pdf", "globex_10k_2024.pdf", "initech_10k_2024.pdf"]:
    client.ingest(doc)

# Query with natural language
result = client.query("Compare Acme and Globex Q4 2024 revenue")
print(result["answer"])
# → "Acme reported $12.4B vs Globex's $8.7B in Q4 2024"

for cite in result["citations"]:
    print(f"  Source: {cite['document']}, page {cite['page']}")
```

## How It Works

1. **Visual Extraction** — VLM-OCR extracts structured data from charts, tables, and diagrams
2. **Fact Indexing** — Facts are disambiguated and connected into a unified ontology
3. **Agentic Reasoning** — Query with natural language, get answers grounded in visual sources

## Products

| Product | Description |
|---------|-------------|
| [**Polyvia API**](https://docs.polyvia.ai/api-reference/introduction) | REST API for visual search and reasoning |
| [**Polyvia MCP Server**](https://docs.polyvia.ai/products/mcp) | Connect to Claude Desktop, Cursor, and MCP-compatible tools |
| [**Polyvia Studio**](https://app.polyvia.ai) | Web app for visual search and exploration |

## Getting Started

1. [Request access](https://polyvia.ai/#access) to Polyvia
2. Sign up at [app.polyvia.ai](https://app.polyvia.ai)
3. Get your API key from Settings
4. Follow the [Quickstart Guide](https://docs.polyvia.ai/quickstart)

## Links

- [Documentation](https://docs.polyvia.ai)
- [Website](https://polyvia.ai)
- [Blog](https://polyvia.ai/blog)

