# AgingResearch.News MCP server

<img src="https://agingresearch.news/logo.png" alt="AgingResearch.News" width="96" height="96">

Every new aging paper, read the minute it lands and judged on what its own work shows. Ask Claude, ChatGPT, Cursor, VS Code or any MCP client about a drug, a gene, an aging clock or a trial, and get answers that cite the papers.

## Add it

Paste this address into your client as a remote MCP server (Streamable HTTP):

```text
https://agingresearch.news/api/mcp
```

Lookups work without an account, up to a daily number. Sign in with a free AgingResearch.News account to follow topics and ask your own questions.

Steps for each client: [agingresearch.news/connect](https://agingresearch.news/s/f7623w) · Every tool and its arguments: [developer docs](https://agingresearch.news/s/yq2dkg)

**Claude Code**

```bash
claude mcp add --transport http agingresearch-news https://agingresearch.news/api/mcp
```

**VS Code** (`.vscode/mcp.json`)

```json
{
  "servers": {
    "agingresearch-news": { "type": "http", "url": "https://agingresearch.news/api/mcp" }
  }
}
```

**Cursor** (`~/.cursor/mcp.json`)

```json
{
  "mcpServers": {
    "agingresearch-news": { "url": "https://agingresearch.news/api/mcp" }
  }
}
```

## Ask it

- "What human evidence is there for rapamycin in aging? Keep animal and human studies apart and list the findings against."
- "Find this month's papers on cellular senescence in pulmonary fibrosis, with a link to each paper."
- "Which senolytic drugs are in clinical trials, and which trials have posted results?"
- "Who funds work on epigenetic clocks, and how much?"

Then say "Follow cellular senescence for me", and its new papers reach your For you feed and a daily email.

## What it covers

- Papers from PubMed, bioRxiv, medRxiv, arXiv and Europe PMC, each with its study type (human trial, human observational, animal, cells, in silico, review) and whether it is a preprint.
- Plain-language stories on the papers worth reading.
- Drugs, supplements, genes, biological processes, diseases and biomarkers, with their findings, contrary findings and replication across labs.
- Clinical trials, research grants (NIH, the EU, UKRI and Wellcome), conferences and their abstracts, drug and therapy programs in development, and the field's news.

Tools: `search_papers`, `list_papers`, `get_paper`, `list_stories`, `find_entities`, `get_entity`, `list_claims`, `list_trials`, `get_trial`, `list_news`, `list_grants`, `list_conferences`, `get_conference`, `list_assets`, `get_asset`, `count_pipeline`, `ask_arn`, `start_ultradeep`, `get_ask_answer`, `follow`, `unfollow`, `list_follows`, `list_questions`.

## Read it on the web

[Cellular senescence](https://agingresearch.news/s/rz7hr2) · [Epigenetic clocks](https://agingresearch.news/s/wkh9e7) · [RSS and topic feeds](https://agingresearch.news/s/p6hpky)

This repository holds the server's public connection manifest ([`server.json`](server.json), the record in the official MCP Registry as `news.agingresearch/agingresearch-news`). The service itself is hosted by AgingResearch.News.

## License

The files in this repository are under the [MIT License](LICENSE); the AgingResearch.News name and logo are not. To cite it, use [`CITATION.cff`](CITATION.cff).
