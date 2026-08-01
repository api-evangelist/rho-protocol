---
name: Read Rho X market data
description: Fetch exchange info, tickers, order books, trades, candles, and volume stats from the Rho X (Rho Exchange) public REST API.
api: openapi/rho-protocol-openapi-original.json
operations:
  - GET /exchange/info
  - GET /tickers
  - GET /tickers/{symbol}
  - GET /symbols/{symbol}/order-book
  - GET /symbols/{symbol}/trades
  - GET /symbols/{symbol}/candles
  - GET /stats/volume
---

# Read Rho X market data

Public market-data endpoints require no authentication. Base URL: `https://x.rho.trading/api/v1`
(alternate `https://api.x.rho.trading/api/v1`).

## Steps

1. **Discover instruments** — `GET /exchange/info` returns supported symbols, markets, currencies, and fees (`dto.ExchangeInfoResponse`). Use it to resolve a tradable `symbol`.
2. **Get quotes** — `GET /tickers` for all tickers, or `GET /tickers/{symbol}` for one. Each ticker carries mid-rate, best bid/ask, 24h volume, and open interest.
3. **Read depth** — `GET /symbols/{symbol}/order-book` returns the bid/ask ladder (`dto.OrderBookEntry`).
4. **Recent prints** — `GET /symbols/{symbol}/trades` for public trade history.
5. **Candles** — `GET /symbols/{symbol}/candles` for OHLC; `GET /markets/{marketId}/floating-rate-candles` for floating-rate series.
6. **Volume** — `GET /stats/volume` for aggregate volume statistics.

## Conventions

- Prices and quantities are **strings** to preserve decimal precision.
- Respect rate limits: back off on `429`, honor `X-RateLimit-Limit` / `X-RateLimit-Remaining`.
- For real-time updates, subscribe to WebSocket public channels (`ticker.<symbol>`, `order-book.<symbol>`, `symbol-trades.<symbol>`) at `wss://stream.x.rho.trading/ws-api/v1` instead of polling.
