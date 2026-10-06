# Polymarket Crypto Up/Down Market Data — Lite Edition · Free Sample

[Polymarket historical data](https://outcometick.com/polymarket-historical-data) for the crypto Up/Down markets, collected 24/7 by [OutcomeTick](https://outcometick.com). This repository hosts a **free sample** of the
lite edition: one real, unmodified UTC day (2026-09-08), laid out exactly as the delivered archive, so code
written against the sample runs unchanged on the full data.

> **中文：** 本仓库是 [OutcomeTick](https://outcometick.com/zh) 采集的[Polymarket 历史数据](https://outcometick.com/zh/polymarket-historical-data)（加密 Up/Down 市场）lite 版的**免费样本**：一个真实、未经修改的
> UTC 日（2026-09-08），目录结构与正式交付的数据完全一致，针对样本写的代码可以原样用在正式数据上。

## Download / 下载

**[polymarket-lite-data-samples.tar.gz](https://github.com/outcometick/polymarket-lite-data-samples/releases/latest/download/polymarket-lite-data-samples.tar.gz)**

```bash
curl -L https://github.com/outcometick/polymarket-lite-data-samples/releases/latest/download/polymarket-lite-data-samples.tar.gz | tar xz
```

Per-file row counts and sha256: [`samples/manifest.json`](samples/manifest.json).
Field reference: [DATA_GUIDE.md](DATA_GUIDE.md) · 中文字段说明：[数据使用说明.md](数据使用说明.md)

## What the lite edition contains / lite 版包含的数据

- **Markets** — the opening price (price to beat) and the settled outcome of each 5m / 15m market
- **[Order book](https://outcometick.com/polymarket-order-book-data) snapshots** — full depth on both sides
- **Trades** — price, size, side, millisecond timestamp
- **[Chainlink settlement streams](https://outcometick.com/chainlink-settlement-data)** — the per-second price, TWAP30s and TWAP60s
- Every asset we collect, 5-minute and 15-minute markets; the 90 days up to the purchase date (a fixed window)

> **中文：** 市场信息（开盘价、结算结果）、盘口快照（完整深度）、逐笔成交、Chainlink 逐秒价与 TWAP30s / TWAP60s 结算流；全部币种、5 分钟 / 15 分钟市场；下单时最近 90 天（固定区间）。

## Files in this sample / 样本包含的文件

| path | rows |
|---|---|
| `data/chainlink/daily/prices/BTCUSD/BTCUSD-prices-2026-09-08.csv.gz` | 81,970 |
| `data/chainlink-twap-30s/daily/prices/BTCUSD/BTCUSD-twap30s-prices-2026-09-08.csv.gz` | 81,946 |
| `data/chainlink-twap-60s/daily/prices/BTCUSD/BTCUSD-twap60s-prices-2026-09-08.csv.gz` | 81,969 |
| `data/polymarket/daily/markets/BTC-5m/BTC-5m-markets-2026-09-08.jsonl.gz` | 292 |
| `data/polymarket/daily/book/BTC-5m/BTC-5m-book-2026-09-08.jsonl.gz` | 141,402 |
| `data/polymarket/daily/last_trade_price/BTC-5m/BTC-5m-last_trade_price-2026-09-08.jsonl.gz` | 480,491 |

## Learn more / 了解更多

- [OutcomeTick](https://outcometick.com) — prediction-market data for Polymarket and Predict.fun · [中文站](https://outcometick.com/zh)
- [Documentation](https://outcometick.com/docs) — quickstart and complete task examples · [中文文档](https://outcometick.com/zh/docs)
- [API reference](https://outcometick.com/docs/api) · [Data schemas](https://outcometick.com/docs/schemas) · [Settlement rules](https://outcometick.com/docs/settlement)
- [Settlement statistics for BTC](https://outcometick.com/data/polymarket/btc) — per-asset data page
- [Backtest in the browser](https://outcometick.com/backtest) — run a strategy on the archive without downloading anything

The full data is delivered with an API key and downloaded by day, asset and interval.
正式数据通过 API key 交付，按天、按币种、按周期下载。

For research and backtesting only; not investment advice. / 仅供研究与回测，不构成投资建议。
