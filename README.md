# Polyvia - Developer Docs

**Polyvia: Multimodal Document Agents over 100K+ files.** We build enterprise agents for large-scale retrieval, research and automation over multimodal docs. We're releasing our first product as part of **Polyvia-1.0: Polyvia API — Multimodal Document Retrieval API for developers of AI agents.**

Agentic, file-by-file search works only up to ~100 multimodal files — past that it's too slow. So at scale, when you're connecting an enterprise's large internal datasets, you still need retrieval. And the multimodal infra tools today stop at visual extractors / PDF parsers. We built **Polyvia Engine** - an end-to-end pipeline for multimodal document intelligence.

We index your visual & multimodal docs (charts, slides, complex tables, infographics, scans, handwriting, invoices, and more), with agents on top for retrieval, research and automation — every answer grounded in a cited source page, in sub-200ms.

[![Docs](https://img.shields.io/badge/docs-docs.polyvia.ai-blue)](https://docs.polyvia.ai)
[![Website](https://img.shields.io/badge/site-polyvia.ai-green)](https://polyvia.ai)
[![Studio](https://img.shields.io/badge/app-app.polyvia.ai-purple)](https://app.polyvia.ai)

## Quick Example

Ingest and query across a whole corpus. Ingest a batch into a **group**, then ask one question across all of it.

```python
from polyvia import Polyvia

client = Polyvia(api_key="poly_<key>")

# Ingest several files into a group
items = client.ingest.batch(
    ["q1.pdf", "q2.pdf", "q3.pdf", "q4.pdf"],
    group="FY24 Earnings",
)

for item in items:
    client.ingest.wait(item.task_id)

# Ask once, across the group — answers cite the exact page in each doc
answer = client.query(
    "How did revenue trend across the four quarters?",
    group="FY24 Earnings"
)
print(answer.answer)
```

## Polyvia Engine

One pipeline turns scattered visual & multimodal files into a queryable knowledge layer — then answers in sub-200ms, grounded in a visual citation.

1. **Visual Extractor** — Reads the hardest visual documents (charts, infographics, complex multi-page tables, slides, scans, handwriting, pictures) into structured facts.
2. **Multimodal Knowledge Ontology** — Disambiguates and connects every extracted fact into one semantic ontology over your whole corpus — a single, queryable source of truth.
3. **Agentic Retrieval with Memory** — Agentic, multi-hop retrieval that self-improves over time. Every answer grounded in a visual citation tied to the exact source page.

## Products: API for developers, Platform for teams

**Polyvia-1.0** ships the **Polyvia API** — available now. Next is **Polyvia-1.1** (the Platform), and soon after, **Polyvia Agents**.

| Product | Description | Status |
|---------|-------------|--------|
| [**Polyvia API**](https://docs.polyvia.ai/products/api) | Multimodal Document Retrieval API, for developers of AI agents | **Available now (1.0)** |
| [**Polyvia Platform**](https://docs.polyvia.ai/products/platform) | Research and Automation Agent over 100K+ multimodal docs, for knowledge workers in enterprises | **Coming next (1.1)** |
| **Polyvia Agents** | Build your own agent for automating processes on large volumes of multimodal documents | **Soon after** |

## Getting Started

1. [Request access](https://polyvia.ai/#access) to Polyvia
2. Sign up at [app.polyvia.ai](https://app.polyvia.ai)
3. Get your API key from Settings
4. Follow the [Quickstart Guide](https://docs.polyvia.ai/quickstart)

## Links

- [Documentation](https://docs.polyvia.ai)
- [Website](https://polyvia.ai)
- [Blog](https://polyvia.ai/blog)
