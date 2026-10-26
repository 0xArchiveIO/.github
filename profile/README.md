<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/0xArchiveIO/.github/HEAD/profile/assets/hero-dark.png">
  <img alt="0xArchive: every fill, every wallet, Hyperliquid and Lighter. One 1-minute BTC candle opened up into the 2,913 fills inside it." src="https://raw.githubusercontent.com/0xArchiveIO/.github/HEAD/profile/assets/hero-light.png" width="800">
</picture>

[Website](https://www.0xarchive.io) · [Docs](https://docs.0xarchive.io) · [Quick start](https://docs.0xarchive.io/quickstart) · [Data Catalog](https://www.0xarchive.io/data) · [Pricing](https://www.0xarchive.io/pricing) · [Status](https://www.0xarchive.io/status)

</div>

Granular market data infrastructure for Hyperliquid and Lighter: live and historical order books down to the single order, every fill, funding, open interest, liquidations and every wallet's positions, through one API.

<sub>The chart: BTC on Hyperliquid, 2026-10-26 01:44 UTC. A candle shows one bar for that minute; trade history returns 2,913 fills from 1,211 wallets.</sub>

## Pick your route

| You want to | Repo | Start with |
| --- | --- | --- |
| Ask an agent, nothing to install | [0xarchive-mcp](https://github.com/0xArchiveIO/0xarchive-mcp) | Connect `https://mcp.0xarchive.io/mcp` and sign in with OAuth |
| Research and backtest with a coding agent | [0xarchive-quant](https://github.com/0xArchiveIO/0xarchive-quant) | `claude plugin marketplace add 0xArchiveIO/0xarchive-quant` |
| Work in Python | [sdk-python](https://github.com/0xArchiveIO/sdk-python) | `pip install oxarchive` |
| Work in TypeScript | [sdk-typescript](https://github.com/0xArchiveIO/sdk-typescript) | `npm install @0xarchive/sdk` |
| Work in Rust | [sdk-rust](https://github.com/0xArchiveIO/sdk-rust) | `cargo add oxarchive` |
| Script it, or run it in CI or cron | [0xarchive-cli](https://github.com/0xArchiveIO/0xarchive-cli) | `npx @0xarchive/cli auth test` |
| See working analysis first | [examples](https://github.com/0xArchiveIO/examples) | Run the liquidation, funding, HIP-3 or live-stream notebook |

Every route but MCP takes an API key: [create a free account](https://www.0xarchive.io/signup), copy a key, and run the [Quick start](https://docs.0xarchive.io/quickstart). Free keys read the most recent 30 days.

## Venues

| Venue | API prefix |
| --- | --- |
| Hyperliquid core perps | `/v1/hyperliquid` |
| Hyperliquid HIP-3 builder perps | `/v1/hyperliquid/hip3` |
| Hyperliquid HIP-4 outcome markets | `/v1/hyperliquid/hip4` |
| Hyperliquid Spot | `/v1/hyperliquid/spot` |
| Lighter mainnet | `/v1/lighter` |
| Lighter on Robinhood Chain | `/v1/rh-lighter` |

For large offline studies, the [Data Catalog](https://www.0xarchive.io/data) quotes and exports zstd-compressed Parquet. Agents can read [llms.txt](https://www.0xarchive.io/llms.txt) and the [OpenAPI spec](https://www.0xarchive.io/openapi.json).

## Agent safety

Give an agent the narrowest key and tool scope that answers its first question. MCP servers, shell commands and skills are real code with real access: start with one read, then widen.
