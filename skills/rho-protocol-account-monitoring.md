---
name: Monitor a Rho X account
description: Read authenticated account state — balances, positions, open orders, trades, and margin accounts — from the Rho X REST API.
api: openapi/rho-protocol-openapi-original.json
operations:
  - GET /users/account
  - GET /users/balances
  - GET /users/balances/withdrawable
  - GET /users/positions
  - GET /users/orders
  - GET /users/trades
  - GET /users/transfers
  - GET /margin-accounts
  - GET /margin-accounts/{marginAccount}
---

# Monitor a Rho X account

These endpoints are user-scoped and require authentication. Send
`Authorization: Bearer <accessToken>` (or an API key) — a `ReadOnly` scope is sufficient.
Base URL: `https://x.rho.trading/api/v1`.

## Auth

1. Sign a nonce (`POST /auth-api/v1/nonce`) with the Ethereum wallet and exchange it at `POST /auth-api/v1/login` for an access token, **or** use a `ReadOnly` API key created in Rho X settings / `POST /apikeys`.

## Steps

2. **Account overview** — `GET /users/account` (and `GET /users/account/candles` for equity history).
3. **Balances** — `GET /users/balances`; `GET /users/balances/withdrawable` for withdrawable amounts.
4. **Positions** — `GET /users/positions` for open positions and margin details.
5. **Orders & fills** — `GET /users/orders` for open/recent orders, `GET /users/trades` for fills, `GET /users/transfers` for deposits/withdrawals.
6. **Margin accounts** — `GET /margin-accounts` (list) and `GET /margin-accounts/{marginAccount}` (+ `/candles`) for margin-account state.

## Conventions

- `401` = missing/expired credential; `403` = scope insufficient. Handle both explicitly.
- For live state, subscribe to private WebSocket channels (`user-orders`, `user-positions`, `user-balances`, `user-margin-account`) using a WS session token from `POST /auth-api/v1/ws-session`.
