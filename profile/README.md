# 0xArchive

Granular market data infrastructure for Hyperliquid and Lighter.xyz.

Hyperliquid includes core perps, HIP-3 builder perps, HIP-4 outcome markets, and Hyperliquid Spot. Lighter.xyz is the second top-level venue API. 0xArchive gives developers, analysts, Claude Code users, ChatGPT Codex users, and agent builders one API surface for live and historical order books, trades, candles, funding, open interest, liquidations, replay, data-quality checks, SDKs, CLI, MCP, skills, and file exports.

## Start With One Request

1. Create an account: [0xArchive signup](https://www.0xarchive.io/signup).
2. Copy an API key.
3. Run the [Quick Start](https://www.0xarchive.io/docs/quick-start).
4. Choose the repo that matches the job.

## Choose A Repo

| Job | Repo | First path |
| --- | --- | --- |
| Use an SDK in Python | [sdk-python](https://github.com/0xArchiveIO/sdk-python) | `pip install oxarchive` |
| Use an SDK in TypeScript | [sdk-typescript](https://github.com/0xArchiveIO/sdk-typescript) | `npm install @0xarchive/sdk` |
| Use an SDK in Rust | [sdk-rust](https://github.com/0xArchiveIO/sdk-rust) | `cargo add oxarchive` |
| Use the terminal, CI, cron, Claude Code, or ChatGPT Codex shells | [0xarchive-cli](https://github.com/0xArchiveIO/0xarchive-cli) | `npm install @0xarchive/cli` |
| Use typed MCP tools in Claude Code, ChatGPT Codex setups with MCP enabled, or other MCP-capable clients | [0xarchive-mcp](https://github.com/0xArchiveIO/0xarchive-mcp) | `npm install @0xarchive/mcp-server` |
| Use a local skill package in Claude Code, ChatGPT Codex with skills enabled, or another skill-capable coding agent | [0xarchive-skill](https://github.com/0xArchiveIO/0xarchive-skill) | Copy into `.claude/skills/0xarchive` or `.agents/skills/0xarchive`. Optional OpenClaw helper: `openclaw install 0xarchive` |
| Inspect working notebooks before wiring a client | [examples](https://github.com/0xArchiveIO/examples) | Run the liquidation, funding, or HIP-3 notebook |

## Public Surfaces

- First request: [Quick Start](https://www.0xarchive.io/docs/quick-start)
- SDKs: [SDK docs](https://www.0xarchive.io/docs/sdks)
- CLI: [CLI docs](https://www.0xarchive.io/docs/cli)
- Agents: [AI Clients](https://www.0xarchive.io/docs/ai-clients)
- File exports: [Data Catalog](https://www.0xarchive.io/data)
- Plans and limits: [Pricing](https://www.0xarchive.io/pricing)
- Status and changes: [Status](https://www.0xarchive.io/status), [Changelog](https://www.0xarchive.io/changelog)
- Machine-readable context: [llms.txt](https://www.0xarchive.io/llms.txt), [OpenAPI](https://www.0xarchive.io/openapi.json)

## Agent Safety

Start local. Give agents the narrowest key and tool scope that can answer the first question. Treat MCP servers, shell commands, and skills as real code with real access. Claude Code and ChatGPT Codex should use the same 0xArchive product truth: one authenticated request first, then expand into SDKs, CLI, MCP, skills, replay, or Data Catalog exports after the result is concrete.

## Venue Model

- Hyperliquid: `/v1/hyperliquid/*`
- Hyperliquid HIP-3: `/v1/hyperliquid/hip3/*`
- Hyperliquid HIP-4: `/v1/hyperliquid/hip4/*`
- Hyperliquid Spot: `/v1/hyperliquid/spot/*`
- Lighter.xyz: `/v1/lighter/*`

HIP-3, HIP-4, and Spot are Hyperliquid-scoped market families, not peer top-level venues beside Hyperliquid and Lighter.xyz.

For large offline studies, use the Data Catalog to quote and export zstd-compressed Parquet. For production systems, use REST, WebSocket, SDKs, CLI, or MCP.
