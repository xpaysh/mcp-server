# xpay MCP Server

980+ AI tools available as MCP servers. Pay $0.01/call in USDC via the [x402 protocol](https://x402.org) — no API keys, no subscriptions.

Connect to one endpoint and get access to 30+ providers including Hunter, Firecrawl, Perplexity, Financial Modeling Prep, FLUX, and more.

## Quick Start

Add to your MCP client config (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "xpay": {
      "url": "https://mcp.xpay.sh/sse"
    }
  }
}
```

That's it. When you call a tool, the server responds with HTTP 402 + a payment invoice. Your client pays $0.01 USDC automatically and the tool executes.

## Collection Servers

Each collection bundles related tools into a focused MCP server:

| Collection | Endpoint | Tools | Providers |
|---|---|---|---|
| **All Tools** | `https://mcp.xpay.sh/sse` | 980+ | All 30+ |
| **Lead Generation** | `https://lead-gen.mcp.xpay.sh/sse` | ~50 | Hunter, Apollo, Tomba, Sixtyfour, Fiber, Exa, Nyne |
| **Competitive Intel** | `https://compete.mcp.xpay.sh/sse` | ~40 | Brand.dev, Coresignal, Keywords Everywhere, Exa, Firecrawl, Shofo |
| **Content Research** | `https://content.mcp.xpay.sh/sse` | ~40 | Perplexity, Tavily, Semantic Scholar, FLUX, Ideogram, Recraft |
| **Web Scraping** | `https://scraping.mcp.xpay.sh/sse` | ~35 | Firecrawl, Bright Data, Jina, Olostep, ScrapeGraph, Notte |
| **Developer Tools** | `https://devtools.mcp.xpay.sh/sse` | ~30 | Context7, Code Runner, Python Execute, NPM Sentinel, PlantUML |
| **Finance** | `https://finance.mcp.xpay.sh/sse` | 253 | Financial Modeling Prep, Alpha Vantage, AkShare, Polymarket |
| **Media Studio** | `https://media.mcp.xpay.sh/sse` | ~25 | FLUX, Ideogram, Recraft, Stability AI, MiniMax, Kokoro |
| **Social Media** | `https://social.mcp.xpay.sh/sse` | 96 | ScapeCreators, Shofo, YouTube |
| **Academic Research** | `https://research.mcp.xpay.sh/sse` | ~30 | Semantic Scholar, Google Scholar, PubMed, arXiv |
| **Marketing** | `https://marketing.mcp.xpay.sh/sse` | ~30 | Keywords Everywhere, Brand.dev, Exa, Tavily, Ideogram |

## How It Works

1. **Connect** — Add any endpoint above to your MCP client config
2. **Call a tool** — Your AI assistant discovers and calls tools naturally
3. **Auto-pay** — The server returns HTTP 402; your client pays $0.01 USDC on [Base](https://base.org)
4. **Get results** — Tool executes and returns data instantly

No API key management. No provider accounts. No subscriptions. Just tools that work.

## Requirements

- USDC on Base network ([get USDC on Coinbase](https://www.coinbase.com))
- Any MCP-compatible client (Claude Desktop, Cursor, Windsurf, Cline, etc.)

## How x402 Works

[x402](https://x402.org) is an open protocol for machine-to-machine payments using HTTP 402 Payment Required. When a tool call requires payment:

1. Server responds with `402 Payment Required` + a payment invoice
2. Client signs a USDC payment on Base blockchain
3. Server verifies payment and executes the tool
4. Settlement is instant, non-custodial, and peer-to-peer

## Browse Tools

- **Hub**: [xpay.tools](https://xpay.tools)
- **Docs**: [docs.xpay.sh](https://docs.xpay.sh)
- **Platform**: [xpay.sh](https://xpay.sh)

## Related

- [`@xpaysh/x402`](https://www.npmjs.com/package/@xpaysh/x402) — x402 facilitator SDK
- [`@xpaysh/n8n-nodes-xpay`](https://www.npmjs.com/package/@xpaysh/n8n-nodes-xpay) — n8n community node
- [`@xpaysh/agent-kit-langchain`](https://www.npmjs.com/package/@xpaysh/agent-kit-langchain) — LangChain integration
- [xpay Facilitator](https://facilitator.xpay.sh) — Open x402 facilitator service

## License

MIT
