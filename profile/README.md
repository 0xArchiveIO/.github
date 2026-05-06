# 0xArchive

Granular market data infrastructure for Hyperliquid and Lighter.xyz.

HIP-3 builder perps, HIP-4 outcome markets, and Hyperliquid spot pairs all live under the Hyperliquid namespace. 0xArchive gives developers, analysts, Claude Code users, GPT Codex users, and agent builders one API surface for live and historical order books, trades, candles, funding, open interest, liquidations, HIP-4 outcome markets, spot pairs, replay, data-quality checks, SDKs, CLI, MCP, skills, and file exports.

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
| Use the terminal, CI, cron, Claude Code, or GPT Codex shells | [0xarchive-cli](https://github.com/0xArchiveIO/0xarchive-cli) | `npm install -g @0xarchive/cli` |
| Use typed MCP tools in Claude Code, Codex CLI or IDE setups with MCP enabled, or other MCP-capable clients | [0xarchive-mcp](https://github.com/0xArchiveIO/0xarchive-mcp) | `npm install -g @0xarchive/mcp-server` |
| Use a local skill package in Claude Code, Codex with skills enabled, OpenClaw, or other skill-capable clients | [0xarchive-skill](https://github.com/0xArchiveIO/0xarchive-skill) | `git clone https://github.com/0xArchiveIO/0xarchive-skill ~/.claude/skills/0xarchive` |
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

Start local. Give agents the narrowest key and tool scope that can answer the first question. Treat MCP servers, shell commands, and skills as real code with real access. Claude Code and GPT Codex should use the same 0xArchive product truth: one authenticated request first, then expand into SDKs, CLI, MCP, skills, replay, or Data Catalog exports after the result is concrete.

## Venue Model

- Hyperliquid (perps): `/v1/hyperliquid/*`
- Hyperliquid Spot: `/v1/hyperliquid/spot/*`
- Hyperliquid HIP-3 (builder perps): `/v1/hyperliquid/hip3/*`
- Hyperliquid HIP-4 (outcome markets): `/v1/hyperliquid/hip4/*`
- Lighter.xyz: `/v1/lighter/*`

For large offline studies, use the Data Catalog to quote and export zstd-compressed Parquet. For production systems, use REST, WebSocket, SDKs, CLI, or MCP.
